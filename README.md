---
editor_options: 
  markdown: 
    wrap: 72
---

# FishMIP_2023_3b_Protocol

### <u>Contents</u>

[Goal $$2$$](#goal)

[Experiments & Scenarios $$3$$](#experiments-scenarios)

[Input data $$6$$](#input-data)

[Climate forcing $$6$$](#climate-forcing)

[Fishing effort forcing $$11$$](#fishing-effort-forcing)

[Output data $$14$$](#output-data)

[Additional notes for Regional FishMIP Models
$$16$$](#additional-notes-for-regional-fishmip-models)

[Reporting model results $$16$$](#reporting-model-results)

## 

## Goal {#goal}

The goal of the FishMIP "Ocean Futures" Protocol is to extend 3b CMIP
climate projections to include:

2)  exploring fishing impacts in addition to those of climate, including
    future projections with fishing under a range of socio-economic
    scenarios (aligned with SSPs, Maury et al. IN PREP);

3)  comparison to a no-climate change preindustrial control baseline
    (which was not available for the last round of simulations), and

4)  if possible, building on the 3a model evaluation simulation round,
    model benchmarking against observed catches.

Note that this FishMIP Phase 2 CMIP6 protocol builds on the Phase 1
CMIP6 protocol which began in 2020 and focussed primarily on results
without fishing for inclusion in the IPCC 6th Assessment.

Modellers are welcome to redo all previous 3b runs that have had
improvements following the 3a model evaluation round, also long as the
version of their model outputs are all appropriately annotated.

Timelines for simulations

| Scenarios        | Models           | Date          |
|------------------|------------------|---------------|
| histsoc, 2015soc | global, regional | July 1st 2024 |
| OSP1soc, OSP2soc | global, regional | Oct 1st, 2024 |

To aid with progress we will hold specific technical workshops to:

-   Ensure correct OSP integration inputs and access

-   Ensure fishing drivers work (separate global and regional breakaway
    groups)

-   Tool sharing & troubleshooting

-   Check model outputs/issues

In this document we describe the general experimental and scenario
set-up (Section 3). Further down in Section 4 we include the details of
the specific **input** variables that modellers can use to implement
scenarios. In Section 5 we describe the set of **outputs** to be
created. Finally in Sections 6-7 we provide further **notes** and
**instructions** on how to report and upload model results.

Further information on this protocol can be found here:

[https://protocol.isimip.org/#ISIMIP3b/marine-fishery_regional/marine-fishery_global](https://protocol.isimip.org/)

**For this simulation round, we are asking you to run XXXXXXXX**

## Experiments & Scenarios {#experiments-scenarios}

Each model experiment is a set of model simulations that has a
particular goal (e.g. combined fishing and climate scenario
projections). A scenario is a particular setting for forcing drivers
that describes how each model run should be set up in the experiment,
including both the type of climate forcing (CF) and the type of direct
human forcing (DHF).

**Below we summarise the simulation experiments for both Phase 1 and
Phase 2 of the 3b simulation round. Modellers that have already
completed Phase 1 can skip to Phase 2. below. Please prioritize the core
runs below, and provide the 'optional' if possible.**

##### Table 1: Experiment set-up. Each experiment is specified by the climate forcing (CF) and Direct Human Forcing (DHF).

+---+--------------+-----------------+-----------+------------+
|   | Experiment   | Short           | H         | Future     |
|   |              | description     | istorical |            |
+===+==============+=================+===========+============+
| 1 | **Pr         | **Climate**: No | picontrol | picontrol  |
|   | e-industrial | climate change, |           |            |
|   | control**    | fixed 1850s     | nat       | nat        |
|   |              | CO~`2`~ levels  |           |            |
|   | nat          |                 |           |            |
|   |              | **Fishing**: No |           |            |
|   |              | fishing         |           |            |
+---+--------------+-----------------+-----------+------------+
| 2 | **Pr         | **Climate**: No | picontrol | picontrol  |
|   | e-industrial | climate change, |           |            |
|   | control**    | fixed 1850s     | histsoc   | 2015soc    |
|   |              | CO~`2`~ levels  |           |            |
|   | histsoc      |                 |           |            |
|   |              | **Fishing**:    |           |            |
|   |              | Historical      |           |            |
|   |              | fishing effort, |           |            |
|   |              | then future     |           |            |
|   |              | fixed at 2015   |           |            |
|   |              | levels          |           |            |
+---+--------------+-----------------+-----------+------------+
| 3 | **S          | **Climate**:    | h         | ssp126     |
|   | SP1-RCP2.6** | Simulated       | istorical |            |
|   |              | historical      |           | nat        |
|   | nat          | climate, then   | nat       |            |
|   |              | SSP1-RCP2.6     |           |            |
|   |              | climate         |           |            |
|   |              |                 |           |            |
|   |              | **Fishing**:No  |           |            |
|   |              | fishing         |           |            |
+---+--------------+-----------------+-----------+------------+
| 4 | **S          | **Climate**:    | h         | ssp126     |
|   | SP1-RCP2.6** | Simulated       | istorical |            |
|   |              | historical      |           | 2015soc    |
|   | histsoc      | climate, then   | histsoc   |            |
|   |              | SSP1-RCP2.6     |           |            |
|   |              | climate         |           |            |
|   |              |                 |           |            |
|   |              | **Fishing**:    |           |            |
|   |              | Historical      |           |            |
|   |              | fishing effort, |           |            |
|   |              | then future     |           |            |
|   |              | fixed at 2015   |           |            |
|   |              | levels          |           |            |
+---+--------------+-----------------+-----------+------------+
| 5 | **S          | **Climate**:    | h         | ssp126     |
|   | SP1-RCP2.6** | Simulated       | istorical |            |
|   |              | historical      |           | OSP1soc    |
|   | OSP1         | climate, then   | histsoc   |            |
|   |              | SSP1-RCP2.6     |           |            |
|   |              | climate         |           |            |
|   |              |                 |           |            |
|   |              | **Fishing**:    |           |            |
|   |              | Historical      |           |            |
|   |              | fishing effort, |           |            |
|   |              | then change     |           |            |
|   |              | driven by OSP1  |           |            |
+---+--------------+-----------------+-----------+------------+
| 6 | **S          | **Climate**:    | h         | ssp585     |
|   | SP5-RCP8.5** | Simulated       | istorical |            |
|   |              | historical      |           | nat        |
|   | nat          | climate, then   | nat       |            |
|   |              | SSP5-RCP2.6     |           |            |
|   |              | climate         |           |            |
|   |              |                 |           |            |
|   |              | **Fishing**: No |           |            |
|   |              | fishing         |           |            |
+---+--------------+-----------------+-----------+------------+
| 7 | **S          | **Climate**:    | h         | ssp585     |
|   | SP5-RCP8.5** | Simulated       | istorical |            |
|   |              | historical      |           | 2015soc    |
|   | histsoc      | climate, then   | histsoc   |            |
|   |              | SSP5-RCP8.5     |           |            |
|   |              | climate         |           |            |
|   |              |                 |           |            |
|   |              | **Fishing**:    |           |            |
|   |              | Historical      |           |            |
|   |              | fishing effort, |           |            |
|   |              | then held fixed |           |            |
|   |              | at 2015 levels  |           |            |
+---+--------------+-----------------+-----------+------------+
| 8 | **S          | **Climate**:    | h         | ssp585     |
|   | SP5-RCP8.5** | Simulated       | istorical |            |
|   |              | historical      |           | OSP2soc    |
|   | OSP2soc?     | climate, then   | histsoc   |            |
|   |              | SSP5-RCP8.5     |           |            |
|   |              | climate         |           |            |
|   |              |                 |           |            |
|   |              | **Fishing**:    |           |            |
|   |              | Historical      |           |            |
|   |              | fishing effort, |           |            |
|   |              | then change     |           |            |
|   |              | driven by OSP2  |           |            |
+---+--------------+-----------------+-----------+------------+

#### NEEDS UPDATE: Note on spin-up and transition period (1841-1960), and historical (experiment) period 1961-2010

The focal historical period for this model evaluation experiment spans
1961-2010. To capture the transition from a pre-industrial spin-up to
1961 we also provide input for a gradual increase in fishing and
environmental variability for the pre-industrial period to 1961.

For fishing effort prior to 1961, we provide input for a nominal spin-up
(1841-1860, fishing held constant at 1861 levels) and pre-industrial
transition period (1861-1960, reconstructed fishing effort).

To set-up climate-forcing variables for the entire 1841-1960 period, we
ask modellers to use the "control run" (ctrlclim) monthly output for the
years 1961-1980 (inclusive) on repeat for six cycles. These years have
been selected because they correspond with an entire ENSO cycle and
because no climate trend is detectable prior to 1980 from the GFDL
model.

For models that require longer spin-up prior to 1841, please keep 1841
levels of fishing effort constant and, if needed, repeat the ENSO cycle
(e.g. monthly values for 1961-1980 inclusive from ctrlclim) for as many
times necessary.

For the 'no fishing' runs (nat), the spin-up and pre-industrial
transition should not use any fishing effort.

We ask modellers to include all outputs from 1841 onwards for use in our
evaluation assessment of model drift. Each output should be saved as two
files, the first covering the spin-up and transition period (1841-1960)
and the second covering the histirical (experiment) period (1961-2010).

#### Scenario definitions

Throughout the protocol we use 'specifiers' that are shortened names
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

+-----------------+----------------------------------------------------+
| **Scenario      | **Description**                                    |
| specifier**     |                                                    |
+:================+:===================================================+
| picontrol       | Pre-industrial climate as simulated by the Earth   |
|                 | System Models (ESMs)                               |
+-----------------+----------------------------------------------------+
| historical      | Historical climate as simulated by the ESMs,       |
|                 | starting in 1950.                                  |
+-----------------+----------------------------------------------------+
| ssp126          | SSP1-RCP2.6 climate as simulated by the ESMs       |
+-----------------+----------------------------------------------------+
| ssp585          | SSP5-RCP8.5 climate as simulated by the ESMs.      |
+-----------------+----------------------------------------------------+
| sspXXX          | ANY OTHERS?                                        |
+-----------------+----------------------------------------------------+

##### Table 3: Socio-economic scenario specifiers (soc-scenario).

+---------------+-----------------------------------------------------+
| **Scenario    | **Description**                                     |
| specifier**   |                                                     |
+:==============+:====================================================+
| **histsoc**   | Varying direct human influences in the historical   |
|               | period (1850-2014) (i.e. historical estimates of    |
|               | fishing effort).                                    |
+---------------+-----------------------------------------------------+
| **2015soc**   | Fixed year-2015 direct human influences             |
|               | (i.e. fishing effort).                              |
+---------------+-----------------------------------------------------+
| **OSPXsoc**   | Future fishing determined by SSP1 and OSP driver    |
|               | forcings for OSPX                                   |
+---------------+-----------------------------------------------------+
| **OSPXsoc**   | Future fishing determined by SSP5 and OSP driver    |
|               | forcings for OSPX                                   |
+---------------+-----------------------------------------------------+
| **nat**       | No fishing (naturalized run).                       |
+---------------+-----------------------------------------------------+

**Please remember to use these same specifiers in your output files.
More on reporting data can be found at the end of this document.**

## Input data {#input-data}

**For modellers new to FishMIP:** to access all input data you first
need to set up an account with ISIMIP to access the DKRZ server. Please
follow the instructions here:
<https://www.isimip.org/dashboard/accessing-isimip-data-dkrz-server/>

### Climate forcing {#climate-forcing}

##### Table 5: Climate forcing

+----------+----------+----------------------------------+----------+
| Title    | Spec     | Institution                      | Or       |
|          | ifiers   |                                  | iginal   |
|          |          |                                  | reso     |
|          |          |                                  | lution   |
+:=========+:=========+:=================================+:=========+
| GF       | gf       | National Oceanic and Atmospheric | 2 88x180 |
| DLESM4   | dlesm4   | Administration, Geophysical      |          |
|          |          | Fluid Dynamics Laboratory,       |          |
|          |          | Princeton, NJ 08540, USA         |          |
+----------+----------+----------------------------------+----------+
| IPSL     | ipslc    | Institut Pierre Simon Laplace,   | 1 44x143 |
| CM6ALR   | m6a-lr   | Paris 75252, France              |          |
+----------+----------+----------------------------------+----------+
| OT       |          |                                  |          |
| HERS??   |          |                                  |          |
+----------+----------+----------------------------------+----------+

MATTHIAS/CHERYL:CROSS CHECK WHAT WE HAVE Vs WHAT IS BELOW

##### Table 6. Climate forcing variables and units for FishMIP 3a simulations. All variables are available on a 0.25 and 1 degree horizontal grid, monthly and annual resolutions. Note: Some variables are available as specific layers extracted from vertically resolved data. Their variable names have been suffixed with -bot (ocean bottom, e.g. o2-bot), -surf (surface values, e.g. pH-surf) or -vint (vertically integrated, e.g. phyc-vint), respectively, or prefixed with int (vertically integrated, e.g. intpp). Temperature is suffixed with b or s for bottom (e.g. tob) or surface (e.g. tos) layers, respectively.

+---------------+-----------+-----------+---------------+-----------+
| Variable      | Sp        | Unit      | Res olution   | ESM       |
|               | ecifier   |           |               | datasets  |
+===============+===========+===========+===============+===========+
| Mass          | **chl**   | kg m-3    | 0.25° , 1°    | GFDL,     |
| Concentration |           |           | grid          | IPSL      |
| of Total      |           |           |               |           |
| Phytoplankton |           |           |               |           |
| Expressed as  |           |           |               |           |
| Chlorophyll   |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Sea Floor     | *         | m         | 0.25° , 1°    | GFDL,     |
| Depth         | *deptho** |           | grid          | IPSL      |
+---------------+-----------+-----------+---------------+-----------+
| Downward Flux | **exp     | mol m-2   | 0.25° , 1°    | GFDL,     |
| of            | c-bot**   | s-1       | grid          | IPSL      |
| Particulate   |           |           |               |           |
| Organic       |           |           |               |           |
| Carbon        |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Particulate   | *         | kg m-2    | 0.25° , 1°    | GFDL,     |
| Organic       | *intpoc** |           | grid          | IPSL      |
| Carbon        |           |           |               |           |
| Content       |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Primary       |           | mol m-2   | 0.25° , 1°    | GFDL,     |
| Organic       | **intpp** | s-1       | grid          | IPSL      |
| Carbon        |           |           |               |           |
| Production by |           |           |               |           |
| All Types of  |           |           |               |           |
| Phytoplankton |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Net Primary   | **intp    | mol m-2   | 0.25° , 1°    | GFDL,     |
| Organic       | pdiat**   | s-1       | grid          | IPSL      |
| Carbon        |           |           |               |           |
| Production by |           |           |               |           |
| Diatoms       |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Net Primary   | **intp    | mol m-2   | 0.25° , 1°    | GFDL,     |
| Mole          | pdiaz**   | s-1       | grid          | IPSL      |
| Productivity  |           |           |               |           |
| of Carbon by  |           |           |               |           |
| Diazotrophs   |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Net Primary   | **intp    | mol m-2   | 0.25° , 1°    | GFDL,     |
| Mole          | ppico**   | s-1       | grid          | IPSL      |
| Productivity  |           |           |               |           |
| of Carbon by  |           |           |               |           |
| Pico          |           |           |               |           |
| phytoplankton |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Maximum Ocean | -         | m         | 0.25° , 1°    | GFDL,     |
| Mixed Layer   |  \*mlotst |           | grid          | IPSL      |
| Thickness     |           | m         |               |           |
| Defined by    | -0125\*\* |           |               |           |
| Sigma T       |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Dissolved     | **o2,**   | mol m-3   | 0.25° , 1°    | GFDL,     |
| Oxygen        |           |           | grid          | IPSL      |
| Concentration | **o       | mol m-2   |               |           |
|               | 2-bot**   |           |               |           |
|               |           | mol m-2   |               |           |
|               | **o2      |           |               |           |
|               | -surf**   |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| pH            | **ph**    | 1         | 0.25° , 1°    | GFDL,     |
|               |           |           | grid          | IPSL      |
|               | **p       | 1         |               |           |
|               | h-bot**   |           |               |           |
|               |           | 1         |               |           |
|               | **ph      |           |               |           |
|               | -surf**   |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Phytoplankton | -   \     | mol m-3   | 0.25° , 1°    | GFDL,     |
| Carbon        | *phyc\*\* |           | grid          | IPSL      |
| Concentration |           | mol m-2   |               |           |
|               | **phyc    |           |               |           |
|               | -vint**   |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Mole          | **ph      | mol m-3   | 0.25° , 1°    | GFDL,     |
| Concentration | ydiat**   |           | grid          | IPSL      |
| of Diatoms    |           | mol m-2   |               |           |
| expressed as  | **phydiat |           |               |           |
| Carbon in sea | -vint**   |           |               |           |
| water         |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Mole          | **ph      | mol m-3   | 0.25° , 1°    | GFDL,     |
| Concentration | ydiaz**   |           | grid          | IPSL      |
| of            |           | mol m-2   |               |           |
| Diazotrophs   | **phydiaz |           |               |           |
| Expressed as  | -vint**   |           |               |           |
| Carbon in Sea |           |           |               |           |
| Water         |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Mole          | **ph      | mol m-3   | 0.25° , 1°    | GFDL,     |
| Concentration | ypico**   |           | grid          | IPSL      |
| of            |           | mol m-2   |               |           |
| Pico          | **phypico |           |               |           |
| phytoplankton | -vint**   |           |               |           |
| Expressed as  |           |           |               |           |
| Carbon in Sea |           |           |               |           |
| Water         |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Sea Water     | **so**    | ‰         | 0.25° , 1°    | GFDL,     |
| Salinity      |           |           | grid          | IPSL      |
|               | **s       | ‰\        |               |           |
|               | o-bot**   | ‰         |               |           |
|               |           |           |               |           |
|               | **so      |           |               |           |
|               | -surf**   |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Sea Water     | **t       | °C        | 0.25° , 1°    | GFDL,     |
| Potential     | hetao**   |           | grid          | IPSL      |
| Temperature   |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Ocean Model   | **thk     | m         | 0.25° , 1°    | GFDL,     |
| Cell          | cello**   |           | grid          | IPSL      |
| Thickness     |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Sea Water     | **tob**   | °C        | 0.25° , 1°    | GFDL,     |
| Potential     |           |           | grid          | IPSL      |
| Temperature   |           |           |               |           |
| at Sea Floor  |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Sea Surface   | **tos**   | °C        | 0.25° , 1°    | GFDL,     |
| Temperature   |           |           | grid          | IPSL      |
+---------------+-----------+-----------+---------------+-----------+
| Sea Water X   | **uo**    | m s-1     | 0.25° , 1°    | GFDL,     |
| Velocity      |           |           | grid          | IPSL      |
+---------------+-----------+-----------+---------------+-----------+
| Sea Water Y   | **vo**    | m s-1     | 0.25° , 1°    | GFDL,     |
| Velocity      |           |           | grid          | IPSL      |
+---------------+-----------+-----------+---------------+-----------+
| Mole          |           | mol m-3   | 0.25° , 1°    | GFDL,     |
| Concentration | **zmeso** |           | grid          | IPSL      |
| of            |           | mol m-2   |               |           |
| Me            | **zmeso   |           |               |           |
| sozooplankton | -vint**   |           |               |           |
| expressed as  |           |           |               |           |
| Carbon in sea |           |           |               |           |
| water         |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Mole          | **z       | mol m-3   | 0.25° , 1°    | GFDL,     |
| Concentration | micro**   |           | grid          | IPSL      |
| of            |           | mol m-2   |               |           |
| Mic           | -         |           |               |           |
| rozooplankton |  \*zmicro |           |               |           |
| expressed as  |           |           |               |           |
| Carbon in sea | -vint\*\* |           |               |           |
| water         |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Zooplankton   | -   \     | mol m-3   | 0.25° , 1°    | GFDL,     |
| Carbon        | *zooc\*\* |           | grid          | IPSL      |
| Concentration |           | mol m-2   |               |           |
|               | **zooc    |           |               |           |
|               | -vint**   |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Net Downward  | **r       | W m-2     | 0.25° , 1°    | GFDL,     |
| Shortwave     | sntds**   |           | grid          | IPSL      |
| Radiation at  |           |           |               |           |
| Sea Water     |           |           |               |           |
| Surface       |           |           |               |           |
+---------------+-----------+-----------+---------------+-----------+
| Sea Ice Area  | **s       | \%        | 0.25° , 1°    | GFDL,     |
| Fraction      | iconc**   |           | grid          | IPSL      |
+---------------+-----------+-----------+---------------+-----------+

### Climate forcing file locations

The climate forcing input files can be found using the following
pattern:

``` linux
levante:/work/bb0820/ISIMIP/ISIMIP3b/InputData/climate/ocean/uncorrected/<glob
al or regional>/monthly/<climate-scenario>/<climate-forcing>/<climateforcing>_<ensemble-member>_<climate-scenario>_<climatevariable>_global_monthly_<start-year>_<end-year>.nc
```

The variables **deptho** and **thkcello** are fixed through time and can
be found in the "fixed/" folder (rather than monthly/).

#### Note on phytoplankton size structure inputs

Production and carbon data for large and small phytoplankton can be
derived from the variables in Table 1 by the following:

large = diatoms + diazotrophs

small = picophytoplankton

The GFDL model treats diazotrophs as large phytoplankton as part of
their food-web processes.

CHECK SHOULD THE TEXT INSTEAD BE:

\* **Small phytoplankton carbon/production data** are not available on
the server, but can be made by modellers by subtracting diatom
carbon/production from total phytoplankton carbon/production. 

#### Note on regional model spatial extractions

For regional models, only specific grid cells will be needed from the
above global outputs. Please let us know if you require assistance to
extract results (e.g. using bounding boxes, masks or shapefiles). This
functionality is now partially available (bounding box) through the
ISIMIP web-based [data portal](https://data.isimip.org/).

A simple worked example on how to do this for specific regions in R is
provided here: UPDATE FOR PROJECTIONS, ASK MATTHIAS ABOUT GETTING
SHAPEFILES ADDED TO DATA PORTAL

### Fishing effort forcing - NEEDS TO BE UPDATED - OSPs

##### Table 7: Fishing effort forcing files and variables for FishMIP 3b simulations.

+-----------+-------------------------------+-----------------+-----------+
| Specifier | Included variables (short     | Time            | Filename  |
|           | names) and definitions        | pe              |           |
|           |                               | riod/Resolution |           |
+===========+===============================+=================+===========+
| histsoc   | NomActive = Nominal fishing   | -   1850-2015   |           |
|           | effort of the active fleet    |                 |           |
|           | dis-aggregated by:            | -   Annual      |           |
|           |                               |                 |           |
|           | -   eez_country_name = The    |                 |           |
|           |     exclusive economic        |                 |           |
|           |     zone/high seas name in    |                 |           |
|           |     which fishing effort is   |                 |           |
|           |     occurring                 |                 |           |
|           |                               |                 |           |
|           | -   LME = A number code of    |                 |           |
|           |     the Large Marine          |                 |           |
|           |     ecosystem in which the    |                 |           |
|           |     Effort is occurring       |                 |           |
|           |                               |                 |           |
|           | -   SAUP = A number code for  |                 |           |
|           |     the fishing country,      |                 |           |
|           |     following Sea Around Us   |                 |           |
|           |     numbering                 |                 |           |
|           |                               |                 |           |
|           | -   Gear = the fishing gear   |                 |           |
|           |                               |                 |           |
|           | -   FGroup = the targeted     |                 |           |
|           |     functional group          |                 |           |
|           |                               |                 |           |
|           | -   Sector = the fishing      |                 |           |
|           |     sector defined by the law |                 |           |
|           |     of the country            |                 |           |
+-----------+-------------------------------+-----------------+-----------+
| 2015soc   | Final year of values from     | -   2015-2100   |           |
|           | histsoc repeated until 2100   |                 |           |
|           |                               | -   Annual      |           |
+-----------+-------------------------------+-----------------+-----------+
| OSP1soc   | Which variables? Determined   | -   2015-2100   |           |
|           | from % change relative to     |                 |           |
|           | 2015 in SSP1Population,       | -   Annual      |           |
|           | SSP1GDP and relative change   |                 |           |
|           | to 2015 (drivers of?) fishing |                 |           |
|           | effort                        |                 |           |
+-----------+-------------------------------+-----------------+-----------+
| OSP2soc   | Which variables? Determined   | -   2015-2100   |           |
|           | from % change relative to     |                 |           |
|           | 2015 in SSP5Population,       | -   Annual      |           |
|           | SSP5GDP and relative change   |                 |           |
|           | to 2015 (drivers of?) fishing |                 |           |
|           | effort                        |                 |           |
+-----------+-------------------------------+-----------------+-----------+
| H         |                               |                 |           |
| istorical |                               |                 |           |
| P         |                               |                 |           |
| opulation |                               |                 |           |
+-----------+-------------------------------+-----------------+-----------+
| H         |                               |                 |           |
| istorical |                               |                 |           |
| GDP       |                               |                 |           |
+-----------+-------------------------------+-----------------+-----------+
| OTHERS?   |                               |                 |           |
+-----------+-------------------------------+-----------------+-----------+
| SSP1      |                               |                 |           |
| P         |                               |                 |           |
| opulation |                               |                 |           |
+-----------+-------------------------------+-----------------+-----------+
| SSP1 GDP  |                               |                 |           |
+-----------+-------------------------------+-----------------+-----------+
| SSP5      |                               |                 |           |
| P         |                               |                 |           |
| opulation |                               |                 |           |
+-----------+-------------------------------+-----------------+-----------+
| SSP5 GDP  |                               |                 |           |
+-----------+-------------------------------+-----------------+-----------+

##### Table 8: Metadata for histsoc fishing effort variables.

+----------+----------+----------+----------------------------------+
| Va       | Long     | Unit     | Description/notes                |
| riable   | name     |          |                                  |
| Name     |          |          |                                  |
+:=========+:=========+:=========+:=================================+
| Year     | (End of  | Number   |                                  |
|          | the)     | code     |                                  |
|          | year     |          |                                  |
|          | when the |          |                                  |
|          | f ishing |          |                                  |
|          | effort   |          |                                  |
|          | is occ   |          |                                  |
|          | urring   |          |                                  |
+----------+----------+----------+----------------------------------+
| Sector   | The f    | Name     | I = Industrial and A =           |
|          | ishing   | code     | artisanal, where artisanal       |
|          | sector d |          | include powered and unpowered    |
|          | efined   |          | artisanal fleets                 |
|          | by the   |          |                                  |
|          | law of   |          |                                  |
|          | the c    |          |                                  |
|          | ountry   |          |                                  |
+----------+----------+----------+----------------------------------+
| LME      | Large    | Number   | A number code of the Large       |
|          | Marine   | code     | Marine ecosystem in which the    |
|          | Eco      |          | Effort is occurring              |
|          | system   |          |                                  |
|          | Number   |          |                                  |
+----------+----------+----------+----------------------------------+
| eez\_    | Exc      | Name     | The country-level exclusive      |
| countr   | lusive   | code     | economic zone (or high seas)     |
| y_name   | Ec       |          | name in which fishing effort is  |
|          | onomic   |          | occurring                        |
|          | Zone     |          |                                  |
+----------+----------+----------+----------------------------------+
| SAUP     | A number | Number   | Ex supranational entities (USSR, |
|          | code for | code     | Yugoslavia) are disaggregated to |
|          | the f    |          | their constituent countries.     |
|          | ishing   |          | Serbian Fishing Effort included  |
|          | co       |          | with Montenegro. Crimea included |
|          | untry,   |          | with Ukrainian.                  |
|          | fol      |          |                                  |
|          | lowing   |          |                                  |
|          | Sea      |          |                                  |
|          | Around   |          |                                  |
|          | Us num   |          |                                  |
|          | bering   |          |                                  |
+----------+----------+----------+----------------------------------+
| Gear     | The f    | Name     | Gear names                       |
|          | ishing   | code     |                                  |
|          | gear     |          |                                  |
+----------+----------+----------+----------------------------------+
| FGroup   | The ta   | Name     | Functional groups are in         |
|          | rgeted   | code     | accordance with those used by    |
|          | func     |          | the Sea Around Us Project        |
|          | tional   |          |                                  |
|          | group    |          |                                  |
+----------+----------+----------+----------------------------------+
| Nom      | N ominal | Days at  | NomActive (of the active fleet;  |
| Active   | f ishing | sea X kW | i.e., total) = P (engine power   |
|          | effort   |          | of active the fleet; i.e.,       |
|          | (i.e.,   |          | total) x DAS (average days at    |
|          | not inc  |          | sea of one vessel). Average DAS  |
|          | luding   |          | for one vessel \~ 200 DAS/year.  |
|          | the t    |          | NomActive corresponds to the     |
|          | echnol   |          | total (reported, IUU, discards)  |
|          | ogical   |          | catch. To find NomActive in DAS  |
|          | creep)   |          | do (NomActive/P) X NV            |
|          | of the   |          |                                  |
|          | active   |          |                                  |
|          | fleet    |          |                                  |
+----------+----------+----------+----------------------------------+

##### Table 9: Details for OSP relative change in drivers of fishing effort variables.

| OSP  | Variable | Change relative to 2015 |
|------|----------|-------------------------|
| OSP1 | ????     | ????                    |
| OSP2 | ????     | ????                    |

#### Implementation of OSPs

TO DO: We provide code examples showing how to implement the OSPs...
NEED TO ADD TO GITHUB REPO

#### Fishing effort forcing file locations

The monthly fishing effort forcing files for the spin-up and experiments
(Table 1) of this simulation protocol can be found on DKRZ here:

``` linux
levante:/work/bb0820/ISIMIP/ISIMIP3b/InputData/socioeconomic/fishing/histsoc/
```

#### Note on historical global model fishing effort forcing

For **global models**, the above spatially aggregated fishing effort can
be spatially allocated into 1.0 grid cells. This can be achieved using
different approaches such as a simple gravity model -- e.g. see [Coll et
al. 2020](https://www.frontiersin.org/articles/10.3389/fmars.2020.567877/full)
but details will depend on model structure.

TO UPDATE: We are developing a simplified worked example for global
modellers to explore and contribute to. This will be made available on
github/FishMIP in due course.

While we recommend using the above spatially aggregated effort, for
**global models** that cannot technically carry out spatial allocation
of effort, gridded total industrial and artisanal nominal active effort
have been provided in the same folder as the file above and are saved as
netcdf files. These can be allocated to functional groups
(e.g. according to relative biomass) depending on model structure.

#### Note on regional model fishing effort forcing

TO UPDATE/ DEVELOP SEPARATE PROTOCOL FOR: Downscaling of the above
fishing effort to match regional model inputs is likely to be needed. We
request that regional modellers work together in their specific regions
to ensure we have clear and common methodologies.

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
effort files (e.g. LME 22 -- North Sea). These files (SAUPnames.csv and
LMEnames.csv) are also available here:

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/InputData/geo_conditions/fishmip_regions/
```

## Output data {#output-data}

All spatially gridded outputs should be created as netcdf files. More
information on how to prepare these files can be found
[here](https://www.isimip.org/protocol/preparing-simulation-files).
Aspatial regional model results may be saved as .csv files.

UPDATE:In the output files, please label the time variable as "days
since 1841-1-1 00:00:00" if the output covers the spin-up and transition
period (1841-1960) or "days since 1901-1-1 00:00:00" if the output
covers the experiment period (1961-2010).

##### Table 9: Mandatory output variables for Fisheries and Marine Ecosystem models (global and regional). See notes on additional optional model outputs below. Please use the value 1.e+20 for missing data within your output files. **All biomasses are in wet weight (not g C).**

+-----------+-----------+-----------+-----------+-------------------+
| Variable  | Va riable | Unit      | Reso      | Comments          |
| long name | spe       |           | lution    |                   |
|           | cifier    |           |           |                   |
+===========+===========+===========+===========+===================+
| Total     | -         | g m-2     | 1° grid,  | All consumers     |
| Consumer  | \*tcb\*\* |           | annual    | (trophic level    |
| Biomass   |           |           |           | \>1, vertebrates  |
| Density   |           |           |           | and               |
|           |           |           |           | invertebrates)    |
+-----------+-----------+-----------+-----------+-------------------+
| Total     | **tcbl    | g m-2     | 1° grid,  | **Level           |
| Consumer  | og10**    |           | annual    | dim               |
| Biomass   |           |           |           | ensions:** (time, |
| Density   |           |           |           | bins, lat, lon).  |
| in log10  |           |           |           |                   |
| Weight    |           |           |           | If the model is   |
| Bins      |           |           |           | size-structured,  |
|           |           |           |           | please provide    |
|           |           |           |           | biomass in equal  |
|           |           |           |           | log 10 g weight   |
|           |           |           |           | bins (1-10g,      |
|           |           |           |           | 10-100g,          |
|           |           |           |           | 100g-1kg, 1-10kg, |
|           |           |           |           | 10-100kg,         |
|           |           |           |           | \>100kg)          |
+-----------+-----------+-----------+-----------+-------------------+
| Total     | -         | g m-2     | 1° grid,  | All pelagic       |
| Pelagic   | \*tpb\*\* |           | annual    | consumers         |
| Biomass   |           |           |           | (trophic level    |
| Density   |           |           |           | \>1, vertebrates  |
|           |           |           |           | and               |
|           |           |           |           | invertebrates)    |
+-----------+-----------+-----------+-----------+-------------------+
| Total     | -         | g m-2     | 1° grid,  | All demersal      |
| Demersal  | \*tdb\*\* |           | annual    | consumers         |
| Biomass   |           |           |           | (trophic level    |
| Density   |           |           |           | \>1, vertebrates  |
|           |           |           |           | and               |
|           |           |           |           | invertebrates)    |
+-----------+-----------+-----------+-----------+-------------------+
| Total     | **tc**    | g m-2     | 1° grid,  | Catch at sea (all |
| Catch     |           |           | annual    | catch as a result |
| Density   |           |           |           | of all effort     |
| (all      |           |           |           | including         |
| c         |           |           |           | reported and IUU) |
| ommercial |           |           |           | summed for both   |
| f         |           |           |           | Industrial and    |
| unctional |           |           |           | Artisanal sector. |
| groups /  |           |           |           |                   |
| size      |           |           |           |                   |
| classes)  |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Total     | -         | g m-2     | 1° grid,  | Catch at sea (all |
| I         | \*tic\*\* |           | annual    | catch as a result |
| ndustrial |           |           |           | of all effort     |
| Catch     |           |           |           | including         |
| Density   |           |           |           | reported and IUU) |
| (all      |           |           |           | for Industrial    |
| c         |           |           |           | sector only.      |
| ommercial |           |           |           |                   |
| f         |           |           |           |                   |
| unctional |           |           |           |                   |
| groups /  |           |           |           |                   |
| size      |           |           |           |                   |
| classes)  |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Total     | **tcl     | g m-2     | 1° grid,  | **Level           |
| Catch     | og10**    |           | annual    | dim               |
| Density   |           |           |           | ensions:** (time, |
| in log10  |           |           |           | bins, lat, lon).  |
| Weight    |           |           |           |                   |
| Bins      |           |           |           | If the model is   |
| across    |           |           |           | size-structured,  |
| both      |           |           |           | please provide    |
| sectors   |           |           |           | biomass in equal  |
|           |           |           |           | log 10 g weight   |
|           |           |           |           | bins (1-10g,      |
|           |           |           |           | 10-100g,          |
|           |           |           |           | 100g-1kg, 1-10kg, |
|           |           |           |           | 10-100kg,         |
|           |           |           |           | \>100kg)          |
+-----------+-----------+-----------+-----------+-------------------+
| Total     | -         | g m-2     | 1° grid,  | Catch at sea of   |
| Pelagic   | \*tpc\*\* |           | annual    | all pelagic       |
| Density   |           |           |           | consumers         |
| Catch     |           |           |           | (trophic level    |
| across    |           |           |           | \>1, vertebrates  |
| Artisanal |           |           |           | and               |
| and       |           |           |           | invertebrates)    |
| I         |           |           |           |                   |
| ndustrial |           |           |           |                   |
| sectors   |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Total     | -         | g m-2     | 1° grid,  | Catch at sea of   |
| Demersal  | \*tdc\*\* |           | annual    | all demersal      |
| Catch     |           |           |           | consumers         |
| Density   |           |           |           | (trophic level    |
| across    |           |           |           | \>1, vertebrates  |
| Artisanal |           |           |           | and               |
| and       |           |           |           | invertebrates)    |
| I         |           |           |           |                   |
| ndustrial |           |           |           |                   |
| sectors   |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| *         |           |           |           |                   |
| *Optional |           |           |           |                   |
| output    |           |           |           |                   |
| from      |           |           |           |                   |
| global    |           |           |           |                   |
| and       |           |           |           |                   |
| regional  |           |           |           |                   |
| models.   |           |           |           |                   |
| All       |           |           |           |                   |
| biomasses |           |           |           |                   |
| are in    |           |           |           |                   |
| wet       |           |           |           |                   |
| weight,   |           |           |           |                   |
| not g     |           |           |           |                   |
| C.**      |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Biomass   | **bp      | g m-2     | 1° grid,  | If a pelagic      |
| Density   | 30cm**    |           | annual    | species and L     |
| of Small  |           |           |           | infinity is \<30  |
| Pelagics  |           |           |           | cm, include in    |
| \<30cm    |           |           |           | this variable     |
+-----------+-----------+-----------+-----------+-------------------+
| Biomass   | **bp30to  | g m-2     | 1° grid,  | If a pelagic      |
| Density   | 90cm**    |           | annual    | species and L     |
| of Medium |           |           |           | infinity is \>=30 |
| Pelagics  |           |           |           | cm and \<90cm,    |
| \>=30cm   |           |           |           | include in this   |
| and       |           |           |           | variable          |
| \<90cm    |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Biomass   | **bp      | g m-2     | 1° grid,  | If a pelagic      |
| Density   | 90cm**    |           | annual    | species and L     |
| of Large  |           |           |           | infinity is       |
| Pelagics  |           |           |           | \>=90cm, include  |
| \>=90cm   |           |           |           | in this variable  |
+-----------+-----------+-----------+-----------+-------------------+
| Biomass   | **bd      | g m-2     | 1° grid,  | If a demersal     |
| Density   | 30cm**    |           | annual    | species and L     |
| of Small  |           |           |           | infinity is \<30  |
| Demersals |           |           |           | cm, include in    |
| \<30cm    |           |           |           | this variable     |
+-----------+-----------+-----------+-----------+-------------------+
| Biomass   | **bd30to  | g m-2     | 1° grid,  | If a demersal     |
| Density   | 90cm**    |           | annual    | species and L     |
| of Medium |           |           |           | infinity is \>=30 |
| Demersals |           |           |           | cm and \<90cm,    |
| \>=30cm   |           |           |           | include in this   |
| and       |           |           |           | variable          |
| \<90cm    |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Biomass   | **bd      | g m-2     | 1° grid,  | If a demersal     |
| Density   | 90cm**    |           | annual    | species and L     |
| of Large  |           |           |           | infinity is       |
| Demersals |           |           |           | \>=90cm, include  |
| \>=90cm   |           |           |           | in this variable  |
+-----------+-----------+-----------+-----------+-------------------+
| Catch     | **cp      | g m-2     | 1° grid,  | Catch at sea of   |
| Density   | 30cm**    |           | annual    | pelagic species   |
| of Small  |           |           |           | with L infinity   |
| Pelagics  |           |           |           | \<30 cm           |
| \<30cm    |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Catch     | **cp30to  | g m-2     | 1° grid,  | Catch at sea of   |
| Density   | 90cm**    |           | annual    | pelagic species   |
| of Medium |           |           |           | with L infinity   |
| Pelagics  |           |           |           | \>=30 cm and \<90 |
| \>=30cm   |           |           |           | cm                |
| and       |           |           |           |                   |
| \<90cm    |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Catch     | **cp      | g m-2     | 1° grid,  | Catch at sea of   |
| Density   | 90cm**    |           | annual    | pelagic species   |
| of Large  |           |           |           | with L infinity   |
| Pelagics  |           |           |           | \>=90 cm          |
| \>=90cm   |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Catch     | **cd      | g m-2     | 1° grid,  | Catch at sea of   |
| Density   | 30cm**    |           | annual    | demersal species  |
| of Small  |           |           |           | with L infinity   |
| Demersals |           |           |           | \<30 cm           |
| \<30cm    |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Catch     | **cd30to  | g m-2     | 1° grid,  | Catch at sea of   |
| Density   | 90cm**    |           | annual    | demersal species  |
| of Medium |           |           |           | with L infinity   |
| Demersals |           |           |           | \>=30 cm and \<90 |
| \>=30cm   |           |           |           | cm                |
| and       |           |           |           |                   |
| \<90cm    |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+
| Catch     | **cd      | g m-2     | 1° grid,  | Catch at sea of   |
| Density   | 90cm**    |           | annual    | demersal species  |
| of Large  |           |           |           | with L infinity   |
| Demersals |           |           |           | \>=90 cm          |
| \>=90cm   |           |           |           |                   |
+-----------+-----------+-----------+-----------+-------------------+

## SEPARATE? Additional notes for Regional FishMIP Models {#additional-notes-for-regional-fishmip-models}

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

## Reporting model results {#reporting-model-results}

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

-   Report one variable per file.

-   In filenames, use lowercase letters only.

-   Use underscore (\_) to separate identifiers.

-   Variable names consist of a single word without hyphens or
    underscores.

-   Use hyphens (-) to separate strings within an identifier, e.g. in a
    model name.

-   Data model is NETCDF4_CLASSIC with minimum compression level of 5.

-   NetCDF file extension is .nc.

-   UPDATE FOR 3B: The relative time axis' reference date is days since
    1841-1-1 00:00:00 if the output covers the spin-up and transition
    period (1841-1960) or days since 1901-1-1 00:00:00 if the output
    covers the experiment period (1961-2010). We have provided .csv
    files to be used for the time dimension in creating NetCDF files
    based on the 365 days calendar. Please see time_axix_spinup.csv and
    time_axis_experiment.csv in this repository. The script time_axis.r
    was used to create these files.

### Name pattern of output files:

Please name the files in the Fisheries and Marine Ecosystems sector
according to the following pattern:

**Global models**

``` linux
<model>_<climate-forcing>_<bias-adjustment>_<climate-scenario>_<soc-scenario>_<sens-scenario>_<variable>_<global>_<time-step>_<start-year>_<end-year>.nc
```

Example:

``` linux
boats_gfdl_none_historical_histsoc_default_tcb_global_monthly_1850_2100.nc
```

**Regional models**

``` linux
<model>_<climate-forcing>_<bias-adjustment>_<climate-scenario>_<soc-scenario>_<sens-scenario>_<variable>_<region>_<time-step>_<start-year>_<end-year>.nc
```

Example:

``` linux
osmose_gfdl_none_historical_histsoc_default_tcb_benguela_monthly_1850_2100.nc
```

Please see the climate-scenario, soc-scenario, sens-scenario and
variable identifiers given in the tables of this document.

### Path to outut files on DKRZ:

**Global models**

The output files covering the spin-up period (pre-1850) can be saved on
DKRZ here:

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/UploadArea/marine-fishery_global/model_name/temp2
```

The output files covering the experiment period (1850-2010) can be saved
on DKRZ here

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/UploadArea/marine-fishery_global/model_name/temp
```

**Regional models**

The output files covering the spin-up period (pre-1850) can be saved on
DKRZ here:

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/UploadArea/marine-fishery_regional/model_name/temp2
```

The output files covering the experiment period (1850-2100) can be saved
on DKRZ here

``` linux
/work/bb0820/ISIMIP/ISIMIP3a/UploadArea/marine-fishery_regional/model_name/temp
```

Please contact FishMIP coordinators or ISIMIP data managers directly
([isimip-data\@pik‐potsdam.de](mailto:isimip-data@pik%E2%80%90potsdam.de))
if you have any questions or clarifications before submitting files or
if you do not find your model's path on DKRZ as described above.

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
