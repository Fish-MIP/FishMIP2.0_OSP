
# FishMIP_2023_3b_Protocol

### <u>Contents</u>

[Goal \[2\]](#goal)

[Experiments & Scenarios \[3\]](#experiments-scenarios)

[Input data \[6\]](#input-data)

[Climate forcing \[6\]](#climate-forcing)

[Fishing effort forcing \[11\]](#fishing-effort-forcing)

[Output data \[14\]](#output-data)

[Additional notes for Regional FishMIP Models
\[16\]](#additional-notes-for-regional-fishmip-models)

[Reporting model results \[16\]](#reporting-model-results)

## 

## Goal

The goal of the FishMIP “Ocean Futures” Protocol is to extend 3b CMIP
climate projections to include:

2)  exploring fishing impacts in addition to those of climate, including
    future projections with fishing under a range of socio-economic
    scenarios (aligned with SSPs, Maury et al. IN PREP);

3)  comparison to a no-climate change preindustrial control baseline
    (which was not available for the last round of simulations), and

4)  if possible, building on the 3a model evaluation simulation round,
    model benchmarking against observed catches.

Note that this FishMIP Phase 2 protocol builds on the Phase 1 2020
protocol which focussed primarily on results without fishing for
inclusion in the IPCC 5th Assessment.

Modellers are welcome to redo all previous 3b runs with version of their
models that have had improvmets following the 3a model evaluation round.

Timelines for simulations

| Scenarios          | Models           | Date          |
|--------------------|------------------|---------------|
| histsoc,soc_2015   | global, regional | July 1st 2024 |
| soc_OSP1, soc_OSP2 | global, regional | Oct 1st, 2024 |

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

Further information on this protocol can be found here:

[https://protocol.isimip.org/#ISIMIP3b/marine-fishery_regional/marine-fishery_global](https://protocol.isimip.org/)

**For this simulation round, we are asking you to run XXXXXXXX**

## Experiments & Scenarios

Each model experiment is a set of model simulations that has a
particular goal (e.g. model evaluation). A scenario is a particular
setting for forcing drivers that describes how each model run should be
set up in the experiment, including both the type of climate forcing
(CF) and the type of direct human forcing (DHF).

**Below we summarise the simulation experiments for both Phase 1 and
Phase 2 of the 3b simulation round. Modellers that have already
completed Phase 1 can skip to Phase 2. below. Please prioritize the core
runs below, and provide the ‘optional’ if possible.**

##### Table 1: Experiment set-up. Each experiment is specified by the climate forcing (CF) and Direct Human Forcing (DHF).

<table style="width:98%;">
<colgroup>
<col style="width: 3%" />
<col style="width: 19%" />
<col style="width: 47%" />
<col style="width: 14%" />
<col style="width: 13%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Experiment</th>
<th>Short description</th>
<th>Historical</th>
<th>Future</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td><p><strong>Pre-industrial control</strong></p>
<p>nat</p></td>
<td><p><strong>Climate</strong>: No climate change, fixed 1850s
CO<sub><code>2</code></sub> levels</p>
<p><strong>F ishing</strong>: No fishing</p></td>
<td><p>picontrol</p>
<p>nat</p></td>
<td><p>picontrol</p>
<p>nat</p></td>
</tr>
<tr class="even">
<td>2</td>
<td><p><strong>Pr e-i ndustrial control</strong></p>
<p>histsoc</p></td>
<td><p><strong>C limate</strong>: No climate change, fixed 1850s
CO<sub><code>2</code></sub> levels</p>
<p><strong>F ishing</strong>: H istorical fishing effort, then future
fixed at 2015 levels</p></td>
<td><p>picontrol</p>
<p>histsoc</p></td>
<td><p>picontrol</p>
<p>2015soc</p></td>
</tr>
<tr class="odd">
<td>3</td>
<td><p><strong>S SP1 -RCP2.6</strong></p>
<p>nat</p></td>
<td><p><strong>C limate</strong>: Simulated historical climate, then SS
P1-RCP2.6 climate</p>
<p><strong>Fis hing</strong>:No fishing</p></td>
<td><p>h istorical</p>
<p>nat</p></td>
<td><p>ssp126</p>
<p>nat</p></td>
</tr>
<tr class="even">
<td>4</td>
<td><p><strong>SSP1 -RCP2.6</strong></p>
<p>histsoc</p></td>
<td><p><strong>Climate</strong>: Simulated h istorical climate, then SS
P1-RCP2.6 climate</p>
<p><strong>F ishing</strong>: H istorical fishing effort, then future
fixed at 2015 levels</p></td>
<td><p>h istorical</p>
<p>histsoc</p></td>
<td><p>ssp126</p>
<p>2015soc</p></td>
</tr>
<tr class="odd">
<td>5</td>
<td><p><strong>S SP1 -RCP2.6</strong></p>
<p>OSP1</p></td>
<td><p><strong>C limate</strong>: Simulated h istorical climate, then SS
P1-RCP2.6 climate</p>
<p><strong>F ishing</strong>: H istorical fishing effort, then change
driven by OSP1</p></td>
<td><p>h istorical</p>
<p>histsoc</p></td>
<td><p>ssp126</p>
<p>OSP1soc</p></td>
</tr>
<tr class="even">
<td>6</td>
<td><p><strong>S SP5 -RCP8.5</strong></p>
<p>nat</p></td>
<td><p><strong>C limate</strong>: Simulated h istorical climate, then SS
P5-RCP2.6 climate</p>
<p><strong>F ishing</strong>: No fishing</p></td>
<td><p>h istorical</p>
<p>nat</p></td>
<td><p>ssp585</p>
<p>nat</p></td>
</tr>
<tr class="odd">
<td>7</td>
<td><p><strong>S SP5 -RCP8.5</strong></p>
<p>histsoc</p></td>
<td><p><strong>C limate</strong>: Simulated h istorical climate, then SS
P5-RCP8.5 climate</p>
<p><strong>F ishing</strong>: H istorical fishing effort, then held
fixed at 2015 levels</p></td>
<td><p>h istorical</p>
<p>histsoc</p></td>
<td><p>ssp585</p>
<p>2015soc</p></td>
</tr>
<tr class="even">
<td>8</td>
<td><p><strong>S SP5 -RCP8.5</strong></p>
<p>OSP2soc?</p></td>
<td><p><strong>C limate</strong>: Simulated h istorical climate, then SS
P5-RCP8.5 climate</p>
<p><strong>F ishing</strong>: H istorical fishing effort, then change
driven by OSP2</p></td>
<td><p>h istorical</p>
<p>histsoc</p></td>
<td><p>ssp585</p>
<p>OSP2soc</p></td>
</tr>
</tbody>
</table>

#### Note on spin-up and transition period (1841-1960), and historical (experiment) period 1961-2010

The focal historical period for this model evaluation experiment spans
1961-2010. To capture the transition from a pre-industrial spin-up to
1961 we also provide input for a gradual increase in fishing and
environmental variability for the pre-industrial period to 1961.  
  
For fishing effort prior to 1961, we provide input for a nominal spin-up
(1841-1860, fishing held constant at 1861 levels) and pre-industrial
transition period (1861-1960, reconstructed fishing effort).  
  
To set-up climate-forcing variables for the entire 1841-1960 period, we
ask modellers to use the “control run” (ctrlclim) monthly output for the
years 1961-1980 (inclusive) on repeat for six cycles. These years have
been selected because they correspond with an entire ENSO cycle and
because no climate trend is detectable prior to 1980 from the GFDL
model.  
  
For models that require longer spin-up prior to 1841, please keep 1841
levels of fishing effort constant and, if needed, repeat the ENSO cycle
(e.g. monthly values for 1961-1980 inclusive from ctrlclim) for as many
times necessary.  
  
For the ‘no fishing’ runs (nat), the spin-up and pre-industrial
transition should not use any fishing effort.  
  
We ask modellers to include all outputs from 1841 onwards for use in our
evaluation assessment of model drift. Each output should be saved as two
files, the first covering the spin-up and transition period (1841-1960)
and the second covering the histirical (experiment) period (1961-2010).

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

##### Table 2: Climate scenario specifiers (climate-scenario).

| **Scenario specifier** | **Description**                                                       |
|:-----------------------|:----------------------------------------------------------------------|
| picontrol              | Pre-industrial climate as simulated by the Earth System Models (ESMs) |
| historical             | Historical climate as simulated by the ESMs, starting in 1950.        |
| ssp126                 | SSP1-RCP2.6 climate as simulated by the ESMs                          |
| ssp585                 | SSP5-RCP8.5 climate as simulated by the ESMs.                         |
| sspXXX                 | ANY OTHERS?                                                           |

##### Table 3: Socio-economic scenario specifiers (soc-scenario).

| **Scenario specifier** | **Description**                                                                                                     |
|:-----------------------|:--------------------------------------------------------------------------------------------------------------------|
| **histsoc**            | Varying direct human influences in the historical period (1850-2014) (i.e. historical estimates of fishing effort). |
| **2015soc**            | Fixed year-2015 direct human influences (i.e. fishing effort).                                                      |
| OSPX                   | Future fishing determined by SSP and OSP driver forcings for OSPX                                                   |
| OSPX                   | Future fishing determined by SSP and OSP driver forcings for OSPX                                                   |
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
<col style="width: 52%" />
<col style="width: 13%" />
<col style="width: 9%" />
<col style="width: 12%" />
<col style="width: 10%" />
</colgroup>
<thead>
<tr class="header">
<th>Variable</th>
<th>Sp ecifier</th>
<th>Unit</th>
<th>Res olution</th>
<th>ESM datasets</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mass Con centration of Total Phy toplankton Expressed as C
hlorophyll</td>
<td><strong>chl</strong></td>
<td>kg m-3</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Sea Floor Depth</td>
<td><ul>
<li>* deptho**</li>
</ul></td>
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
<td><ul>
<li>* intpoc**</li>
</ul></td>
<td>kg m-2</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Primary Organic Carbon Production by All Types of Phy
toplankton</td>
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
<td>Net Primary Mole Pr oductivity of Carbon by D iazotrophs</td>
<td><strong>intp pdiaz</strong></td>
<td>mol m-2 s-1</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Net Primary Mole Pr oductivity of Carbon by Pico phy toplankton</td>
<td><strong>intp ppico</strong></td>
<td>mol m-2 s-1</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Maximum Ocean Mixed Layer Thickness Defined by Sigma T</td>
<td><ul>
<li>*mlotst</li>
</ul>
<p>-0125**</p></td>
<td><p>m</p>
<p>m</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Dissolved Oxygen Con centration</td>
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
<p><strong>p h-bot</strong></p>
<p><strong>ph -surf</strong></p></td>
<td><p>1</p>
<p>1</p>
<p>1</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Phy toplankton Carbon Con centration</td>
<td><ul>
<li><br />
</li>
</ul>
<p>*phyc**</p>
<p><strong>phyc -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Mole Con centration of Diatoms expressed as Carbon in sea water</td>
<td><p><strong>ph ydiat</strong></p>
<p><strong>phydiat -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Mole Con centration of D iazotrophs Expressed as Carbon in Sea
Water</td>
<td><p><strong>ph ydiaz</strong></p>
<p><strong>phydiaz -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Mole Con centration of Pico phy toplankton Expressed as Carbon in
Sea Water</td>
<td><p><strong>ph ypico</strong></p>
<p><strong>phypico -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Sea Water Salinity</td>
<td><p><strong>so</strong></p>
<p><strong>s o-bot</strong></p>
<p><strong>so -surf</strong></p></td>
<td><p>‰</p>
<p>‰<br />
‰</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Sea Water Potential T emperature</td>
<td><strong>t hetao</strong></td>
<td>°C</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Ocean Model Cell Thickness</td>
<td><strong>thk cello</strong></td>
<td>m</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Sea Water Potential T emperature at Sea Floor</td>
<td><strong>tob</strong></td>
<td>°C</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Sea Surface T emperature</td>
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
<td>Mole Con centration of Me soz ooplankton expressed as Carbon in sea
water</td>
<td><p><strong>zmeso</strong></p>
<p><strong>zmeso -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Mole Con centration of Mic roz ooplankton expressed as Carbon in sea
water</td>
<td><p><strong>z micro</strong></p>
<ul>
<li>*zmicro</li>
</ul>
<p>-vint**</p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Z ooplankton Carbon Con centration</td>
<td><ul>
<li><br />
</li>
</ul>
<p>*zooc**</p>
<p><strong>zooc -vint</strong></p></td>
<td><p>mol m-3</p>
<p>mol m-2</p></td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="even">
<td>Net Downward Shortwave Radiation at Sea Water Surface</td>
<td><strong>r sntds</strong></td>
<td>W m-2</td>
<td>0.25° , 1° grid</td>
<td>GFDL, IPSL</td>
</tr>
<tr class="odd">
<td>Sea Ice Area Fraction</td>
<td><strong>s iconc</strong></td>
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

##### Table 7: Fishing effort forcing files and variables for FishMIP 3b simulations.

<table style="width:99%;">
<colgroup>
<col style="width: 12%" />
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 7%" />
</colgroup>
<thead>
<tr class="header">
<th>Specifier</th>
<th>Included variables (short names) and definitions</th>
<th>Time pe riod /Resolution</th>
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
<td>H istorical P opulation</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>H istorical GDP</td>
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
<td>SSP1 P opulation</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>SSP1 GDP</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>SSP5 P opulation</td>
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

| Va riable Name      | Long name                                                                                     | Unit             | Description/notes                                                                                                                                                                                                                                                                                          |
|:--------------------|:----------------------------------------------------------------------------------------------|:-----------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Year                | (End of the) year when the f ishing effort is occ urring                                      | Number code      |                                                                                                                                                                                                                                                                                                            |
| Sector              | The f ishing sector d efined by the law of the c ountry                                       | Name code        | I = Industrial and A = artisanal, where artisanal include powered and unpowered artisanal fleets                                                                                                                                                                                                           |
| LME                 | Large Marine Eco system Number                                                                | Number code      | A number code of the Large Marine ecosystem in which the Effort is occurring                                                                                                                                                                                                                               |
| eez\_ countr y_name | Exc lusive Ec onomic Zone                                                                     | Name code        | The country-level exclusive economic zone (or high seas) name in which fishing effort is occurring                                                                                                                                                                                                         |
| SAUP                | A number code for the f ishing co untry, fol lowing Sea Around Us num bering                  | Number code      | Ex supranational entities (USSR, Yugoslavia) are disaggregated to their constituent countries. Serbian Fishing Effort included with Montenegro. Crimea included with Ukrainian.                                                                                                                            |
| Gear                | The f ishing gear                                                                             | Name code        | Gear names                                                                                                                                                                                                                                                                                                 |
| FGroup              | The ta rgeted func tional group                                                               | Name code        | Functional groups are in accordance with those used by the Sea Around Us Project                                                                                                                                                                                                                           |
| Nom Active          | N ominal f ishing effort (i.e., not inc luding the t echnol ogical creep) of the active fleet | Days at sea X kW | NomActive (of the active fleet; i.e., total) = P (engine power of active the fleet; i.e., total) x DAS (average days at sea of one vessel). Average DAS for one vessel \~ 200 DAS/year. NomActive corresponds to the total (reported, IUU, discards) catch. To find NomActive in DAS do (NomActive/P) X NV |

##### Table 9: Details for OSP relative change in drivers of fishing effort variables.

| OSP  | Variable | Change relative to 2015 |
|------|----------|-------------------------|
| OSP1 | ????     | ????                    |
| OSP2 | ????     | ????                    |

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
