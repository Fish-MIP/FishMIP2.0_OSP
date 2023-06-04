---
editor_options:
  markdown:
    wrap: 72
output:
  word_document: default
  pdf_document: default
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

+----------+----------+----------+----------+----------+
|          | Ex       | Short    | Hi       | Future   |
|          | periment | des      | storical |          |
|          |          | cription |          |          |
+==========+==========+==========+==========+==========+
| 1        | **Pre-in | **Cl     | p        | p        |
|          | dustrial | imate**: | icontrol | icontrol |
|          | c        | No       |          |          |
|          | ontrol** | climate  | nat      | nat      |
|          |          | change,  |          |          |
|          | nat      | fixed    |          |          |
|          |          | 1850s    |          |          |
|          |          | CO~`2`~  |          |          |
|          |          | levels   |          |          |
|          |          |          |          |          |
|          |          | **F      |          |          |
|          |          | i        |          |          |
|          |          | shing**: |          |          |
|          |          | No       |          |          |
|          |          | fishing  |          |          |
+----------+----------+----------+----------+----------+
| 2        | **Pr e-i | **C      | p        | p        |
|          | n        | l        | icontrol | icontrol |
|          | dustrial | imate**: |          |          |
|          | c        | No       | histsoc  | 2015soc  |
|          | ontrol** | climate  |          |          |
|          |          | change,  |          |          |
|          | histsoc  | fixed    |          |          |
|          |          | 1850s    |          |          |
|          |          | CO~`2`~  |          |          |
|          |          | levels   |          |          |
|          |          |          |          |          |
|          |          | **F      |          |          |
|          |          | i        |          |          |
|          |          | shing**: |          |          |
|          |          | H        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | fishing  |          |          |
|          |          | effort,  |          |          |
|          |          | then     |          |          |
|          |          | future   |          |          |
|          |          | fixed at |          |          |
|          |          | 2015     |          |          |
|          |          | levels   |          |          |
+----------+----------+----------+----------+----------+
| 3        | **S SP1  | **C      | h        | ssp126   |
|          | -        | l        | i        |          |
|          | RCP2.6** | imate**: | storical | nat      |
|          |          | S        |          |          |
|          | nat      | imulated | nat      |          |
|          |          | hi       |          |          |
|          |          | storical |          |          |
|          |          | climate, |          |          |
|          |          | then SS  |          |          |
|          |          | P        |          |          |
|          |          | 1-RCP2.6 |          |          |
|          |          | climate  |          |          |
|          |          |          |          |          |
|          |          | **Fis    |          |          |
|          |          | h        |          |          |
|          |          | ing**:No |          |          |
|          |          | fishing  |          |          |
+----------+----------+----------+----------+----------+
| 4        | **S SP1  | **C      | h        | ssp126   |
|          | -        | l        | i        |          |
|          | RCP2.6** | imate**: | storical | 2015soc  |
|          |          | S        |          |          |
|          | histsoc  | imulated | histsoc  |          |
|          |          | h        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | climate, |          |          |
|          |          | then SS  |          |          |
|          |          | P        |          |          |
|          |          | 1-RCP2.6 |          |          |
|          |          | climate  |          |          |
|          |          |          |          |          |
|          |          | **F      |          |          |
|          |          | i        |          |          |
|          |          | shing**: |          |          |
|          |          | H        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | fishing  |          |          |
|          |          | effort,  |          |          |
|          |          | then     |          |          |
|          |          | future   |          |          |
|          |          | fixed at |          |          |
|          |          | 2015     |          |          |
|          |          | levels   |          |          |
+----------+----------+----------+----------+----------+
| 5        | **S SP1  | **C      | h        | ssp126   |
|          | -        | l        | i        |          |
|          | RCP2.6** | imate**: | storical | OSP1soc  |
|          |          | S        |          |          |
|          | OSP1     | imulated | histsoc  |          |
|          |          | h        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | climate, |          |          |
|          |          | then SS  |          |          |
|          |          | P        |          |          |
|          |          | 1-RCP2.6 |          |          |
|          |          | climate  |          |          |
|          |          |          |          |          |
|          |          | **F      |          |          |
|          |          | i        |          |          |
|          |          | shing**: |          |          |
|          |          | H        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | fishing  |          |          |
|          |          | effort,  |          |          |
|          |          | then     |          |          |
|          |          | change   |          |          |
|          |          | driven   |          |          |
|          |          | by OSP1  |          |          |
+----------+----------+----------+----------+----------+
| 6        | **S SP5  | **C      | h        | ssp585   |
|          | -        | l        | i        |          |
|          | RCP8.5** | imate**: | storical | nat      |
|          |          | S        |          |          |
|          | nat      | imulated | nat      |          |
|          |          | h        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | climate, |          |          |
|          |          | then SS  |          |          |
|          |          | P        |          |          |
|          |          | 5-RCP2.6 |          |          |
|          |          | climate  |          |          |
|          |          |          |          |          |
|          |          | **F      |          |          |
|          |          | i        |          |          |
|          |          | shing**: |          |          |
|          |          | No       |          |          |
|          |          | fishing  |          |          |
+----------+----------+----------+----------+----------+
| 7        | **S SP5  | **C      | h        | ssp585   |
|          | -        | l        | i        |          |
|          | RCP8.5** | imate**: | storical | 2015soc  |
|          |          | S        |          |          |
|          | histsoc  | imulated | histsoc  |          |
|          |          | h        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | climate, |          |          |
|          |          | then SS  |          |          |
|          |          | P        |          |          |
|          |          | 5-RCP8.5 |          |          |
|          |          | climate  |          |          |
|          |          |          |          |          |
|          |          | **F      |          |          |
|          |          | i        |          |          |
|          |          | shing**: |          |          |
|          |          | H        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | fishing  |          |          |
|          |          | effort,  |          |          |
|          |          | then     |          |          |
|          |          | held     |          |          |
|          |          | fixed at |          |          |
|          |          | 2015     |          |          |
|          |          | levels   |          |          |
+----------+----------+----------+----------+----------+
| 8        | **S SP5  | **C      | h        | ssp585   |
|          | -        | l        | i        |          |
|          | RCP8.5** | imate**: | storical | OSP2soc  |
|          |          | S        |          |          |
|          | OSP2soc? | imulated | histsoc  |          |
|          |          | h        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | climate, |          |          |
|          |          | then SS  |          |          |
|          |          | P        |          |          |
|          |          | 5-RCP8.5 |          |          |
|          |          | climate  |          |          |
|          |          |          |          |          |
|          |          | **F      |          |          |
|          |          | i        |          |          |
|          |          | shing**: |          |          |
|          |          | H        |          |          |
|          |          | i        |          |          |
|          |          | storical |          |          |
|          |          | fishing  |          |          |
|          |          | effort,  |          |          |
|          |          | then     |          |          |
|          |          | change   |          |          |
|          |          | driven   |          |          |
|          |          | by OSP2  |          |          |
+----------+----------+----------+----------+----------+

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

+----------------+--------------------------------------------------+
| **Scenario     | **Description**                                  |
| specifier**    |                                                  |
+:===============+:=================================================+
| picontrol      | Pre-industrial climate as simulated by the Earth |
|                | System Models (ESMs)                             |
+----------------+--------------------------------------------------+
| historical     | Historical climate as simulated by the ESMs,     |
|                | starting in 1950.                                |
+----------------+--------------------------------------------------+
| ssp126         | SSP1-RCP2.6 climate as simulated by the ESMs     |
+----------------+--------------------------------------------------+
| ssp585         | SSP5-RCP8.5 climate as simulated by the ESMs.    |
+----------------+--------------------------------------------------+
| sspXXX         | ANY OTHERS?                                      |
+----------------+--------------------------------------------------+

##### Table 3: Socio-economic scenario specifiers (soc-scenario).

+---------------+-------------------------------------------------+
| **Scenario    | **Description**                                 |
| specifier**   |                                                 |
+:==============+:================================================+
| **histsoc**   | Varying direct human influences in the          |
|               | historical period (1850-2014) (i.e. historical  |
|               | estimates of fishing effort).                   |
+---------------+-------------------------------------------------+
| **2015soc**   | Fixed year-2015 direct human influences         |
|               | (i.e. fishing effort).                          |
+---------------+-------------------------------------------------+
| **OSPXsoc**   | Future fishing determined by SSP1 and OSP       |
|               | driver forcings for OSPX                        |
+---------------+-------------------------------------------------+
| **OSPXsoc**   | Future fishing determined by SSP5 and OSP       |
|               | driver forcings for OSPX                        |
+---------------+-------------------------------------------------+
| **nat**       | No fishing (naturalized run).                   |
+---------------+-------------------------------------------------+

**Please remember to use these same specifiers in your output files.
More on reporting data can be found at the end of this document.**

## Input data {#input-data}

**For modellers new to FishMIP:** to access all input data you first
need to set up an account with ISIMIP to access the DKRZ server. Please
follow the instructions here:
<https://www.isimip.org/dashboard/accessing-isimip-data-dkrz-server/>

### Climate forcing {#climate-forcing}

##### Table 5: Climate forcing

+------------+------------+-----------------------+------------+
| Title      | Spec       | Institution           | Or iginal  |
|            | ifiers     |                       | reso       |
|            |            |                       | lution     |
+:===========+:===========+:======================+:===========+
| GF DLESM4  | gf dlesm4  | National Oceanic and  | 2 88x180   |
|            |            | Atmospheric           |            |
|            |            | Administration,       |            |
|            |            | Geophysical Fluid     |            |
|            |            | Dynamics Laboratory,  |            |
|            |            | Princeton, NJ 08540,  |            |
|            |            | USA                   |            |
+------------+------------+-----------------------+------------+
| IPSL       | ipslc      | Institut Pierre Simon | 1 44x143   |
| CM6ALR     | m6a-lr     | Laplace, Paris 75252, |            |
|            |            | France                |            |
+------------+------------+-----------------------+------------+
| OT HERS??  |            |                       |            |
+------------+------------+-----------------------+------------+

MATTHIAS/CHERYL:CROSS CHECK WHAT WE HAVE Vs WHAT IS BELOW

##### Table 6. Climate forcing variables and units for FishMIP 3a simulations. All variables are available on a 0.25 and 1 degree horizontal grid, monthly and annual resolutions. Note: Some variables are available as specific layers extracted from vertically resolved data. Their variable names have been suffixed with -bot (ocean bottom, e.g. o2-bot), -surf (surface values, e.g. pH-surf) or -vint (vertically integrated, e.g. phyc-vint), respectively, or prefixed with int (vertically integrated, e.g. intpp). Temperature is suffixed with b or s for bottom (e.g. tob) or surface (e.g. tos) layers, respectively.

+-----------+-----------+-----------+-----------+-----------+
| Variable  | Sp        | Unit      | Res       | ESM       |
|           | ecifier   |           | olution   | datasets  |
+===========+===========+===========+===========+===========+
| Mass Con  | **chl**   | kg m-3    | 0.25° ,   | GFDL,     |
| c         |           |           | 1° grid   | IPSL      |
| entration |           |           |           |           |
| of Total  |           |           |           |           |
| Phy       |           |           |           |           |
| t         |           |           |           |           |
| oplankton |           |           |           |           |
| Expressed |           |           |           |           |
| as C      |           |           |           |           |
| h         |           |           |           |           |
| lorophyll |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Sea Floor | -   \*    | m         | 0.25° ,   | GFDL,     |
| Depth     |     d     |           | 1° grid   | IPSL      |
|           | eptho\*\* |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Downward  | **exp     | mol m-2   | 0.25° ,   | GFDL,     |
| Flux of P | c-bot**   | s-1       | 1° grid   | IPSL      |
| a         |           |           |           |           |
| rticulate |           |           |           |           |
| Organic   |           |           |           |           |
| Carbon    |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| P         | -   \*    | kg m-2    | 0.25° ,   | GFDL,     |
| a         |     i     |           | 1° grid   | IPSL      |
| rticulate | ntpoc\*\* |           |           |           |
| Organic   |           |           |           |           |
| Carbon    |           |           |           |           |
| Content   |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Primary   | **intpp** | mol m-2   | 0.25° ,   | GFDL,     |
| Organic   |           | s-1       | 1° grid   | IPSL      |
| Carbon    |           |           |           |           |
| P         |           |           |           |           |
| roduction |           |           |           |           |
| by All    |           |           |           |           |
| Types of  |           |           |           |           |
| Phy       |           |           |           |           |
| t         |           |           |           |           |
| oplankton |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Net       | **intp    | mol m-2   | 0.25° ,   | GFDL,     |
| Primary   | pdiat**   | s-1       | 1° grid   | IPSL      |
| Organic   |           |           |           |           |
| Carbon    |           |           |           |           |
| P         |           |           |           |           |
| roduction |           |           |           |           |
| by        |           |           |           |           |
| Diatoms   |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Net       | **intp    | mol m-2   | 0.25° ,   | GFDL,     |
| Primary   | pdiaz**   | s-1       | 1° grid   | IPSL      |
| Mole Pr   |           |           |           |           |
| o         |           |           |           |           |
| ductivity |           |           |           |           |
| of Carbon |           |           |           |           |
| by D      |           |           |           |           |
| i         |           |           |           |           |
| azotrophs |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Net       | **intp    | mol m-2   | 0.25° ,   | GFDL,     |
| Primary   | ppico**   | s-1       | 1° grid   | IPSL      |
| Mole Pr   |           |           |           |           |
| o         |           |           |           |           |
| ductivity |           |           |           |           |
| of Carbon |           |           |           |           |
| by Pico   |           |           |           |           |
| phy       |           |           |           |           |
| t         |           |           |           |           |
| oplankton |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Maximum   | -         | m         | 0.25° ,   | GFDL,     |
| Ocean     |  \*mlotst |           | 1° grid   | IPSL      |
| Mixed     |           | m         |           |           |
| Layer     | -0125\*\* |           |           |           |
| Thickness |           |           |           |           |
| Defined   |           |           |           |           |
| by Sigma  |           |           |           |           |
| T         |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Dissolved | **o2,**   | mol m-3   | 0.25° ,   | GFDL,     |
| Oxygen    |           |           | 1° grid   | IPSL      |
| Con       | **o       | mol m-2   |           |           |
| c         | 2-bot**   |           |           |           |
| entration |           | mol m-2   |           |           |
|           | **o2      |           |           |           |
|           | -surf**   |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| pH        | **ph**    | 1         | 0.25° ,   | GFDL,     |
|           |           |           | 1° grid   | IPSL      |
|           | **p       | 1         |           |           |
|           | h-bot**   |           |           |           |
|           |           | 1         |           |           |
|           | **ph      |           |           |           |
|           | -surf**   |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Phy       | -   \     | mol m-3   | 0.25° ,   | GFDL,     |
| t         |           |           | 1° grid   | IPSL      |
| oplankton | \         | mol m-2   |           |           |
| Carbon    | *phyc\*\* |           |           |           |
| Con       |           |           |           |           |
| c         | **phyc    |           |           |           |
| entration | -vint**   |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Mole Con  | **ph      | mol m-3   | 0.25° ,   | GFDL,     |
| c         | ydiat**   |           | 1° grid   | IPSL      |
| entration |           | mol m-2   |           |           |
| of        | **phydiat |           |           |           |
| Diatoms   | -vint**   |           |           |           |
| expressed |           |           |           |           |
| as Carbon |           |           |           |           |
| in sea    |           |           |           |           |
| water     |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Mole Con  | **ph      | mol m-3   | 0.25° ,   | GFDL,     |
| c         | ydiaz**   |           | 1° grid   | IPSL      |
| entration |           | mol m-2   |           |           |
| of D      | **phydiaz |           |           |           |
| i         | -vint**   |           |           |           |
| azotrophs |           |           |           |           |
| Expressed |           |           |           |           |
| as Carbon |           |           |           |           |
| in Sea    |           |           |           |           |
| Water     |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Mole Con  | **ph      | mol m-3   | 0.25° ,   | GFDL,     |
| c         | ypico**   |           | 1° grid   | IPSL      |
| entration |           | mol m-2   |           |           |
| of Pico   | **phypico |           |           |           |
| phy       | -vint**   |           |           |           |
| t         |           |           |           |           |
| oplankton |           |           |           |           |
| Expressed |           |           |           |           |
| as Carbon |           |           |           |           |
| in Sea    |           |           |           |           |
| Water     |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Sea Water | **so**    | ‰         | 0.25° ,   | GFDL,     |
| Salinity  |           |           | 1° grid   | IPSL      |
|           | **s       | ‰\        |           |           |
|           | o-bot**   | ‰         |           |           |
|           |           |           |           |           |
|           | **so      |           |           |           |
|           | -surf**   |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Sea Water | **t       | °C        | 0.25° ,   | GFDL,     |
| Potential | hetao**   |           | 1° grid   | IPSL      |
| T         |           |           |           |           |
| e         |           |           |           |           |
| mperature |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Ocean     | **thk     | m         | 0.25° ,   | GFDL,     |
| Model     | cello**   |           | 1° grid   | IPSL      |
| Cell      |           |           |           |           |
| Thickness |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Sea Water | **tob**   | °C        | 0.25° ,   | GFDL,     |
| Potential |           |           | 1° grid   | IPSL      |
| T         |           |           |           |           |
| e         |           |           |           |           |
| mperature |           |           |           |           |
| at Sea    |           |           |           |           |
| Floor     |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Sea       | **tos**   | °C        | 0.25° ,   | GFDL,     |
| Surface T |           |           | 1° grid   | IPSL      |
| e         |           |           |           |           |
| mperature |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Sea Water | **uo**    | m s-1     | 0.25° ,   | GFDL,     |
| X         |           |           | 1° grid   | IPSL      |
| Velocity  |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Sea Water | **vo**    | m s-1     | 0.25° ,   | GFDL,     |
| Y         |           |           | 1° grid   | IPSL      |
| Velocity  |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Mole Con  | **zmeso** | mol m-3   | 0.25° ,   | GFDL,     |
| c         |           |           | 1° grid   | IPSL      |
| entration | **zmeso   | mol m-2   |           |           |
| of Me soz | -vint**   |           |           |           |
| o         |           |           |           |           |
| oplankton |           |           |           |           |
| expressed |           |           |           |           |
| as Carbon |           |           |           |           |
| in sea    |           |           |           |           |
| water     |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Mole Con  | **z       | mol m-3   | 0.25° ,   | GFDL,     |
| c         | micro**   |           | 1° grid   | IPSL      |
| entration |           | mol m-2   |           |           |
| of Mic    | -         |           |           |           |
| roz       |  \*zmicro |           |           |           |
| o         |           |           |           |           |
| oplankton | -vint\*\* |           |           |           |
| expressed |           |           |           |           |
| as Carbon |           |           |           |           |
| in sea    |           |           |           |           |
| water     |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Z         | -   \     | mol m-3   | 0.25° ,   | GFDL,     |
| o         |           |           | 1° grid   | IPSL      |
| oplankton | \         | mol m-2   |           |           |
| Carbon    | *zooc\*\* |           |           |           |
| Con       |           |           |           |           |
| c         | **zooc    |           |           |           |
| entration | -vint**   |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Net       | **r       | W m-2     | 0.25° ,   | GFDL,     |
| Downward  | sntds**   |           | 1° grid   | IPSL      |
| Shortwave |           |           |           |           |
| Radiation |           |           |           |           |
| at Sea    |           |           |           |           |
| Water     |           |           |           |           |
| Surface   |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+
| Sea Ice   | **s       | \%        | 0.25° ,   | GFDL,     |
| Area      | iconc**   |           | 1° grid   | IPSL      |
| Fraction  |           |           |           |           |
+-----------+-----------+-----------+-----------+-----------+

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

+-------------+---------------------+-------------+-------------+
| Specifier   | Included variables  | Time pe     | Filename    |
|             | (short names) and   | riod        |             |
|             | definitions         | /Resolution |             |
+=============+=====================+=============+=============+
| histsoc     | NomActive = Nominal | -           |             |
|             | fishing effort of   |   1850-2015 |             |
|             | the active fleet    |             |             |
|             | dis-aggregated by:  | -   Annual  |             |
|             |                     |             |             |
|             | -                   |             |             |
|             |    eez_country_name |             |             |
|             |     = The exclusive |             |             |
|             |     economic        |             |             |
|             |     zone/high seas  |             |             |
|             |     name in which   |             |             |
|             |     fishing effort  |             |             |
|             |     is occurring    |             |             |
|             |                     |             |             |
|             | -   LME = A number  |             |             |
|             |     code of the     |             |             |
|             |     Large Marine    |             |             |
|             |     ecosystem in    |             |             |
|             |     which the       |             |             |
|             |     Effort is       |             |             |
|             |     occurring       |             |             |
|             |                     |             |             |
|             | -   SAUP = A number |             |             |
|             |     code for the    |             |             |
|             |     fishing         |             |             |
|             |     country,        |             |             |
|             |     following Sea   |             |             |
|             |     Around Us       |             |             |
|             |     numbering       |             |             |
|             |                     |             |             |
|             | -   Gear = the      |             |             |
|             |     fishing gear    |             |             |
|             |                     |             |             |
|             | -   FGroup = the    |             |             |
|             |     targeted        |             |             |
|             |     functional      |             |             |
|             |     group           |             |             |
|             |                     |             |             |
|             | -   Sector = the    |             |             |
|             |     fishing sector  |             |             |
|             |     defined by the  |             |             |
|             |     law of the      |             |             |
|             |     country         |             |             |
+-------------+---------------------+-------------+-------------+
| 2015soc     | Final year of       | -           |             |
|             | values from histsoc |   2015-2100 |             |
|             | repeated until 2100 |             |             |
|             |                     | -   Annual  |             |
+-------------+---------------------+-------------+-------------+
| OSP1soc     | Which variables?    | -           |             |
|             | Determined from %   |   2015-2100 |             |
|             | change relative to  |             |             |
|             | 2015 in             | -   Annual  |             |
|             | SSP1Population,     |             |             |
|             | SSP1GDP and         |             |             |
|             | relative change to  |             |             |
|             | 2015 (drivers of?)  |             |             |
|             | fishing effort      |             |             |
+-------------+---------------------+-------------+-------------+
| OSP2soc     | Which variables?    | -           |             |
|             | Determined from %   |   2015-2100 |             |
|             | change relative to  |             |             |
|             | 2015 in             | -   Annual  |             |
|             | SSP5Population,     |             |             |
|             | SSP5GDP and         |             |             |
|             | relative change to  |             |             |
|             | 2015 (drivers of?)  |             |             |
|             | fishing effort      |             |             |
+-------------+---------------------+-------------+-------------+
| H istorical |                     |             |             |
| P opulation |                     |             |             |
+-------------+---------------------+-------------+-------------+
| H istorical |                     |             |             |
| GDP         |                     |             |             |
+-------------+---------------------+-------------+-------------+
| OTHERS?     |                     |             |             |
+-------------+---------------------+-------------+-------------+
| SSP1 P      |                     |             |             |
| opulation   |                     |             |             |
+-------------+---------------------+-------------+-------------+
| SSP1 GDP    |                     |             |             |
+-------------+---------------------+-------------+-------------+
| SSP5 P      |                     |             |             |
| opulation   |                     |             |             |
+-------------+---------------------+-------------+-------------+
| SSP5 GDP    |                     |             |             |
+-------------+---------------------+-------------+-------------+

##### Table 8: Metadata for histsoc fishing effort variables.

+------------+------------+------------+-----------------------+
| Va riable  | Long name  | Unit       | Description/notes     |
| Name       |            |            |                       |
+:===========+:===========+:===========+:======================+
| Year       | (End of    | Number     |                       |
|            | the) year  | code       |                       |
|            | when the f |            |                       |
|            | ishing     |            |                       |
|            | effort is  |            |                       |
|            | occ urring |            |                       |
+------------+------------+------------+-----------------------+
| Sector     | The f      | Name code  | I = Industrial and A  |
|            | ishing     |            | = artisanal, where    |
|            | sector d   |            | artisanal include     |
|            | efined by  |            | powered and unpowered |
|            | the law of |            | artisanal fleets      |
|            | the c      |            |                       |
|            | ountry     |            |                       |
+------------+------------+------------+-----------------------+
| LME        | Large      | Number     | A number code of the  |
|            | Marine Eco | code       | Large Marine          |
|            | system     |            | ecosystem in which    |
|            | Number     |            | the Effort is         |
|            |            |            | occurring             |
+------------+------------+------------+-----------------------+
| eez\_      | Exc lusive | Name code  | The country-level     |
| countr     | Ec onomic  |            | exclusive economic    |
| y_name     | Zone       |            | zone (or high seas)   |
|            |            |            | name in which fishing |
|            |            |            | effort is occurring   |
+------------+------------+------------+-----------------------+
| SAUP       | A number   | Number     | Ex supranational      |
|            | code for   | code       | entities (USSR,       |
|            | the f      |            | Yugoslavia) are       |
|            | ishing co  |            | disaggregated to      |
|            | untry, fol |            | their constituent     |
|            | lowing Sea |            | countries. Serbian    |
|            | Around Us  |            | Fishing Effort        |
|            | num bering |            | included with         |
|            |            |            | Montenegro. Crimea    |
|            |            |            | included with         |
|            |            |            | Ukrainian.            |
+------------+------------+------------+-----------------------+
| Gear       | The f      | Name code  | Gear names            |
|            | ishing     |            |                       |
|            | gear       |            |                       |
+------------+------------+------------+-----------------------+
| FGroup     | The ta     | Name code  | Functional groups are |
|            | rgeted     |            | in accordance with    |
|            | func       |            | those used by the Sea |
|            | tional     |            | Around Us Project     |
|            | group      |            |                       |
+------------+------------+------------+-----------------------+
| Nom Active | N ominal f | Days at    | NomActive (of the     |
|            | ishing     | sea X kW   | active fleet; i.e.,   |
|            | effort     |            | total) = P (engine    |
|            | (i.e., not |            | power of active the   |
|            | inc luding |            | fleet; i.e., total) x |
|            | the t      |            | DAS (average days at  |
|            | echnol     |            | sea of one vessel).   |
|            | ogical     |            | Average DAS for one   |
|            | creep) of  |            | vessel \~ 200         |
|            | the active |            | DAS/year. NomActive   |
|            | fleet      |            | corresponds to the    |
|            |            |            | total (reported, IUU, |
|            |            |            | discards) catch. To   |
|            |            |            | find NomActive in DAS |
|            |            |            | do (NomActive/P) X NV |
+------------+------------+------------+-----------------------+

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

+------------+------------+------------+------------+------------+
| Variable   | Va riable  | Unit       | Reso       | Comments   |
| long name  | spe cifier |            | lution     |            |
+============+============+============+============+============+
| Total      | -          | g m-2      | 1° grid,   | All        |
| Consumer   |  \*tcb\*\* |            | annual     | consumers  |
| Biomass    |            |            |            | (trophic   |
| Density    |            |            |            | level \>1, |
|            |            |            |            | v          |
|            |            |            |            | ertebrates |
|            |            |            |            | and in     |
|            |            |            |            | ve         |
|            |            |            |            | rtebrates) |
+------------+------------+------------+------------+------------+
| Total      | **tcbl     | g m-2      | 1° grid,   | **Level    |
| Consumer   | og10**     |            | annual     | dim ensio  |
| Biomass    |            |            |            | ns         |
| Density in |            |            |            | :** (time, |
| log10      |            |            |            | bins, lat, |
| Weight     |            |            |            | lon).      |
| Bins       |            |            |            |            |
|            |            |            |            | If the     |
|            |            |            |            | model is   |
|            |            |            |            | size       |
|            |            |            |            | -s         |
|            |            |            |            | tructured, |
|            |            |            |            | please     |
|            |            |            |            | provide    |
|            |            |            |            | biomass in |
|            |            |            |            | equal log  |
|            |            |            |            | 10 g       |
|            |            |            |            | weight     |
|            |            |            |            | bins       |
|            |            |            |            | (1-10g,    |
|            |            |            |            | 10-100g,   |
|            |            |            |            | 100g-1kg,  |
|            |            |            |            | 1-10kg,    |
|            |            |            |            | 10-100kg,  |
|            |            |            |            | \>100kg)   |
+------------+------------+------------+------------+------------+
| Total      | -          | g m-2      | 1° grid,   | All        |
| Pelagic    |  \*tpb\*\* |            | annual     | pelagic    |
| Biomass    |            |            |            | consumers  |
| Density    |            |            |            | (trophic   |
|            |            |            |            | level \>1, |
|            |            |            |            | v          |
|            |            |            |            | ertebrates |
|            |            |            |            | and in     |
|            |            |            |            | ve         |
|            |            |            |            | rtebrates) |
+------------+------------+------------+------------+------------+
| Total      | -          | g m-2      | 1° grid,   | All        |
| Demersal   |  \*tdb\*\* |            | annual     | demersal   |
| Biomass    |            |            |            | consumers  |
| Density    |            |            |            | (trophic   |
|            |            |            |            | level \>1, |
|            |            |            |            | v          |
|            |            |            |            | ertebrates |
|            |            |            |            | and in     |
|            |            |            |            | ve         |
|            |            |            |            | rtebrates) |
+------------+------------+------------+------------+------------+
| Total      | **tc**     | g m-2      | 1° grid,   | Catch at   |
| Catch      |            |            | annual     | sea (all   |
| Density    |            |            |            | catch as a |
| (all c     |            |            |            | result of  |
| ommercial  |            |            |            | all effort |
| f          |            |            |            | including  |
| unctional  |            |            |            | reported   |
| groups /   |            |            |            | and IUU)   |
| size       |            |            |            | summed for |
| classes)   |            |            |            | both       |
|            |            |            |            | Industrial |
|            |            |            |            | and        |
|            |            |            |            | Artisanal  |
|            |            |            |            | sector.    |
+------------+------------+------------+------------+------------+
| Total I    | -          | g m-2      | 1° grid,   | Catch at   |
| ndustrial  |  \*tic\*\* |            | annual     | sea (all   |
| Catch      |            |            |            | catch as a |
| Density    |            |            |            | result of  |
| (all c     |            |            |            | all effort |
| ommercial  |            |            |            | including  |
| f          |            |            |            | reported   |
| unctional  |            |            |            | and IUU)   |
| groups /   |            |            |            | for        |
| size       |            |            |            | Industrial |
| classes)   |            |            |            | sector     |
|            |            |            |            | only.      |
+------------+------------+------------+------------+------------+
| Total      | **tcl      | g m-2      | 1° grid,   | **Level    |
| Catch      | og10**     |            | annual     | dim ensio  |
| Density in |            |            |            | ns         |
| log10      |            |            |            | :** (time, |
| Weight     |            |            |            | bins, lat, |
| Bins       |            |            |            | lon).      |
| across     |            |            |            |            |
| both       |            |            |            | If the     |
| sectors    |            |            |            | model is   |
|            |            |            |            | size       |
|            |            |            |            | -s         |
|            |            |            |            | tructured, |
|            |            |            |            | please     |
|            |            |            |            | provide    |
|            |            |            |            | biomass in |
|            |            |            |            | equal log  |
|            |            |            |            | 10 g       |
|            |            |            |            | weight     |
|            |            |            |            | bins       |
|            |            |            |            | (1-10g,    |
|            |            |            |            | 10-100g,   |
|            |            |            |            | 100g-1kg,  |
|            |            |            |            | 1-10kg,    |
|            |            |            |            | 10-100kg,  |
|            |            |            |            | \>100kg)   |
+------------+------------+------------+------------+------------+
| Total      | -          | g m-2      | 1° grid,   | Catch at   |
| Pelagic    |  \*tpc\*\* |            | annual     | sea of all |
| Density    |            |            |            | pelagic    |
| Catch      |            |            |            | consumers  |
| across     |            |            |            | (trophic   |
| Artisanal  |            |            |            | level \>1, |
| and I      |            |            |            | v          |
| ndustrial  |            |            |            | ertebrates |
| sectors    |            |            |            | and in     |
|            |            |            |            | ve         |
|            |            |            |            | rtebrates) |
+------------+------------+------------+------------+------------+
| Total      | -          | g m-2      | 1° grid,   | Catch at   |
| Demersal   |  \*tdc\*\* |            | annual     | sea of all |
| Catch      |            |            |            | demersal   |
| Density    |            |            |            | consumers  |
| across     |            |            |            | (trophic   |
| Artisanal  |            |            |            | level \>1, |
| and I      |            |            |            | v          |
| ndustrial  |            |            |            | ertebrates |
| sectors    |            |            |            | and in     |
|            |            |            |            | ve         |
|            |            |            |            | rtebrates) |
+------------+------------+------------+------------+------------+
| -          |            |            |            |            |
| \*Optional |            |            |            |            |
|     output |            |            |            |            |
|     from   |            |            |            |            |
|     global |            |            |            |            |
|     and    |            |            |            |            |
|            |            |            |            |            |
|            |            |            |            |            |
|   regional |            |            |            |            |
|            |            |            |            |            |
|            |            |            |            |            |
|    models. |            |            |            |            |
|     All    |            |            |            |            |
|            |            |            |            |            |
|            |            |            |            |            |
|  biomasses |            |            |            |            |
|     are in |            |            |            |            |
|     wet    |            |            |            |            |
|            |            |            |            |            |
|            |            |            |            |            |
|    weight, |            |            |            |            |
|     not g  |            |            |            |            |
|     C.\*\* |            |            |            |            |
+------------+------------+------------+------------+------------+
| Biomass    | **bp       | g m-2      | 1° grid,   | If a       |
| Density of | 30cm**     |            | annual     | pelagic    |
| Small      |            |            |            | species    |
| Pelagics   |            |            |            | and L      |
| \<30cm     |            |            |            | infinity   |
|            |            |            |            | is \<30    |
|            |            |            |            | cm,        |
|            |            |            |            | include in |
|            |            |            |            | this       |
|            |            |            |            | variable   |
+------------+------------+------------+------------+------------+
| Biomass    | **bp30to   | g m-2      | 1° grid,   | If a       |
| Density of | 90cm**     |            | annual     | pelagic    |
| Medium     |            |            |            | species    |
| Pelagics   |            |            |            | and L      |
| \>=30cm    |            |            |            | infinity   |
| and \<90cm |            |            |            | is \>=30   |
|            |            |            |            | cm and     |
|            |            |            |            | \<90cm,    |
|            |            |            |            | include in |
|            |            |            |            | this       |
|            |            |            |            | variable   |
+------------+------------+------------+------------+------------+
| Biomass    | **bp       | g m-2      | 1° grid,   | If a       |
| Density of | 90cm**     |            | annual     | pelagic    |
| Large      |            |            |            | species    |
| Pelagics   |            |            |            | and L      |
| \>=90cm    |            |            |            | infinity   |
|            |            |            |            | is         |
|            |            |            |            | \>=90cm,   |
|            |            |            |            | include in |
|            |            |            |            | this       |
|            |            |            |            | variable   |
+------------+------------+------------+------------+------------+
| Biomass    | **bd       | g m-2      | 1° grid,   | If a       |
| Density of | 30cm**     |            | annual     | demersal   |
| Small      |            |            |            | species    |
| Demersals  |            |            |            | and L      |
| \<30cm     |            |            |            | infinity   |
|            |            |            |            | is \<30    |
|            |            |            |            | cm,        |
|            |            |            |            | include in |
|            |            |            |            | this       |
|            |            |            |            | variable   |
+------------+------------+------------+------------+------------+
| Biomass    | **bd30to   | g m-2      | 1° grid,   | If a       |
| Density of | 90cm**     |            | annual     | demersal   |
| Medium     |            |            |            | species    |
| Demersals  |            |            |            | and L      |
| \>=30cm    |            |            |            | infinity   |
| and \<90cm |            |            |            | is \>=30   |
|            |            |            |            | cm and     |
|            |            |            |            | \<90cm,    |
|            |            |            |            | include in |
|            |            |            |            | this       |
|            |            |            |            | variable   |
+------------+------------+------------+------------+------------+
| Biomass    | **bd       | g m-2      | 1° grid,   | If a       |
| Density of | 90cm**     |            | annual     | demersal   |
| Large      |            |            |            | species    |
| Demersals  |            |            |            | and L      |
| \>=90cm    |            |            |            | infinity   |
|            |            |            |            | is         |
|            |            |            |            | \>=90cm,   |
|            |            |            |            | include in |
|            |            |            |            | this       |
|            |            |            |            | variable   |
+------------+------------+------------+------------+------------+
| Catch      | **cp       | g m-2      | 1° grid,   | Catch at   |
| Density of | 30cm**     |            | annual     | sea of     |
| Small      |            |            |            | pelagic    |
| Pelagics   |            |            |            | species    |
| \<30cm     |            |            |            | with L     |
|            |            |            |            | infinity   |
|            |            |            |            | \<30 cm    |
+------------+------------+------------+------------+------------+
| Catch      | **cp30to   | g m-2      | 1° grid,   | Catch at   |
| Density of | 90cm**     |            | annual     | sea of     |
| Medium     |            |            |            | pelagic    |
| Pelagics   |            |            |            | species    |
| \>=30cm    |            |            |            | with L     |
| and \<90cm |            |            |            | infinity   |
|            |            |            |            | \>=30 cm   |
|            |            |            |            | and \<90   |
|            |            |            |            | cm         |
+------------+------------+------------+------------+------------+
| Catch      | **cp       | g m-2      | 1° grid,   | Catch at   |
| Density of | 90cm**     |            | annual     | sea of     |
| Large      |            |            |            | pelagic    |
| Pelagics   |            |            |            | species    |
| \>=90cm    |            |            |            | with L     |
|            |            |            |            | infinity   |
|            |            |            |            | \>=90 cm   |
+------------+------------+------------+------------+------------+
| Catch      | **cd       | g m-2      | 1° grid,   | Catch at   |
| Density of | 30cm**     |            | annual     | sea of     |
| Small      |            |            |            | demersal   |
| Demersals  |            |            |            | species    |
| \<30cm     |            |            |            | with L     |
|            |            |            |            | infinity   |
|            |            |            |            | \<30 cm    |
+------------+------------+------------+------------+------------+
| Catch      | **cd30to   | g m-2      | 1° grid,   | Catch at   |
| Density of | 90cm**     |            | annual     | sea of     |
| Medium     |            |            |            | demersal   |
| Demersals  |            |            |            | species    |
| \>=30cm    |            |            |            | with L     |
| and \<90cm |            |            |            | infinity   |
|            |            |            |            | \>=30 cm   |
|            |            |            |            | and \<90   |
|            |            |            |            | cm         |
+------------+------------+------------+------------+------------+
| Catch      | **cd       | g m-2      | 1° grid,   | Catch at   |
| Density of | 90cm**     |            | annual     | sea of     |
| Large      |            |            |            | demersal   |
| Demersals  |            |            |            | species    |
| \>=90cm    |            |            |            | with L     |
|            |            |            |            | infinity   |
|            |            |            |            | \>=90 cm   |
+------------+------------+------------+------------+------------+

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
