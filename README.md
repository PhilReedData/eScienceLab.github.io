# eScienceLab.github.io

website for eScience Lab, University of Manchester


Published at http://www.esciencelab.org.uk/

## License

&copy; 2015-- University of Manchester.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
</div>

Some resources are covered by other licenses or have different attributions, see [NOTICE](NOTICE) for details.

## Documentation

Website is generated by  [Jekyll](http://jekyllrb.com/d) and [GitHub Pages](https://pages.github.com/)

See the [Jekyll documentation](http://jekyllrb.com/docs/home/)

* Pages are edited in [MarkDown](https://daringfireball.net/projects/markdown/)
 * See also various Jekyll's documentation on [writing posts](http://jekyllrb.com/docs/posts/) and [writing pages](http://jekyllrb.com/docs/pages/)
* You can edit directly in GitHub web interface, or use `git` and your favourite editor
* Edited pages are published automatically by GitHub after a few minutes.
  * For extensive changes or debugging, you might want to `git clone` this repository and run [Jekyll](http://jekyllrb.com/) locally to test your changes and see debug outputs.
  * Test locally with Docker image [jekyll/jekyll:pages](https://hub.docker.com/r/jekyll/jekyll/):
    * `docker run -it --rm --name jekyll --volume=$(pwd):/srv/jekyll -p 4000:4000 jekyll/jekyll:pages`
    * Inspect at http://0.0.0.0:4000/ - edited files are updated live
    * Stop it with Ctrl-C or `docker stop jekyll`.

## Types of pages

The corresponding source file for a particular URL depends on what type it is.

### Regular pages

**Regular pages** like [about.md](about.md) correspond directly to pages on http://www.esciencelab.org.uk/, but with `/` as ending instead of `.md`, e.g. http://www.esciencelab.org.uk/about/.  These can be nested in folders, e.g.
[publications/index.md](publications/index.md) corresponds to http://www.esciencelab.org.uk/publications/,

Regular pages should have a header like this:

```markdown
---
layout: page
title: About
permalink: /about/
---
```

The `title` is used to generate the `<title>` and `<h1>` text, and `permalink` can be added to modify the final relative URI. If a page should NOT be included in the menu, then also add `exclude_from_nav: true`. 

Note that the MarkDown preview in GitHub might differ slightly from the final Jekyll's rendering on http://esciencelab.org.uk.


### Pages using Jekyll templates

The layout files and some of the top-level pages use [Jekyll Liquid Templates](https://jekyllrb.com/docs/templates/) to include content from their child pages.  For instance, [projects.md](projects.md) include:

```markdown
## Current funded projects

{% for project in site.projects %}
{% unless project.expired %}
* [{{ project.title }}]({{ project.url }}) - {{ project.description }}
{% endunless %}
{% endfor %}
```

You can recognize templates as using the `{{` or `{%` syntax. You should be more careful when editing 
these, e.g. by testing with your own Jekyll locally and check the logs.

In the example above, the properties are picked up from the headers of the 
files in the corresponding [_project](_project) folder. 


### Collection pages

The pages in `_` folders are called *collection pages*, because they are listed in their parent pages. For instance the folder [_products](_products) is used to generate http://www.esciencelab.org.uk/products/, where sub-pages like http://www.esciencelab.org.uk/products/researchobject/ correspond to [_products/researchobject.md](_products/researchobject.md).

It is important to maintain the special collection page _headers_; each collection folder has a different `layout` and (somewhat) differerent properties. The easiest is to copy from a neighbouring collection page that looks complete, for instance  [_projects/bioexcel.md](_projects/bioexcel.md) has Markdown headers like:

```markdown
---
layout: project
name: bioexcel
title: BioExcel
path: bioexcel.html
collection: projects
description: Centre of Excellence for Biomolecular Research
logo: bioexcel.svg
website: http://bioexcel.eu
start_date: 2015-11-01
duration: 36 months
project_reference: http://cordis.europa.eu/project/rcn/198303
---
```

These properties are picked up the the corresponding layout file in [_layouts](_layouts), e.g. [_layouts/product.html](_layouts/product.html) include:

```markdown
        <h1 class="post-title">{{ page.title }}</h1>
        <!-- .. -->
            <img src="{{ page.logo }}" alt="{{ page.title }}" height="75" max-height="100">
        
```

Some of the properties might also be picked up by the collection index page at the root, e.g. [products.md](products.md) or even the [index page](index.md).


### Resources

Images should be uploaded to [/images](/images), but could also be nested in a regular folder, e.g.
`gamble-mim-10.1109_eScience.2012.6404489.pdf` in [/publications/preprints/2012](/publications/preprints/2012) is shown in http://www.esciencelab.org.uk/publications/preprints/2012/gamble-mim-10.1109_eScience.2012.6404489.pdf. 

Note that unlike an Apache httpd server, no directory listing is generated, so unless an `index.md` file is provided or a page specifies the folder as its `permalink` property, then the corresponding parent, e.g. http://www.esciencelab.org.uk/publications/preprints/2012/ will say `404 Not Found`.  (Tip: the folder-listing is still public in GitHub, so the URLs aren't secret)


## Contributing

We appreciate any contributions to keep our website up to date. Feel free to 
raise a [pull request](https://github.com/eScienceLab/eScienceLab.github.io/pulls)
or raise an [issue](https://github.com/eScienceLab/eScienceLab.github.io/issues).
Every page should have an **Improve this page** link at the bottom, which you are free to use
to suggest a change.

