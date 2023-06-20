## Model description

The model parameterizes interception, throughfall, canopy drip, snow
accumulation and melt, water transfer between snow layers, infiltration,
evaporation, surface runoff, sub-surface drainage, redistribution within
the soil column, and groundwater discharge and recharge to simulate
changes in canopy water $\Delta W_{can,\,liq}$, canopy snow water
$\Delta W_{can,\,sno}$ surface water $\Delta W_{sfc}$ ,
snow water $\Delta W_{sno}$ , soil water
$\Delta w_{liq,\, i}$ , and soil ice $\Delta w_{ice,\, i}$ ,
and water in the unconfined aquifer $\Delta W_{a}$  (all in kg
m$^{-2}$ or mm of H$_2$O).

The total water balance \eqref{eqn:h2o_budget} of the system is

\begin{multline}
  \label{eqn:h2o_budget}
  \Delta W_{can,\,liq} +\Delta W_{can,\,sno} +\Delta W_{sfc} +\Delta W_{sno} + \\
      \sum _{i=1}^{N_{levsoi} }\left(\Delta w_{liq,\, i} +\Delta w_{ice,\, i} \right)+\Delta W_{a} = \\
         \left(\begin{array}{l} {q_{rain} +q_{sno} -E_{v} -E_{g} -q_{over} } \\ 
         {-q_{h2osfc} -q_{drai} -q_{rgwl} -q_{snwcp,\, ice} } \end{array}\right) \Delta t
\end{multline}

where $q_{rain}$  is the liquid part of precipitation,
$q_{sno}$  is the solid part of precipitation,
$E_{v}$  is ET from vegetation,
$E_{g}$  is ground evaporation,
$q_{over}$  is surface runoff,
$q_{h2osfc}$  is runoff from surface water storage,
$q_{drai}$  is sub-surface drainage,
$q_{rgwl}$  and
$q_{snwcp,ice}$  are liquid and solid runoff from glaciers and lakes, and runoff from other surface types
due to snow capping
(all in kg m$^{-2}$ s$^{-1}$), $N_{levsoi}$  is the number of soil layers
(note that hydrology calculations are only done over soil layers 1 to
$N_{levsoi}$ ; ground levels $N_{levsoi} +1$ to
$N_{levgrnd}$ are currently hydrologically inactive;
and $\Delta t$ is the time step (s).

