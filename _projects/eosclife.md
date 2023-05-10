---
layout: project
name: eosclife
title: EOSC-Life
path: eosclife
collection: projects
description: The EOSC-Life project develops an open collaborative space for digital biology in Europe
logo: eosc-life20k.png
website: http://www.eosc-life.eu/
start_date: 2019-03-01
duration: 54 months
project_reference: https://doi.org/10.3030/824087
---

[EOSC-Life](http://www.eosc-life.eu/) brings together the 13  Biological and Medical ESFRI research infrastructures (BMS RIs) to create an open collaborative space for digital biology.  It is our joint response to the challenge of analysing and reusing the prodigious amounts of data produced by life-science. Managing and integrating this data is beyond the capabilities of most individual end-users and institutes. By publishing data and tools in a Europe-wide cloud EOSC-Life aims to bring the capabilities of big science projects to the wider research community.  Federated user access (AAI) will allow transnational resource access and authorisation. EOSC-Life establishes a novel access model for the BMS RI: through EOSC scientists would gain direct access to FAIR data and tools in a cloud environment available throughout the European Research Area. 

Funded by call [H2020-INFRAEOSC-2018-2](https://cordis.europa.eu/programme/id/H2020_INFRAEOSC-04-2018) 824087, EOSC-Life will make BMS RIs data resources FAIR and publish  them in the EOSC following guidelines and standards (e.g. EDMI). Overall this will drive the evolution of the RI repository infrastructure for EOSC and integration of the BMS RI repositories. EOSC-Life will implement workflows that cross disciplines and RI boundaries and address the needs of interdisciplinary science. Through open hackathons and bring-your-own-data events we will co-create  EOSC-Life  with our user communities , providing a blueprint for how the EOSC supports wide-spread and excellent data-driven life science research. EOSC-Life will address the data policies needed for human research data under GDPR. Interoperable provenance information describe history of sample and data to ensure reproducibility and adherence to regulatory requirements.

The goal of the EOSC-Life project is to make sure that life-scientists can find, access and integrate life-science data for analysis and reuse in academic and industrial research. EOSC-Life will transform European life-science by providing an open, continent-scale, collaborative and interdisciplinary environment for data science.

## eScienceLab contribution

The eScience Lab is contributing in eScienceLab as part of ELIXIR-UK.

* WP1: Publishing FAIR RI data resources in EOSC
* WP2: _Tools Collaboratory_: Deployment of life-science data integration and analysis workflows in EOSC 
  * Implementation of a mechanism for publishing and sharing workflows across instances of the environment
* WP3: Demonstrators and Open Calls for User Projects

We will address cross-RI interoperability in the EOSC by fostering implementation of tools and workflows in
an integrated EOSC environment. To this end, this task will leverage pre-existing work on standardization and,
where possible, try to synergize with relevant efforts such as GA4GH Cloud Work Stream. 

The proposed integrated environment is to build on a limited number of components in the following areas:
* _software_ and _tools packaging_ will leverage existing efforts around package managers for software (e.g. [BioConda](https://bioconda.github.io/)) and containerization technology (e.g. [Docker](https://www.docker.com/), [Singularity](https://www.sylabs.io/singularity/)) with reference to standards from the [Open Containers Initiative](https://www.opencontainers.org/).
* _workflow composition_ and execution will rely on widely adopted standards for workflow specification (e.g. [Common Workflow Language](/activities/cwl/)) to ensure interoperability and re-usability across research infrastructure.
* an environment with a _graphical user interface_ (e.g. based on [Galaxy](http://galaxyproject.org/)) to support end-users with little or no experience in the design, customization and implementation of software pipelines.

![EOSC-Life architecture](/images/eosclife-architecture.png)

Tools and workflows must be findable and accessible. They should also be citable, have managed metadata profiles and openly available for review and analytics. The proposed registry solution will be built in the following components:

* A **Workflow Registry** based on a prior open source platform (e.g. myExperiment) that is workflow system agnostic, supports a repository of workflows in native and standardised form (e.g. CWL) and the virtual aggregation of established tool, workflow and registries to support discovery over a fragmented ecosystem.  The federated registry would support a common API to simplify access for tool developers.
* Standardised _workflow identifiers_ and _metadata descriptions_ (e.g. CWL) needed for workflow discovery, reuse, preservation, interoperability and monitoring and metadata harvesting using standard protocols.  Workflows are usually multi-component (requiring links to test data, example runs, explanatory documentation, etc) and used in collections for scientific use cases. We plan to use the Research Object specification for packaging workflows, which has already been combined with CWL and is part of the [BioComputeObject](http://biocomputeobject.org/) specification.
* Workflow snapshot preservation, publishing, citation and monitoring, credit claiming and workflows part of the scholarly communication landscape partnering with platforms like DataCite and EOSC’s OpenAIRE and their Research Community Dashboards linking publications with workflows, associated datasets, software, etc.

The workflow registry is planned to be based on the [SEEK platform](/products/seek/) using [Common Workflow Language](/activities/cwl/) and [Research Objects](/products/researchobject/) to glue in federated workflow and tool descriptions across the research infrastructures.

## Related pages

* [EOSC-Life homepage](http://www.eosc-life.eu/)
* [ELIXIR: The EOSC-Life project develops an open collaborative space for digital biology in Europe](https://elixir-europe.org/news/eosc-life-start)
* [BSC: EOSC-Life: Providing an open collaborative space for digital biology in Europe](https://www.bsc.es/es/research-and-development/projects/eosc-life-providing-open-collaborative-space-digital-biology)

## Related deliverables

Carole Goble, Stian Soiland-Reyes, Finn Bacall, Stuart Owen, Luca Pireddu, Simone Leo (2023):  
[**EOSC-Life Implementation of a mechanism for publishing and sharing workflows across instances of the environment**](https://doi.org/10.5281/zenodo.7886545).  
_EOSC-Life_, Project deliverable D2.3  
<https://doi.org/10.5281/zenodo.7886545>

Antonio Rosato, Jean-Karim Hériché (2022):  
[**EOSC-Life A common environment that can run cross-RIs workflows**](https://doi.org/10.5281/zenodo.7217294).  
_EOSC-Life_, Project deliverable D2.2  
<https://doi.org/10.5281/zenodo.7217294>

Florence Bietrix, José Maria Carazo, Salvador Capella-Gutierrez, Frederik Coppens, Maria Luisa Chiusano, Romain David, Jose Maria Fernandez, Maddalena Fratelli, Jean-Karim Heriche, Carole Goble, Philip Gribbon, Petr Holub, Robbie P. Joosten, Simone Leo, Stuart Owen, Helen Parkinson, Roland Pieruschka, Luca Pireddu, Luca Porcu, Michael Raess, Laura Rodriguez-Navas, Andreas Scherer, Stian Soiland-Reyes, Jing Tang, Gary Saunders  (2022):  
[**EOSC-Life Methodology framework to enhance reproducibility within EOSC-Life – revised version**](https://doi.org/10.5281/zenodo.7137744)
_EOSC-Life_, Project deliverable D8.1 (revised)  
<https://doi.org/10.5281/zenodo.7137744>

Helen Parkinson, Philip Gribbon, Ugis Sarkans, Gesa Witt, Andrea Zaliani, Manfred Kohler, Jason Swedlow, Jean-Marie Burel, Morris Swertz, Esther van Enckevort, Petr Holub, Marzia Massimi, Rafaele Matteoni, Holger Maier, Reetta Hinttala, Anne Heikkinen, Philipp Gormanns, Laurent Vasseur, Sophie Leblanc, Yann Herault, Dimitris Kontoyiannis, Christina Chandras, Dimitra Panou, José Miguel López Coronado, Rosa Aznar Novella, Vincent Robert, Ammar Ben Hadj Amor, Serge Casaregola, Jean-Luc Legras, Michel-Yves Mistou, Paolo Romano, Isabelle Perseil, Romain David, Roland Pieruschka, Katrina Exter, Marc Portier, Cedric Decruw, Steve Canham, Christian Ohmann, Sergey Goryanin, Laura Del Cano, Maddalena Fratelli, Carole Goble, Stuart Owen, Stian Soiland- Reyes, Nick Juty, Henriette Harmse, Dario Longo, Susanna Sansone, Allyson L. Lister, Peter McQuilton, Milo Tursthon, Ramon Granell, Hossein Mirian, Marco Roos, Luiz Bonino (2021):  
[**EOSC-Life EOSC FAIR services deployment for open calls**](https://doi.org/10.5281/zenodo.6208249).  
_EOSC-Life_, Project deliverable D1.3  
<https://doi.org/10.5281/zenodo.6208249>

Frauke Leitner, Jose Maria Carazo, Johanna Bischof, Natalie Haley, Pauline Audergon, Carlos Oscar Sorzano, Laura del Cano, Pablo Conesa, Cymon J. Cox, Gianluca De Moro, Corre Erwan, Katrina Exter, Gildas Le Corguillé, Romain Dallet, Lorraine Gueguen, Jean-Karim Heriche, Beatriz Serrano, Yi Sun, Jean-Marie Burel, Sara Zullino, Dario Livio Longo, Cyril Pommier, Asis Hallab, Constantin Eiteneuer, Romain David, Bjorn Usadel, Stuart Owen, Kristina Gruden, Roland Pieruschka, Alexander Sczyrba, Alfred Puhler, Martin Beracochea, Robert Finn, Philip Gribbon, Andrea Zaliani, Rachael Skyner, Frank von Delft, Ctibor Skuta, Andrew Leach, Jing Tang, Salvador Capella, José M. Fernández, Jordi Rambla, Sergi Beltran (2021):  
[**EOSC-Life Report on the work of the initial demonstrators**](https://doi.org/10.5281/zenodo.4817723).  
_EOSC-Life_, Project deliverable D3.2  
<https://doi.org/10.5281/zenodo.4817723>

Rudolf Wittner, Cecilia Mascia, Francesca Frexia, Heimo Müller, Jörg Geiger, Katrina Exter & Petr Holub (2021):  
[**EOSC-Life Common Provenance Model**](https://doi.org/10.5281/zenodo.4705074).  
_EOSC-Life_, Project deliverable D6.2  
<https://doi.org/10.5281/zenodo.4705074>

Helen Parkinson, Philip Gribbon, Ugis Sarkans, Gesa Witt, Andrea Zaliani, Manfred Kohler, Jason Swedlow, Jean-Marie Burel, Morris Swertz, Esther van Enckevort, Petr Holub, Marzia Massimi, Rafaele Matteonie, Holger Maier, Reetta Hinttala, Anne Heikkinen, Philipp Gormanns, Laura del Cano, Laurent Vasseur, Sophie Leblanc, Yann Herault, Dimitris Kontoyiannis, Christina Chandras, Dimitra Panou, José Miguel López Coronado, Rosa Aznar Novella, Vincent Robert, Ammar Ben Hadj Amor, Serge Casaregola, Jean-Luc Legras, Michel-Yves Mistou, Paolo Romano, Isabelle Perseil, Romain David, Roland Pieruschka, Katrina Exter, Marc Portier, Cedric Decruw, Steve Canham, Christian Ohmann, Sergey Goryanin, Laura Del Cano, Maddalena Fratelli, Carole Goble, Stuart Owen, Stian Soiland-Reyes, Nick Juty, Susanna Sansone, Peter McQuilton, Marco Roos, Luiz Bonino (2021):  
[**EOSC-Life EOSC repository deployment for project demonstrators**](https://doi.org/10.5281/zenodo.4432029).  
_EOSC-Life_, Project deliverable D1.2  
<https://doi.org/10.5281/zenodo.4432029>

Antonio Rosato, Jean-Karim Hériché, Beatriz Serrano-Solano, Björn Grüning, Luca Pireddu & Carole Goble (2020):  
[**EOSC-Life Cloud implementation of exemplary workflows**](https://doi.org/10.5281/zenodo.4010401).  
_EOSC-Life_, Project deliverable D2.1  
<https://doi.org/10.5281/zenodo.4010401>
