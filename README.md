<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [A Global Good Project](#a-global-good-project)
  - [Introduction](#introduction)
  - [The Open Soil Spectral Library (OSSL)](#the-open-soil-spectral-library-ossl)
  - [OSSL Explorer](#ossl-explorer)
  - [OSSL manual](#ossl-manual)
- [Soil Data Research](#soil-data-research)
  - [Spectroscopy](#spectroscopy)
  - [Soil](#soil)
    - [Minerals](#minerals)
    - [Organic Matter (SOM)](#organic-matter-som)
    - [Structure](#structure)
    - [Organic Carbon (SOC)](#organic-carbon-soc)
  - [Example: Visual Analysis of Soil](#example-visual-analysis-of-soil)
  - [Soil Health](#soil-health)
- [START: Connecting to the OSSL](#start-connecting-to-the-ossl)
- [Exporting the OSSL as CSV](#exporting-the-ossl-as-csv)
  - [Exporting a Sample of the OSSL as CSV](#exporting-a-sample-of-the-ossl-as-csv)
- [WIP --> Building a Data Pipeline](#wip----building-a-data-pipeline)
- [END](#end)
  - [Visualizing the OSSL](#visualizing-the-ossl)
  - [About Us](#about-us)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

<!-----------------------------------------------  -->
<!-- Title:                                        -->
<!-----------------------------------------------  -->

# A Global Good Project

## Introduction

![Soil and prisma](images/dalle_earth_prisma.png)

Created with [DALL·E](https://labs.openai.com/s/MXs5BGiumacsHINDgiS3bOGg)

The purpose of this series of articles is to explore a path from data collection to data visualization and machine learning.

My background is in operations, analysis, and mathematics. Particular interest to me is the environment and the field of soil science concerning the **health** of the soil system.

Coincidentally, [Hackers News](https://news.ycombinator.com/item?id=32293359) led me to an article about the open soil spectral database.

## The Open Soil Spectral Library (OSSL)

The Open Soil Spectral Library (OSSL) is a global good project which serves collections of soil properties derived from spectral data. OSSL is also a network that delivers robust statistical models, calibration and prediction models, research tools, and opportunities to collaborate across borders.

The initiative received a funding award through the National Institute of Food and Agriculture (USDA).
[NIFA](https://www.nifa.usda.gov/about-nifa/press-releases/nifa-invests-over-7-million-big-data-artificial-intelligence-other) has invested over $7 Million in Big Data, Artificial Intelligence, and Other Cyberinformatics Research.

Among other valuable resources, the OSSL project offers beautifully developed software:

## [OSSL Explorer](https://explorer.soilspectroscopy.org/)

And the user manual, which is open for contributions:

## [OSSL manual](https://soilspectroscopy.github.io/ossl-manual/)

![Explorer](images/ossl_explorer.png)

<!-----------------------------------------------  -->
<!-- Title:                                        -->
<!-----------------------------------------------  -->

# Soil Data Research

## Spectroscopy

The importance of [spectroscopy](https://en.wikipedia.org/wiki/Spectroscopy) is centered around the fact that every element in the periodic table has a unique light spectrum.

[Soil spectroscopy](<(https://soilspectroscopy.org/about/#:~:text=Soil%20spectroscopy%20offers%20a%20safe%20and%20rapid%20alternative%20(Figure%201).&text=Soil%20spectroscopy%20is%20the%20measurement,applied%20to%20a%20soil%20surface.)>) is the measurement of light absorption when a light in the visible, near-infrared or mid-infrared (Vis–NIR-MIR) regions of the electromagnetic spectrum is applied to a soil surface.

![Spectroradiometer](images/spectroscopy.png)

The reflected infrared radiation is converted to electrical energy and fed to a computer for interpretation. Each major organic component of the soil absorbs and reflects light differently. By measuring these different reflectance characteristics, the Spectroradiometer and a computer determine the ingredients in the soil sample.

A typical soil spectrum in the (A) visible, (B) near-infrared, and (C) mid-infrared portion of the Electromagnetic Spectrum:

![Explorer](images/spectrum.png)
[Image Source: Advances in Agronomy](https://www.sciencedirect.com/topics/agricultural-and-biological-sciences/reflectance-spectroscopy#:~:text=NEAR%2DINFRARED%20REFLECTANCE%20SPECTROSCOPY%20ANALYSIS,%2C%20energy%2C%20and%20mineral%20content.)

Light absorption in the VIS region is due to the excitation of electrons.
For longer wavelengths, NIR-MIR, the absorption is due to [vibrations](https://youtu.be/QVOx4oFugts) in the chemical bonds within molecules: symmetrical stretch, asymmetrical stretch, and bending vibrations.

The spectra will show overtones and combinations of these vibrations, mainly in the NIR region.

Water has unique soil spectral features (Absorbance vs. Wavelength):

![Spectra_overtones_water](images/overtone_spectra.png)

## Soil

Soil is a living system working as a life-sustaining resource. It teams up with billions of bacteria, fungi, and other microbes to create an abundant [soil community](https://www.sciencedirect.com/topics/earth-and-planetary-sciences/microbial-community) filled with diverse soil biota.

Soils have [4 essential components](http://www.nzdl.org/cgi-bin/library?e=d-00000-00---off-0hdl--00-0----0-10-0---0---0direct-10---4-------0-1l--11-en-50---20-about---00-0-1-00-0-0-11----0-0-&a=d&c=hdl&cl=CL1.16&d=HASH412cd503b5262205ac14c6.3.1):

- Mineral particles: sand, silt, and clay
- Organic matter
- Water
- Air

Organism abundance, diversity, and activity are not randomly distributed in the soil but vary in a patchy fashion both horizontally across a landscape and vertically through the [soil profile](https://www.sciencedirect.com/topics/earth-and-planetary-sciences/soil-biota).

![Soil_horizons](images/soil_horizons_screens.png)
[Image Source: Soil Horizons](https://www.youtube.com/watch?v=_aZbGBaP_7Y)

Most soils evolve slowly over centuries through the weathering of underlying rocks and the decomposition of organic matter. Other soils are formed from deposits laid down by rivers, seas, or wind forces.

> A sample of typical [topsoil](http://www.nzdl.org/cgi-bin/library?e=d-00000-00---off-0hdl--00-0----0-10-0---0---0direct-10---4-------0-1l--11-en-50---20-about---00-0-1-00-0-0-11----0-0-&a=d&c=hdl&cl=CL1.16&d=HASH412cd503b5262205ac14c6.3.1) contains about
>
> - ~50% pore space filled with varying proportions of air and water, depending on the soil's current moisture content.
> - ~50% of the volume is made up of mineral particles and organic matter

> Organic soils formed in marshes, bogs, and swamps contain 30-100% organic matter.

### Minerals

Soil minerals give soil different texture attributes and colors. Minerals are classified by size:

![Soil_minerals](images/mineral_size.png)
[Image Source](https://www.nature.com/scitable/knowledge/library/what-are-soils-67647639/)

![Mineral_description](images/mineral_table.png)
[Image Source](https://www.ctahr.hawaii.edu/mauisoil/a_comp01.aspx)

The most common mineral in soils is quartz; it is not very reactive. But on the other hand, clay is very reactive.
Clay particles can form strongly protected structures that [store soil C](<(https://www.sciencedirect.com/topics/earth-and-planetary-sciences/soil-aggregate)>) for long periods.

These protected structures made with clay ensure good water-holding capacity and provide a good [source of plant nutrients](http://www.nzdl.org/cgi-bin/library?e=d-00000-00---off-0hdl--00-0----0-10-0---0---0direct-10---4-------0-1l--11-en-50---20-about---00-0-1-00-0-0-11----0-0-&a=d&c=hdl&cl=CL1.16&d=HASH412cd503b5262205ac14c6.3.4).

### Organic Matter (SOM)

Soil organic matter [SOM](<https://www.agric.wa.gov.au/measuring-and-assessing-soils/what-soil-organic-carbon#:~:text=Soil%20organic%20carbon%20(SOC)%20refers,to%20measure%20and%20report%20SOC.>) is composed mainly of carbon, hydrogen and oxygen, and has small amounts of other elements, such as nitrogen, phosphorous, sulfur, potassium, calcium and magnesium contained in organic residues. It is divided into ‘living’ and ‘dead’ components and can range from very recent inputs, such as stubble, to largely decayed materials that might be many hundreds of years old. About 10% of below-ground SOM, such as roots, fauna and microorganisms, is ‘living’:

SOM exists as 4 distinct fractions which vary widely in size, turnover time and composition in the soil (Table 1):

- dissolved organic matter
- particulate organic matter
- stable organic matter or humus
- resistant organic matter

### Structure

[Soil structure](https://www.sciencedirect.com/topics/earth-and-planetary-sciences/soil-structure) refers to the proportions of solids and voids. A key aspect of soil structure is the aggregation of individual mineral and organic particles into larger units.

Aggregates are separated into size classes: macroaggregates (250 μm–2 mm) and microaggregates (53–250 μm).

Macroaggregates are formed when [light fraction SOM](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0033217#:~:text=The%20light%20fraction%20is%20a,inputs%20and%20decomposition%20%5B31%5D.), which is composed of fresh plant residue, is decomposed by fungi and bacteria.

Bacterial secretion of high-molecular-weight sugar-based polymers (EPSs). These EPSs and fungal hyphae serve as nucleation cores to accrete larger masses of slightly decayed SOM that become macroaggregates. These macroaggregates are constantly weathering in the soil to produce microaggregates within SOM.

![Macro_micro_aggregates](images/soil_matrix.png)

![Macro_micro_aggregates](images/water_gas.png)
[Image Source: American Society of Microbiology](https://journals.asm.org/doi/10.1128/AEM.00324-19#)

### Organic Carbon (SOC)

Soil Organic Carbon [SOC](<https://www.agric.wa.gov.au/measuring-and-assessing-soils/what-soil-organic-carbon#:~:text=Soil%20organic%20carbon%20(SOC)%20refers,to%20measure%20and%20report%20SOC.>) refers to the carbon components in organic compounds. Soil organic matter (SOM) is challenging to measure directly, so laboratories tend to measure and report SOC. [Soil organic carbon](<https://www.agric.wa.gov.au/measuring-and-assessing-soils/what-soil-organic-carbon#:~:text=Soil%20organic%20carbon%20(SOC)%20refers,to%20measure%20and%20report%20SOC.>) is a measurable component of soil organic matter which contributes to nutrient retention and turnover, soil structure, moisture retention and availability, degradation of pollutants, and carbon sequestration. SOC has been identified as a [global indicator for monitoring soil health and productivity](https://www.openaccessgovernment.org/what-is-soil-organic-carbon-soc/120702/).

## Visual Analysis of Soil Example

![SOM composition](images/som.png)

> Below are four Swedish soils samples demonstrating the interaction of sand-and-clay textures versus SOM compositions

> ![Soil samples](images/sandVSsom_screen.png)
> Image Source: [FAO](https://youtu.be/QVOx4oFugts)(min: 37:42)

> - The Left samples are 100% sand, 0% clay.
> - The Right samples are illite clay soil samples; thus, they appear brighter in color.
> - The Bottom samples have no organic matter
> - The Top samples have very little organic matter; thus, they appear darker.

## Soil Health

The basic principles of soil health:

- Maximize Presence of Living Roots
- Maximize Soil Cover
- Maximize Biodiversity
- Minimize Disturbance

![Soil health](images/soil_health_screen.png)
[Image Source: USDA](https://www.nrcs.usda.gov/wps/portal/nrcs/main/soils/health/)

# START: Connecting to the OSSL

The OSSL manual mentioned two ways to access the data. The first method uses MongoDb via R; however, the last yields a certification error. See the image below:
![cert_error](images/cert_error.png)

As an alternative, we tried to connect directly with Javascript through NodeJS, but we also ran into another certificate error.

```
/Users/dev/code/soil_data_research/node_modules/mongodb/lib/utils.js:419
                    throw error;
                    ^

MongoServerSelectionError: certificate has expired
    at Timeout._onTimeout (/Users/dev/code/soil_data_research/node_modules/mongodb/lib/sdam/topology.js:293:38)
    at listOnTimeout (node:internal/timers:564:17)
    at process.processTimers (node:internal/timers:507:7) {
  reason: TopologyDescription {
    type: 'Unknown',
```

Lastly, we used the second method from the OSSL manual to access the data with Studio 3T and inserted the following parameters:

- Connection Name: `soilspec4gg`
- Server: `api.soilspectroscopy.org`
- Authentication DB: `soilspec4gg`
- User name: `soilspec4gg`
- Password: `soilspec4gg`
- Use SSL: `true`
- Accept any SSL certificates: `true`

Step 1: Free download [Studio 3T](https://robomongo.org/) and complete installation.

Step 2: In Studio 3T,

- Click on the New Collection icon:
  <!------------------------------------------------->
  <!-- image                                       -->
  <!------------------------------------------------->

  ![new collection icon](images/new_collection.png)

- select the `manually configure my connection setting` option
  ![auth step1](images/auth_screen1.png)
- Fill in the Connection name: `soilspec4gg` and, in the `Server` tab, fill with OSSL's given address: `api.soilspectroscopy.org`
  ![auth step2](images/auth_screen2.png)

- Go to the Authentication tab and select Basic Authentication Mode:
  ![auth step3](images/auth_screen3.png)

  - Fill in the User name, Password, and Authentication DB with `soilspec4gg`
    ![auth step4](images/auth_screen4.png)

- - Under the SSL tab, select `Use SSL protocol to connect` and `accept any server SSL certificates.
    ![auth step5](images/auth_screen5.png)

- Test Connection before saving:
  ![auth step6](images/auth_screen6.png)

- Finally, click save and connect.
  ![auth step7](images/auth_screen7.png)

# Exporting the OSSL as CSV

- Find the `soilsite` collection in `soispec4gg`
  ![export step1](images/export_screen1.png)
  ![export step2](images/export_screen2.png)

- Select `CSV` and click `Configure`
  ![export step3](images/export_screen3.png)

- Set the `Export Target` to be the current working directory. For instance, name the file `soilsite.csv` and save it.
  ![export step4](images/export_screen4.png)
  ![export step5](images/export_screen5.png)

- Click `Run`
  ![export step6](images/export_screen6.png)

- Results from the export are shown in the console.
  ![export step7](images/export_screen7.png)

- The data `soilsite_full.csv` is now exported to the current working directory.
  ![export step8](images/export_screen8.png)

## Exporting a Sample of the OSSL as CSV

To export a sample of the data, query a sample of 10 soil sites from the `soilsite` collection.

- Double click the `soilsite` collection.
  ![export sample step1](images/export_sample_screen1.png)

- Run the entire script (`F5`)
  ![export sample step2](images/export_sample_screen2.png)
  ![export sample step3](images/export_sample_screen3.png)

- Select 10 soil sites
  ![export sample step4](images/export_sample_screen4.png)

- Right-click anywhere inside the 10 sample query and select `Export Documents`
  ![export sample step5](images/export_sample_screen5.png)

- Select `Current Query Result`. Then follow the same steps to select and configure the CSV file described [earlier](#exporting-the-ossl-as-csv).
  ![export sample step6](images/export_sample_screen6.png)

# WIP --> Building a Data Pipeline

Because the VSC are long files, we decided to build a data pipeline to stream the data using SQLite:

```sql
=============
=============
```

And we used this SQL to query behind the web server:

```sql
=============
=============
```

Then we connected the database to [PyScript](https://github.com/pyscript/pyscript) and called the soil database with this code:

```python
=============
=============
```

We use [D3](htt`ps://react-d3-library.github.io/) to build this globe based on some modified instructions and added [Uber/h3](https://github.com/uber/h3), a hexagonal grid to partition the globe into hexagons (and a few pentagons).

Here is a link to the JSON file:

D3 plot and PyScript plot

# END

## Visualizing the OSSL

## About Us

Highlights of my background

<div>
    <ul>
        <li>Worked for Goldman Sachs</li>
        <li>Learning  to program with other technologies machine learning technologies</li>
        <li>Working with a team of developers to build a web application</li>
        <li>Experience in People Ops</li>
        <li>Enjoy preparing, growing and studying food plants </li>
        <li>People Operations complete cycles and Total Compensations Analisus</li>
        <li>JS, HTML, CSS, Python, SQL</li>        
    </ul>
</div>

I am available for contract work or full-time employment. I am also applying for environmental research graduate programs.

This I am collaborating with a team [chromatic.systems](chromatic.systems)

Here is a link to this project's code

The following post will explore a simple Machine Learning model.
