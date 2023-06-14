
# FishMIP_2023_3b_Protocol

### <u>Contents</u>

[Goal \[2\]](#goal)

[Experiments & Scenarios \[3\]](#experiments-scenarios)

[Input data \[6\]](#input-data)

[Climate forcing \[6\]](#climate-forcing)

[Fishing forcing \[11\]](#fishing-effort-forcing)

[Output data \[14\]](#output-data)

[Additional notes for Regional FishMIP Models
\[16\]](#additional-notes-for-regional-fishmip-models)

[Reporting model results \[16\]](#reporting-model-results)

## 

## Goal

The goal of FishMIP’s “Fish Futures” Protocol is to assess adaptation
pathways to climate change under different societal and fisheries
management development pathways. This simulation round extends our
previous CMIP6 climate impact projections to include past and future
fisheries development to enable us to identify key risks and adaptation
to climate change including consequences for biodiversity, fisheries and
food security.

The future scenarios we are using have been developed to be consistent
with each of the [Shared Socioeconomic
Pathways](https://www.climateforesight.eu/seeds/shared-socioeconomic-pathways/),
but with explicit additional details needed for fisheries and
aquaculture development, are called Ocean System Pathways (OSPs) (Maury
et al. 2023 - TO BE SUBMITTED).

This protocol provides details on the experimental set-up and data
forcings required to run each of these scenarios, with and without
climate change.

Note that this protocol builds on the FishMIP’s [“CMIP6” Phase
1](https://github.com/Fish-MIP/FishMIP_2023_3b_Protocol/blob/main/FishMIP_Phase1_2020_CMIP6_runs_protocol_v1.0.pdf)
protocol which focused primarily on results without fishing, for
fast-track inclusion in the IPCC 6th Assessment. Modellers are welcome
to redo previous Phase 1 runs with new versions of their models that
have had improvements following the FishMIP [“Model
Evaluation”](https://github.com/Fish-MIP/FishMIP_2022_3a_Protocol)
protocol round.

Timelines for simulations: TO BE DISCUSSED

| Scenarios                     | Models           | Date          |
|-------------------------------|------------------|---------------|
| Historical (See Table X)      | global, regional | July 1st 2024 |
| OSPs (See Table X)            | global, regional | Oct 1st, 2024 |
| Additional runs (See Table X) | global           |               |

To aid with progress we will hold specific technical workshops to:

- Ensure correct OSP integration inputs and access

- Ensure fishing drivers work (separate global and regional breakaway
  groups)

- Tool sharing & troubleshooting

- Check model outputs/issues

In this document we describe the general experimental and scenario
set-up (Section 3). Further down in Section 4 we include the details of
the specific **input** variables that modellers can use to implement
scenarios. In Section 5 we describe the set of **outputs** to be
created. Finally in Sections 6-7 we provide further **notes** and
**instructions** on how to report and upload model results.

This protocal is a contribution to the wider Inter-Sectoral Model
Intercomparison Project (ISIMIP3b) simulation round, further details can
be found here:

[https://protocol.isimip.org/#ISIMIP3b/marine-fishery_regional/marine-fishery_global](https://protocol.isimip.org/)

**For this simulation round, we are asking you to run XXXXXXXX**

## Experiments & Scenarios

Each model experiment is a set of model simulations that has a
particular goal (e.g. model evaluation). A scenario is a particular
setting for forcing drivers that describes how each model run should be
set up in the experiment, including both the type of climate forcing
(CF) and the type of direct human forcing (DHF). All model runs are to
be carried out using each Earth System Model ().

**Modellers that have already completed Phase 1 runs can skip to Phase 2
below, unless they wish to update runs based on improvements since the
Model Evaluation simulation round. Please prioritize the core ‘priority’
runs below, and provide the ‘optional’ if possible.**

##### Table 1: Control run and historical simulation experimental set-up. Note that each simulation is specified by the Climate forcing and Fishing forcing. Definitions of the specifiers (e.g. nat, picontrol etc.) that are used for ISIMIP filenaming are provided in Tables 3 and 4 below.

<table style="width:98%;">
<colgroup>
<col style="width: 5%" />
<col style="width: 24%" />
<col style="width: 38%" />
<col style="width: 15%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th>No.</th>
<th>Experiment</th>
<th>Short description</th>
<th>Time period and specifiers</th>
<th>Phase</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td><strong>Pre-industrial control</strong></td>
<td><p><strong>Climate</strong>: No climate change, fixed 1850s
CO<sub><code>2</code></sub> levels</p>
<p><strong>Fishing</strong>: No fishing</p></td>
<td><p>1850-2100</p>
<p>picontrol</p>
<p>nat</p></td>
<td>1 (optional re-runs only)</td>
</tr>
<tr class="even">
<td>2</td>
<td><strong>Historical fishing effort, no climate</strong></td>
<td><p><strong>Climate</strong>: No climate change, fixed 1850s
CO<sub><code>2</code></sub> levels</p>
<p><strong>Fishing</strong>: Historical fishing effort, forced directly
by effort data</p></td>
<td><p>1850-2014</p>
<p>picontrol</p>
<p>histsoc</p></td>
<td>1 (optional re-runs only)</td>
</tr>
<tr class="odd">
<td>3</td>
<td><strong>Historical fishing dynamics, no climate</strong></td>
<td><p><strong>Climate</strong>: No climate change, fixed 1850s
CO<sub><code>2</code></sub> levels</p>
<p><strong>Fishing</strong>: Historical fishing dynamics, forced by OSP
drivers</p></td>
<td><p>1850-2014</p>
<p>picontrol</p>
<p>histsocOSP</p></td>
<td>2 (priority)</td>
</tr>
<tr class="even">
<td>4</td>
<td><strong>Historical climate only</strong></td>
<td><p><strong>Climate</strong>: Simulated<strong>/reanalysis?</strong>
historical climate change</p>
<p><strong>Fishing</strong>: No fishing</p></td>
<td><p>1850-2014</p>
<p>historical</p>
<p>nat</p></td>
<td>1 (optional re-runs only)</td>
</tr>
<tr class="odd">
<td>5</td>
<td><strong>Historical climate and fishing effort</strong></td>
<td><p><strong>Climate</strong>: Simulated<strong>/reanalysis?</strong>
historical climate change</p>
<p><strong>Fishing</strong>: Historical fishing effort, forced directly
by effort data</p></td>
<td><p>1850-2014</p>
<p>historical</p>
<p>histsoc</p></td>
<td>1 (optional re-runs only)</td>
</tr>
<tr class="even">
<td>6</td>
<td><strong>Historical climate and fishing dynamics</strong></td>
<td><p><strong>Climate</strong>: Simulated<strong>/reanalysis?</strong>
historical climate change</p>
<p><strong>Fishing</strong>: Historical fishing dynamics, forced by OSP
drivers</p></td>
<td><p>1850-2014</p>
<p>historical</p>
<p>histOSP</p></td>
<td>2 (priority)</td>
</tr>
</tbody>
</table>

#### Note on spin-up period (pre-1850)

For fishing effort prior to 1850 hold fishing at 1850 levels.  
  
For the ‘no fishing’ runs (nat), the spin-up should not use any fishing
effort.  

##### Table 2: Future scenarios simulation experimental set-up. Note that each simulation is specified by the Climate forcing and Fishing forcing. Definitions of the specifiers (e.g. nat, picontrol etc.) that are used for ISIMIP filenaming are provided in Tables 3 and 4 below.

<table style="width:99%;">
<colgroup>
<col style="width: 3%" />
<col style="width: 30%" />
<col style="width: 41%" />
<col style="width: 12%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th>No.</th>
<th>Simulation</th>
<th>Short description</th>
<th>Time period and specifiers</th>
<th>Phase</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1-5</td>
<td><strong>All SSPs (1-5), no climate change, OSP1-5
fishing</strong></td>
<td><p><strong>Climate</strong>: No climate change</p>
<p><strong>Fishing</strong>: OSP1-5 future fisheries dynamics (following
on from historical OSP)</p></td>
<td><p>2015-2100</p>
<p>picontrol</p>
<p>OSP1soc</p></td>
<td>2, priority</td>
</tr>
<tr class="even">
<td>6-10</td>
<td><strong>All SSPs with climate change (SSP1RCP2.6, SSP5RCP8.5) , no
fishing</strong></td>
<td><p><strong>Climate</strong>: SSP-RCP climate scenarios
(e.g. SSP1RCP2.6, SSP5RCP8.5)</p>
<p><strong>Fishing</strong>: No fishing</p></td>
<td><p>2015-2100</p>
<p>ssp&lt;scen&gt;</p>
<p>nat</p></td>
<td>1 (optional re-runs only)</td>
</tr>
<tr class="odd">
<td>11-15</td>
<td><strong>All SSPs with climate change (SSP1RCP2.6, SSP5RCP8.5) and
OSP fishing</strong></td>
<td><p><strong>Climate</strong>: SSP-RCP climate scenario,
(e.g. SSP1RCP2.6, SSP5RCP8.5)</p>
<p><strong>Fishing</strong>: OSP1-5 future fisheries dynamics (matched
to each SSP, e.g. SSP1RCP2.6 would use OSP1)</p></td>
<td><p>historical</p>
<p>OSP&lt;x&gt;soc</p></td>
<td>2 priority</td>
</tr>
</tbody>
</table>

#### Scenario definitions

Throughout the protocol we use ‘specifiers’ that are shortened names
used to denote a particular scenario, variables, or other parameter in
the filenames of model inputs and outputs. It is crucial that you also
use the same specifiers in your output files.  
  
**Correct formatting and naming of output files are essential for model
intercomparison and analysis.**  
  
Tables 2-4 describe the different scenarios for the model runs described
in Table 1. These specifiers are used in the file names of the
corresponding input files and should also be used for the names of the
output files (see 
[7](https://protocol.isimip.org/#reporting-model-results). Reporting
model results).

##### Table 3: Climate scenario specifiers (climate-scenario).

| **Scenario specifier** | **Description**                                                       |
|:-----------------------|:----------------------------------------------------------------------|
| picontrol              | Pre-industrial climate as simulated by the Earth System Models (ESMs) |
| historical             | Historical climate as simulated by the ESMs, starting in 1950.        |
| ssp126                 | SSP1-RCP2.6 climate as simulated by the ESMs                          |
| ssp585                 | SSP5-RCP8.5 climate as simulated by the ESMs.                         |
| sspXXX                 | ANY OTHERS?                                                           |

##### Table 4: Socio-economic scenario specifiers (soc-scenario).

| **Scenario specifier** | **Description**                                                                                                     |
|:-----------------------|:--------------------------------------------------------------------------------------------------------------------|
| **histsoc**            | Varying direct human influences in the historical period (1850-2014) (i.e. historical estimates of fishing effort). |
| **2015soc**            | Fixed year-2015 direct human influences (i.e. fishing effort).                                                      |
| **OSP\<x\>soc**        | Future fishing determined by SSP and OSP driver forcings for OSP\<x\>, where \<x\> is 1-5.                          |
| **nat**                | No fishing (naturalized run).                                                                                       |

**Please remember to use these same specifiers in your output files.
More on reporting data can be found at the end of this document.**

## Input data

**For modellers new to FishMIP:** to access all input data you first
need to set up an account with ISIMIP to access the DKRZ server. Please
follow the instructions here:
<https://www.isimip.org/dashboard/accessing-isimip-data-dkrz-server/>

### Climate forcing

##### Table 5: Climate forcing

| Title      | Specifiers  | Institution                                                                                                      | Original resolution |
|:-----------|:------------|:-----------------------------------------------------------------------------------------------------------------|:--------------------|
| GFDLESM4   | gfdlesm4    | National Oceanic and Atmospheric Administration, Geophysical Fluid Dynamics Laboratory, Princeton, NJ 08540, USA | 288x180             |
| IPSLCM6ALR | ipslcm6a-lr | Institut Pierre Simon Laplace, Paris 75252, France                                                               | 144x143             |
| OTHERS??   |             |                                                                                                                  |                     |

##### Table 6. Climate forcing variables and units for FishMIP 3a simulations. All variables are available on a 0.25 and 1 degree horizontal grid, monthly and annual resolutions. Note: Some variables are available as specific layers extracted from vertically resolved data. Their variable names have been suffixed with -bot (ocean bottom, e.g. o2-bot), -surf (surface values, e.g. pH-surf) or -vint (vertically integrated, e.g. phyc-vint), respectively, or prefixed with int (vertically integrated, e.g. intpp). Temperature is suffixed with b or s for bottom (e.g. tob) or surface (e.g. tos) layers, respectively.

<table style="width:98%;">
<colgroup>
<col style="width: 51%" />
<col style="width: 13%" />
<col style="width: 9%" />
<col style="width: 12%" />
<col style="width: 10%" />
</colgroup>
<thead>
<tr class="header">
<th>Variable</th>
<th>Specifier</th>
<th>Unit</th>
<th>Resolution</th>
<th>ESM datasets</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mass Concentration of Total Phytoplankton Expressed as
Chlorophyll</td>
<td><strong>chl</strong></td>
<td>kg m-3</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Sea Floor Depth</td>
<td>*deptho**</td>
<td>m</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Downward Flux of P articulate Organic Carbon</td>
<td><strong>exp c-bot</strong></td>
<td>mol m-2 s-1</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>P articulate Organic Carbon Content</td>
<td>* intpoc**</td>
<td>kg m-2</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Primary Organic Carbon Production by All Types of Phytoplankton</td>
<td><strong>intpp</strong></td>
<td>mol m-2 s-1</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Net Primary Organic Carbon Production by Diatoms</td>
<td><strong>intp pdiat</strong></td>
<td>mol m-2 s-1</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Net Primary Mole Productivity of Carbon by Diazotrophs</td>
<td><strong>intp pdiaz</strong></td>
<td>mol m-2 s-1</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Net Primary Mole Productivity of Carbon by Picophytoplankton</td>
<td><strong>intp ppico</strong></td>
<td>mol m-2 s-1</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Maximum Ocean Mixed Layer Thickness Defined by Sigma T</td>
<td><p>*mlotst</p>
<p>-0125**</p></td>
<td><p>m</p>
<p>m</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Dissolved Oxygen Concentration</td>
<td><p><strong>o2,</strong></p>
<p><strong>o 2-bot</strong></p>
<p><strong>o2 -surf</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>pH</td>
<td><p><strong>ph</strong></p>
<p><strong>ph-bot</strong></p>
<p><strong>ph -surf</strong></p></td>
<td><p>1</p>
<p>1</p>
<p>1</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Phytoplankton Carbon Concentration</td>
<td><p>*phyc**</p>
<p><strong>phyc -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Mole Concentration of Diatoms expressed as Carbon in sea water</td>
<td><p><strong>phydiat</strong></p>
<p><strong>phydiat -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Mole Concentration of Diazotrophs Expressed as Carbon in Sea
Water</td>
<td><p><strong>phydiaz</strong></p>
<p><strong>phydiaz -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Mole Concentration of Picophytoplankton Expressed as Carbon in Sea
Water</td>
<td><p><strong>phypico</strong></p>
<p><strong>phypico -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Sea Water Salinity</td>
<td><p><strong>so</strong></p>
<p><strong>so-bot</strong></p>
<p><strong>so -surf</strong></p></td>
<td><p>‰</p>
<p>‰<br />
‰</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Sea Water Potential Temperature</td>
<td><strong>thetao</strong></td>
<td>°C</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Ocean Model Cell Thickness</td>
<td><strong>thkcello</strong></td>
<td>m</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Sea Water Potential Temperature at Sea Floor</td>
<td><strong>tob</strong></td>
<td>°C</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Sea Surface Temperature</td>
<td><strong>tos</strong></td>
<td>°C</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Sea Water X Velocity</td>
<td><strong>uo</strong></td>
<td>m s-1</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Sea Water Y Velocity</td>
<td><strong>vo</strong></td>
<td>m s-1</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Mole Concentration of Mesozooplankton expressed as Carbon in sea
water</td>
<td><p><strong>zmeso</strong></p>
<p><strong>zmeso -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Mole Concentration of Microzooplankton expressed as Carbon in sea
water</td>
<td><p><strong>z micro</strong></p>
<p>*zmicro</p>
<p>-vint**</p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Zooplankton Carbon Concentration</td>
<td><p>*zooc**</p>
<p><strong>zooc -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Net Downward Shortwave Radiation at Sea Water Surface</td>
<td><strong>rsntds</strong></td>
<td>W m-2</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Sea Ice Area Fraction</td>
<td><strong>siconc</strong></td>
<td>%</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
</tbody>
</table>

### Climate forcing file locations

The climate forcing input files can be found using the following
pattern:

``` linux
levante:/work/bb0820/ISIMIP/ISIMIP3b/InputData/climate/ocean/uncorrected/<glob
al or regional>/monthly/<climate-scenario>/<climate-forcing>/<climateforcing>_<ensemble-member>_<climate-scenario>_<climatevariable>_global_monthly_<start-year>_<end-year>.nc
```

The variables **deptho** and **thkcello** are fixed through time and can
be found in the “fixed/” folder (rather than monthly/).

#### Note on phytoplankton size structure inputs

Production and carbon data for large and small phytoplankton can be
derived from the variables in Table 1 by the following:

large = diatoms + diazotrophs

small = picophytoplankton

The GFDL model treats diazotrophs as large phytoplankton as part of
their food-web processes.

#### Note on regional model spatial extractions

For regional models, only specific grid cells will be needed from the
above global outputs. Please let us know if you require assistance to
extract results (e.g. using bounding boxes, masks or shapefiles). This
functionality is now partially available (bounding box) through the
ISIMIP web-based [data portal](https://data.isimip.org/).

A simple worked example on how to do this for specific regions in R is
provided here: <https://github.com/Fish-MIP/FishMIP_extracting-data>

### Fishing effort forcing - NEEDS TO BE UPDATED - OSPs

##### Table 7: Fishing effort forcing files and variables for FishMIP 3b simulations.

<table style="width:99%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 69%" />
<col style="width: 12%" />
<col style="width: 5%" />
</colgroup>
<thead>
<tr class="header">
<th>Specifier</th>
<th>Included variables (short names) and definitions</th>
<th>Time period /Resolution</th>
<th>Filename</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>histsoc</td>
<td><p>NomActive = Nominal fishing effort of the active fleet
dis-aggregated by:</p>
<ul>
<li><p>eez_country_name = The exclusive economic zone/high seas name in
which fishing effort is occurring</p></li>
<li><p>LME = A number code of the Large Marine ecosystem in which the
Effort is occurring</p></li>
<li><p>SAUP = A number code for the fishing country, following Sea
Around Us numbering</p></li>
<li><p>Gear = the fishing gear</p></li>
<li><p>FGroup = the targeted functional group</p></li>
<li><p>Sector = the fishing sector defined by the law of the
country</p></li>
</ul></td>
<td><ul>
<li><p>1850-2015</p></li>
<li><p>Annual</p></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>2015soc</td>
<td>Final year of values from histsoc repeated until 2100</td>
<td><ul>
<li><p>2015-2100</p></li>
<li><p>Annual</p></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>OSP1soc</td>
<td>Which variables? Determined from % change relative to 2015 in
SSP1Population, SSP1GDP and relative change to 2015 (drivers of?)
fishing effort</td>
<td><ul>
<li><p>2015-2100</p></li>
<li><p>Annual</p></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>OSP2soc</td>
<td>Which variables? Determined from % change relative to 2015 in
SSP5Population, SSP5GDP and relative change to 2015 (drivers of?)
fishing effort</td>
<td><ul>
<li><p>2015-2100</p></li>
<li><p>Annual</p></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Historical Population</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Historical GDP</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>OTHERS?</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>SSP1 Population</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>SSP1GDP</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>SSP5P opulation</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>SSP5 GDP</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

##### Table 8: Metadata for histsoc fishing effort variables.

| Variable Name       | Long name                                                                                | Unit             | Description/notes                                                                                                                                                                                                                                                                                          |
|:--------------------|:-----------------------------------------------------------------------------------------|:-----------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Year                | (End of the) year when the fishing effort is occurring                                   | Number code      |                                                                                                                                                                                                                                                                                                            |
| Sector              | The fishing sector defined by the law of the country                                     | Name code        | I = Industrial and A = artisanal, where artisanal include powered and unpowered artisanal fleets                                                                                                                                                                                                           |
| LME                 | Large Marine Eco system Number                                                           | Number code      | A number code of the Large Marine ecosystem in which the Effort is occurring                                                                                                                                                                                                                               |
| eez\_ countr y_name | Exclusive Economic Zone                                                                  | Name code        | The country-level exclusive economic zone (or high seas) name in which fishing effort is occurring                                                                                                                                                                                                         |
| SAUP                | A number code for the fishing country, fol lowing Sea Around Us numbering                | Number code      | Ex supranational entities (USSR, Yugoslavia) are disaggregated to their constituent countries. Serbian Fishing Effort included with Montenegro. Crimea included with Ukrainian.                                                                                                                            |
| Gear                | The fishing gear                                                                         | Name code        | Gear names                                                                                                                                                                                                                                                                                                 |
| FGroup              | The targeted functional group                                                            | Name code        | Functional groups are in accordance with those used by the Sea Around Us Project                                                                                                                                                                                                                           |
| Nom Active          | Nominal fishing effort (i.e., not including the technological creep) of the active fleet | Days at sea X kW | NomActive (of the active fleet; i.e., total) = P (engine power of active the fleet; i.e., total) x DAS (average days at sea of one vessel). Average DAS for one vessel \~ 200 DAS/year. NomActive corresponds to the total (reported, IUU, discards) catch. To find NomActive in DAS do (NomActive/P) X NV |

##### Table 9: Details for OSP relative change in drivers of fishing effort variables. HOW TO DESCRIBE HOW WE WILL VARY MANAGEMENT IN THE MODELS ACROSS OSPs??

| OSP  | Management                                 |
|------|--------------------------------------------|
| OSP1 | All stocks fished at Fmsy or B/B0 \> 0.5?? |
| OSP5 | Fmsy or B/B0??                             |

#### Implementation of OSPs

TO DO: We provide code examples showing how to implement the OSPs… NEED
TO ADD TO GITHUB REPO

##### Table 8: Metadata for fishing effort variables.

#### Fishing effort forcing file locations

The monthly fishing effort forcing files for the spin-up and experiments
(Table 1) of this simulation protocol can be found on DKRZ here:

``` linux
levante:/work/bb0820/ISIMIP/ISIMIP3b/InputData/socioeconomic/fishing/histsoc/
```

#### Note on global model fishing effort forcing

For **global models**, the above spatially aggregated fishing effort can
be spatially allocated into 0.25 grid cells. This can be achieved using
different approaches such as a simple gravity model – e.g. see [Coll et
al. 2020](https://www.frontiersin.org/articles/10.3389/fmars.2020.567877/full)
but details will depend on model structure.

We are developing a simplified worked example for global modellers to
explore and contribute to. This will be made available on github/FishMIP
in due course.

While we recommend using the above spatially aggregated effort, for
**global models** that cannot technically carry out spatial allocation
of effort, gridded total industrial and artisanal nominal active effort
have been provided in the same folder as the file above and are saved as
netcdf files. These can be allocated to functional groups
(e.g. according to relative biomass) depending on model structure.

#### Note on regional model fishing effort forcing

Downscaling of the above fishing effort to match regional model inputs
is likely to be needed. We request that regional modellers work together
in their specific regions to ensure we have clear and common
methodologies.

We are developing a worked example for regional modellers to explore and
contribute to for their region which will be made available on
github/FishMIP in due course.

#### Note on model calibration using fishing catch data and model evaluation requirements

Modellers are permitted to calibrate or tune their models using
historical fisheries catch data (that will also be used for model
evaluation) on the condition that **only years up to and including
2004** are used in model calibration/tuning.

Modelling groups **must** keep **detailed documentation** on how their
model was calibrated (e.g. input forcing, calibration data, time domain,
spatial domain, fish grouping (size, functional types, total),
optimization metric(s), weighting schemes, etc.) to be included in
manuscript methods. Written description of sources of calibration data
and methods used need to be provided with all simulation outputs. A
template will be provided for this documentation in due course.

The fisheries catch data .csv file that can be used for model
calibration is here:

``` linux
levante:/work/bb0820/ISIMIP/ISIMIP3a/InputData/socioeconomic/fishing/histsoc/calibration_catch_histsoc_1850_2004.csv.
```

The fisheries catch data are already aggregated into the functional
groups and spatial zones as the above effort forcing data. The original
reference including links to full database is [Watson & Tidd, 2018,
Marine Policy, 93:
171-177](https://www.sciencedirect.com/science/article/pii/S0308597X18300605).

### **Other static geographic information**:

Large marine ecosystem (LME) masks in four different spatial
resolutions. 0.1°, 0.25°, 0.5° and 1° are available here:

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/InputData/geo_conditions/fishmip_regions/
```

Each region has its own variable within each file.

We have also provided conversion tables that can be used to look up LME
and SAUP names according to the numeric codes used in the catch and
effort files (e.g. LME 22 – North Sea). These files (SAUPnames.csv and
LMEnames.csv) are also available here:

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/InputData/geo_conditions/fishmip_regions/
```

## Output data

All spatially gridded outputs should be created as netcdf files. More
information on how to prepare these files can be found
[here](https://www.isimip.org/protocol/preparing-simulation-files).
Aspatial regional model results may be saved as .csv files.

In the output files, please label the time variable as “days since
1841-1-1 00:00:00” if the output covers the spin-up and transition
period (1841-1960) or “days since 1901-1-1 00:00:00” if the output
covers the experiment period (1961-2010).

##### Table 9: Mandatory output variables for Fisheries and Marine Ecosystem models (global and regional). See notes on additional optional model outputs below. Please use the value 1.e+20 for missing data within your output files. **All biomasses are in wet weight (not g C).**

<table style="width:99%;">
<colgroup>
<col style="width: 34%" />
<col style="width: 7%" />
<col style="width: 3%" />
<col style="width: 4%" />
<col style="width: 49%" />
</colgroup>
<thead>
<tr class="header">
<th>Variable long name</th>
<th>Variable specifier</th>
<th>Unit</th>
<th>Resolution</th>
<th>Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Total Consumer Biomass Density</td>
<td><strong>tcb</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>All consumers (trophic level &gt;1, vertebrates and
invertebrates)</td>
</tr>
<tr class="even">
<td>Total Consumer Biomass Density in log10 Weight Bins</td>
<td><strong>tcblog10</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td><p><strong>Level dimensions:</strong> (time, bins, lat, lon).</p>
<p>If the model is size-structured, please provide biomass in equal log
10 g weight bins (1-10g, 10-100g, 100g-1kg, 1-10kg, 10-100kg,
&gt;100kg)</p></td>
</tr>
<tr class="odd">
<td>Total Pelagic Biomass Density</td>
<td><strong>tpb</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>All pelagic consumers (trophic level &gt;1, vertebrates and
invertebrates)</td>
</tr>
<tr class="even">
<td>Total Demersal Biomass Density</td>
<td><strong>tdb</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>All demersal consumers (trophic level &gt;1, vertebrates and
invertebrates)</td>
</tr>
<tr class="odd">
<td>Total Catch Density (all commercial functional groups / size
classes)</td>
<td><strong>tc</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea (all catch as a result of all effort including reported
and IUU) summed for both Industrial and Artisanal sector.</td>
</tr>
<tr class="even">
<td>Total Industrial Catch Density (all commercial functional groups /
size classes)</td>
<td><strong>tic</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea (all catch as a result of all effort including reported
and IUU) for Industrial sector only.</td>
</tr>
<tr class="odd">
<td>Total Catch Density in log10 Weight Bins across both sectors</td>
<td><strong>tclog10</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td><p><strong>Level dimensions:</strong> (time, bins, lat, lon).</p>
<p>If the model is size-structured, please provide biomass in equal log
10 g weight bins (1-10g, 10-100g, 100g-1kg, 1-10kg, 10-100kg,
&gt;100kg)</p></td>
</tr>
<tr class="even">
<td>Total Pelagic Density Catch across Artisanal and Industrial
sectors</td>
<td><strong>tpc</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea of all pelagic consumers (trophic level &gt;1,
vertebrates and invertebrates)</td>
</tr>
<tr class="odd">
<td>Total Demersal Catch Density across Artisanal and Industrial
sectors</td>
<td><strong>tdc</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea of all demersal consumers (trophic level &gt;1,
vertebrates and invertebrates)</td>
</tr>
<tr class="even">
<td><strong>Optional output from global and regional models. All
biomasses are in wet weight, not g C.</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>Biomass Density of Small Pelagics &lt;30cm</td>
<td><strong>bp30cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>If a pelagic species and L infinity is &lt;30 cm, include in this
variable</td>
</tr>
<tr class="even">
<td>Biomass Density of Medium Pelagics &gt;=30cm and &lt;90cm</td>
<td><strong>bp30to90cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>If a pelagic species and L infinity is &gt;=30 cm and &lt;90cm,
include in this variable</td>
</tr>
<tr class="odd">
<td>Biomass Density of Large Pelagics &gt;=90cm</td>
<td><strong>bp90cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>If a pelagic species and L infinity is &gt;=90cm, include in this
variable</td>
</tr>
<tr class="even">
<td>Biomass Density of Small Demersals &lt;30cm</td>
<td><strong>bd30cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>If a demersal species and L infinity is &lt;30 cm, include in this
variable</td>
</tr>
<tr class="odd">
<td>Biomass Density of Medium Demersals &gt;=30cm and &lt;90cm</td>
<td><strong>bd30to90cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>If a demersal species and L infinity is &gt;=30 cm and &lt;90cm,
include in this variable</td>
</tr>
<tr class="even">
<td>Biomass Density of Large Demersals &gt;=90cm</td>
<td><strong>bd90cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>If a demersal species and L infinity is &gt;=90cm, include in this
variable</td>
</tr>
<tr class="odd">
<td>Catch Density of Small Pelagics &lt;30cm</td>
<td><strong>cp30cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea of pelagic species with L infinity &lt;30 cm</td>
</tr>
<tr class="even">
<td>Catch Density of Medium Pelagics &gt;=30cm and &lt;90cm</td>
<td><strong>cp30to90cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea of pelagic species with L infinity &gt;=30 cm and
&lt;90 cm</td>
</tr>
<tr class="odd">
<td>Catch Density of Large Pelagics &gt;=90cm</td>
<td><strong>cp90cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea of pelagic species with L infinity &gt;=90 cm</td>
</tr>
<tr class="even">
<td>Catch Density of Small Demersals &lt;30cm</td>
<td><strong>cd30cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea of demersal species with L infinity &lt;30 cm</td>
</tr>
<tr class="odd">
<td>Catch Density of Medium Demersals &gt;=30cm and &lt;90cm</td>
<td><strong>cd30to90cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea of demersal species with L infinity &gt;=30 cm and
&lt;90 cm</td>
</tr>
<tr class="even">
<td>Catch Density of Large Demersals &gt;=90cm</td>
<td><strong>cd90cm</strong></td>
<td>g m-2</td>
<td><p>0.25° grid</p>
<p>monthly</p></td>
<td>Catch at sea of demersal species with L infinity &gt;=90 cm</td>
</tr>
</tbody>
</table>

## Additional notes for Regional FishMIP Models

More specific protocols for each regional model type will be developed
through our monthly online regional modeller sessions. Please contact
regional FishMIP coordinators for more information.

As a first step, regional modellers will need to provide shapefiles for
their respective model domains for us to help with spatial extraction of
the above global climate and fishing effort forcing inputs.

Region-specific climate forcing variables will be made available here:

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/InputData/climate/ocean/<obsclim> or <ctrlclim>/regional/
```

A .csv file with fishing effort extracted for regional model ecosystems
is also available in the same folder as the global fishing effort data
(`../fishing/histsoc`), for regional models that have provided
shapefiles.

Regional modellers may wish to make their raw unaggregated output
available for more detailed analyses, including for example, a wider
range of functional groups/size classes/species and ecosystem
indicators. Please discuss this with FishMIP regional coordinators
before uploading files.

## Reporting model results

The specification on how to submit the data, as well as further
information and instructions are given on the ISIMIP website at:

<https://www.isimip.org/protocol/preparing-simulation-files>

**It is important that you comply precisely with the formatting
specified there**, to facilitate the analysis of your simulation results
in the ISIMIP framework. Incorrect formatting can seriously delay
analyses. The ISIMIP Team will be glad to assist with the preparation of
these files if necessary.

File names consist of a series of identifier, separated by underscores.
Things to note:

- Report one variable per file.

- In filenames, use lowercase letters only.

- Use underscore (\_) to separate identifiers.

- Variable names consist of a single word without hyphens or
  underscores.

- Use hyphens (-) to separate strings within an identifier, e.g. in a
  model name.

- Data model is NETCDF4_CLASSIC with minimum compression level of 5.

- NetCDF file extension is .nc.

- The relative time axis’ reference date is days since 1841-1-1 00:00:00
  if the output covers the spin-up and transition period (1841-1960) or
  days since 1901-1-1 00:00:00 if the output covers the experiment
  period (1961-2010). We have provided .csv files to be used for the
  time dimension in creating NetCDF files based on the 365 days
  calendar. Please see time_axix_spinup.csv and time_axis_experiment.csv
  in this repository. The script time_axis.r was used to create these
  files.

### Name pattern of output files:

Please name the files in the Fisheries and Marine Ecosystems sector
according to the following pattern:

**Global models**

``` linux
<model>_<climate-forcing>_<bias-adjustment>_<climate-scenario>_<soc-scenario>_<sens-scenario>_<variable>_<global>_<time-step>_<start-year>_<end-year>.nc
```

Example:

``` linux
boats_gfdl-mom6_cobalt2_none_obsclim_histsoc_default_tcb_global_monthly_1961_2010.nc
```

**Regional models**

``` linux
<model>_<climate-forcing>_<bias-adjustment>_<climate-scenario>_<soc-scenario>_<sens-scenario>_<variable>_<region>_<time-step>_<start-year>_<end-year>.nc
```

Example:

``` linux
osmose_gfdl-mom6_cobalt2_none_obsclim_histsoc_default_tcb_benguela_monthly_1961_2010.nc
```

Please see the climate-scenario, soc-scenario, sens-scenario and
variable identifiers given in the tables of this document.

### Path to outut files on DKRZ:

**Global models**

The output files covering the spin-up period (1841-1960) can be saved on
DKRZ here:

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/UploadArea/marine-fishery_global/model_name/temp2
```

The output files covering the experiment period (1961-2010) can be saved
on DKRZ here

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/UploadArea/marine-fishery_global/model_name/temp
```

**Regional models**

The output files covering the spin-up period (1841-1960) can be saved on
DKRZ here:

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/UploadArea/marine-fishery_regional/model_name/temp2
```

The output files covering the experiment period (1961-2010) can be saved
on DKRZ here

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/UploadArea/marine-fishery_regional/model_name/temp
```

Please contact FishMIP coordinators or ISIMIP data managers directly
([isimip-data@pik‐potsdam.de](mailto:isimip-data@pik%E2%80%90potsdam.de))
if you have any questions or clarifications before submitting files or
if you do not find your model’s path on DKRZ as described above.

**Please contact FishMIP coordinators** if you would like to participate
in this simulation round but have encountered issues with any aspect of
the protocol.

(For fishing): please provide all assumptions about catchability,
technological creep, and model calibration.

Please provide any conversion factors that you have used to convert
units.

### **Thank you for your contributions to FishMIP and ISI-MIP!**

FishMIP is entirely community-driven, and we appreciate the effort of
all involved.
