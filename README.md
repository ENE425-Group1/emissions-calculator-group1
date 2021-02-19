# Emissions Calculator Group 1
## Hello and welcome!
#### This is group 1's project diary. As part of ENE425 Sustainable Energy's assessment, students are tasked with developing a *software application* to work out the transport carbon emissions of each group. The objective of the app is to explore how technology, public policy and our own personal decisions could contribute towards mitigating carbon emissions. This section is meant to be kept up to date so that everyone is able to follow the project as it progresses.

#### The directory tree for our Emmissions app below:

    +---Emissions_App
    |   app.py
    |   LICENSE
    |   Output_tree.doc
    |   Procfile
    |   python-app.yml
    |   requirements.txt
    |   
    +---notes
    |       .gitkeep
    |       module_design_v2.png
    |       
    +---static
    |       favicon.png
    |       
    \---templates
            add_record.html
            edit_or_delete.html
            error.html
            index.html
            list.html
            login.html
            result.html
            select_record.html

## Methodology Research
#### This section is for research on relevant methods for calculating emissions from transportation. When adding to this section, include a short description of the methodology and referances to the source material and other relevant research (*URL links*), as shown in the example below: 
 
#### *Example*
*This a short description of the findings of the research, and the methodology IEA has used to calculate the emission factors. The method is based on such and such research, and uses this and that data. The methodology is further described on this page: *URL link*. The research is similiar to several other sources on the issue, such as this research (*URL*) and this research (*URL*). On the other hand, there are also other findings with different results, such as the method used by "some statistic group" (*URL*), which gives lower emission factors. The majority of research, however, supports the described research.*

#### Defining the term "Vehicle"
To have a basic understanding it is important to have a classification of transport as urban transport or industrial transport (e.g. maritime, air). For a more segregated classification of the term "vehicle" under EC standards, this [link](https://www.eafo.eu/knowledge-center/european-vehicle-categories), connected to the last study of ["Determining the Environmental Impacts of Conventional and Alternatively Fuelled Vehicles Through LCA"](https://ec.europa.eu/clima/sites/clima/files/transport/vehicles/docs/2020_study_main_report_en.pdf) by Ricardo Energy and Environment for the European Comission. The segregation used in this study is practical for our purposes. However, a more advanced methodology is used than what is our intention with this app. 

#### Conversion Factors for Greenhouse Gas Reporting
[Here](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/891105/Conversion_Factors_2020_-_Condensed_set__for_most_users_.xlsx) are the conversion factors used by UK and international organisations to report on 2020 greenhouse gas emissions. For instance, one can find how many kilograms of CO2 emissions the different car types

The UK Government greenhouse gas conversion factors [https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/901692/conversion-factors-2020-methodology.pdf] also include detailed information about average emissions of cars (page 54), buses (p. 60), motorcycles (p. 61), rail (p.64) and aviation (p.76-78 and 81/82). It is distinguished between fuel types and even different brands.
Developed out of this data this site [https://ourworldindata.org/travel-carbon-footprint] shows the carbon footprint per person per km with different means of transport.

#### The Norwegian Emission inventory 2016 and IPCC and NFR methodology
This document shows how the Norwegian government calculates emissions. On the pages 49-74 it deals with the emissions from transport. Norway uses mainly the methodology from IPCC and NFR. The IPCC methodology to calculate emissions in the transport sector is explained in the following document: [https://www.ipcc.ch/site/assets/uploads/2018/02/ipcc_wg3_ar5_chapter8.pdf]. It shows the range of emissions for different means of transport on page 610. 
The NFR methodology is also used in the UK. You can find information about it in this document:[https://uk-air.defra.gov.uk/assets/documents/reports/cat07/1804121004_Road_transport_emissions_methodology_report_2018_v1.1.pdf]. CO2 emissions of cars, motorcycles and buses - distinguished by fuel type and type of drive (highway, city, etc.) - are stated on pages 32/33.

## Design changes

Given the purpose of our webpage, a sustainable web design which aims to minimize our environmental impact seems quite appropriate. As a general rule of thumb, a minimalistic design approach is sought after, while not comprimising user experience. Our proposals for web design changes, as well as sources with general guidelines on sustainable web design, can be found in our shared design document. Everyone is encouraged to share design ideas and pictures in the document, which can be found here: https://docs.google.com/document/d/15Gy1Lkh3RP-vnlTLJ4eCP6kqifS_cOSXQxEBNxlattw/edit?usp=sharing. 

Here is an examplatory "mockup" of a possible web design for our emission app: 

![Image of web design example](https://raw.githubusercontent.com/ENE425-Group1/emissions-calculator-group1/main/notes/Mockup%20picture.png)

## Weekly progress

#### Week 5 - Task 1: 
The coding environment here in GitHub was created. 
#### Week 6 - Task 2: 
We have uploaded files from a repository to our repository, and read a directory tree from other developers. 
#### Week 7 - Task 3: 
The diary team created a shared document for design change proposals, which can be accessed by the link in the "Design changes" section above. The app developement team have changed the layout for the app. They have changed the favicon and the background color to cde4da. In the index section they have changed the name to "Emissions calculator for ENE425, Group 1. 
#### Week 8 - Task 4: 

#### Post your suggestions to the questions below:
Question 1. What other cloud service can be used to deploy apps from github repo’s?

[Azure](https://azure.microsoft.com/en-us/free/search/?&ef_id=Cj0KCQiA4L2BBhCvARIsAO0SBdZmo_X3KZDPWmbj9okoBFuotwwPaxNOZVrtfouGt3bq-pfrAxJC9YMaAnugEALw_wcB:G:s&OCID=AID2100088_SEM_Cj0KCQiA4L2BBhCvARIsAO0SBdZmo_X3KZDPWmbj9okoBFuotwwPaxNOZVrtfouGt3bq-pfrAxJC9YMaAnugEALw_wcB:G:s) is Microsoft's own cloud solution (public cloud) and web portal and enables continuous deployment from GitHub.

[Amazon Web Services (AWS)](https://aws.amazon.com/) is Amazon’s cloud platform. It is said to be the most comprehensive and adopted cloud platform. AWS can be used to deploy apps from GitHub repositories’. 

[Google Cloud Platform (GCP)](https://cloud.google.com/) is offered by Google and runs the same infrastructure that Google uses internally for its end-user products. GCP allows continuous deployment from GitHub repository. 


Question 2. What options would you consider to make your app safer against attacks? (Attacks examples: Abusive requests that could crash your server; password theft)
    -
