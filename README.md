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
#### This section is for research on relevant methods for calculating emissions from transportation. Document with all the methodologies previously researced by Group 1 can be found [here](https://docs.google.com/document/d/1lYmhqOsNPrKsHHmqBDZx6apvHNXIWH4zdgCUNXkfTMw/edit?usp=sharing). 

### Selected methodology
The emission calculations in our app is primarily based on the methodology and emission factors provided by the The Handbook Emission Factors for Road Transport (HBEFA). The emission factors from "HBEFA" are used for all road vehicles, while emission factors for "planes", "ferries" and "hybrid passenger cars" are taken from "The UK government greenhouse gas conversion factors".   

#### HBEFA
[The Handbook Emission Factors for Road Transport (HBEFA)](https://www.hbefa.net/e/index.html) provides emission factors for all current vehicle categories (PC, LDV, HGV, urban buses, coaches and motor cycles), each divided into different categories, for a wide variety of traffic situations. Emission factors for all regulated and the most important non-regulated pollutants as well as fuel/energy consumption and CO2 are included. 

The emission factors used in our app is taken from the HBEFA online version [online version](https://www.hbefa.net/e/index.html). The emission factors of the online version are weighted average values for the countries Germany, Austria, Switzerland, France, Norway and Sweden. The version only provide overall emission factors for the following pollutants: CO, CO2, HC, NOx and PM. In the online version, NOx is given in in nitrogen dioxide (NO2) equivalents, while the particulate matter (PM) components refer to PM10 (sizes up to 10 µm). However, the most important greenhouse gas emissions are that of CO2, CH4 (methane) and N20 (nitrus oxide). The CO2 emissions are calculated as “total CO2“ – based on the assumption that the carbon in the fuel is totally oxidised into CO2. Hydro carbons (HC) are differentiated into the following components: CH4, NMHC, Benzene, Toluene and Xylene. The CH4 and N2O emissions are calculated by their share in the total HC-emissions, which are not available in the online version. Thus, the current methodology for our app only calculates "total CO2" emissions from transportation, and does not include CH4 or N2O. The list of all emission factors currently used can be found in this [Excel file.](https://github.com/ENE425-Group1/emissions-calculator-group1/blob/main/notes/Emission%20Factors%20HBEFA.xlsx)

However, the objective is to calculate CO2 equivalents (CO2e) from CH4 and N20, i.e the relevant greenhouse gases from the transport sector, multiplied with their respective 100-year Global Warming Potentials (GWP) and sum them up with the total CO2 emission. HBEFA has defined the CO2e conversion factors in accordence with the [IPPC 2007](https://climatechangeconnection.org/emissions/co2-equivalents/), which gives us the following CO2e values: 
- CH4: 25
- N2O: 298
    
The calculation of CO2e requires the calculation of the following input pollutants:
- FC (fuel consumption in g/km) – required as input to calculate CO2 (reported)
- CO2 (reported)
- HC, since CH4 and N2O is derived from HC

Thus, in order to calculate CO2 equivalents we need more information on the share of CH4 and N2O in HC emissions. The [HBEFA development report](https://www.hbefa.net/e/documents/HBEFA41_Development_Report.pdf) gives further information on CH4 and N20. Especially, the report contains information on CH4/HC ratios, which is given in table 8 on p. 49. However, the shares are differentiated by aggregated emission concept (vehicle category and fuel type) and emission category (hot, cold start, evaporation), and are not given as weighted averages such as in the online version. 

#### Conversion Factors for Greenhouse Gas Reporting by the UK Government
[Here](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/891105/Conversion_Factors_2020_-_Condensed_set__for_most_users_.xlsx) are the conversion factors used by UK and international organisations to report on 2020 greenhouse gas emissions. For instance, one can find how many kilograms of CO2 emissions the different car types. [The UK Government greenhouse gas conversion factors](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/901692/conversion-factors-2020-methodology.pdf) also include detailed information about average emissions of cars (page 54), buses (p. 60), motorcycles (p. 61), rail (p.64) and aviation (p.76-78 and 81/82). It is distinguished between fuel types and even different brands. Developed out of this data, this [site](https://ourworldindata.org/travel-carbon-footprint) shows the carbon footprint per person per km with different means of transport.

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

- [Amazon Web Services (AWS)](https://aws.amazon.com/) is Amazon’s cloud platform. It is said to be the most comprehensive and adopted cloud platform. AWS can be used to deploy apps from GitHub repositories. 

- [Google Cloud Platform (GCP)](https://cloud.google.com/) is offered by Google and runs the same infrastructure that Google uses internally for its end-user products. GCP allows continuous deployment from GitHub repositories. 


Question 2. What options would you consider to make your app safer against attacks? (Attacks examples: Abusive requests that could crash your server; password theft)

- To avoid a crash in our server due bots attacks, we could implement a CAPTCHAs on our Website to have a "I'm not a robot" check. With this solution only humans would be able to use/login our website, for example through an imagen selection test. 
- To avoid password theft, the app can require Two-Factor Authentication to log in to the app. Two-Factor Authentication is a method of access control where a user is only given access after presenting two separate proofs of their identity, such as e-mail, SMS, etc. This can also be extended to three or more proofs of identity.
- For extreme security, user login may be integrated with Bank-ID. However, this will be limited to Norwegian users of the app.  
- Distributed Denial of Service (DDoS) attacks is when many different servers try to load the login/home page of the app simultaneously, causing it to eventually crash. To avoid this problem, the app should implement a early threat detection and traffic profiling systems. Another way to avoid this problem is to secure our network infrastructure, including advanced intrusion prevention and threat management systems, which combine firewalls, VPN, anti-spam, content filtering and load balancing. 
#### Week 9 - Task 5:
We decided which methodology we want to use for our app. The code in the app.py file has been updated according to the chosen methodology and we included the option to choose between light duty (< 3,5 t) and heavy duty (> 3,5 t) vehicles. Also the design of our app has been improved.
