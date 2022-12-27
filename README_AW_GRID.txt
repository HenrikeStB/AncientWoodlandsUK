#
################################################################################################
#											       #
# 	Dataset: Climate change and edge effects affecting ancient woodlands in the UK (grid)  #
#											       #
# 	Author: Henrike Schulte to Bühne (henrike.schultetobuhne@ioz.ac.uk)                    #
#											       #
# 	Current version: 22/12/2022                                                            #
#											       #
################################################################################################
#
# This project was funded by the Woodland Trust.
# This dataset contains information on (1) current exposure of ancient woodlands to edge effects and (2) predicted risks from climate change to ancient woodlands in the UK.
# Each grid cell (12 km by 12 km) contains data averaged over all ancient woodlands contained in the gridcell.
# Data for individual ancient woodlands can be obtained from Henrike Schulte to Bühne (henrike.schultetobuhne@ioz.ac.uk).
#
#
#
##################################################
#					         #
#~~~~~~~~~~~~ Description of dataset ~~~~~~~~~~~~#
#					         #
##################################################
#
# AREA_HA: 	Area (ha) of all ancient woodlands contained in the grid cell
# ANY: 		Area (ha) of ancient woodland within 100 m of any non-woodland land cover
# PR_ANY: 	Ancient woodland area within 100 m of any non-woodland land cover as proportion of total ancient woodland area in the grid cell.
# CORE: 	Area (ha) of ancient woodland that is *NOT* within 100 m of any non-woodland land cover
# PR_CORE:    	Ancient woodland area that is *NOT* within 100 m of any non-woodland land cover as proportion of total ancient woodland area in the grid cell (inverse of PR_ANY)
# INT: 		Area (ha) of ancient woodland within 100 m of any intensive land use (urban and suburban areas, arable and horticulture, improved grasslands)
# PR_INT:	Ancient woodland area within 100 m of any intensive land use as proportion of total ancient woodland area in the grid cell.
​# OPEN: 	Area (ha) of ancient woodland within 100 m of any semi-natural, non-woodland land cover (e.g. grassland, heath, water)
# PR_OPEN: 	Ancient woodland area within 100 m of any semi-natural, non-woodland land cover as proportion of total ancient woodland area in the grid cell.
# FLAMM:	Area (ha) of ancient woodland within 100 m of any highly flammable non-woodland land cover (urban and suburban, arable and horticulture, heathland, grassland)
# PR_FLAMM:	Ancient woodland area within 100 m of any highly flammable land cover as proportion of total ancient woodland area in the grid cell.
# HABSUIT: 	Expected change in the proportion of tree species for which the climatic conditions will no longer be suitable by the end of the century (average for all ancient woodlands in a grid cell). The dataset underlying this does not contain habitat suitability for all British tree species, so it can only give a relative indication of how many tree species may struggle to persist in a given location.
# DROUGHT:	Expected change in the number of total drought months from the present (2001-2020) to the future (2061-2080) (average for all ancient woodlands in a grid cell). The 1975/76 drought in Great Britain is taken as a benchmark for what constitutes an extreme drought.
# FIRE: 	Expected change in the annual number of days with very high fire risk from the present (1991-2020) to the future (2061-2090)(average for all ancient woodlands in a grid cell). Fire risk was based on the Met Office Fire Severity Index.
# STORM:	Expected change in the severity of storms (99th percentile daily wind speed) between 2000-2020 and 2060-2080 (average for all ancient woodlands in a grid cell)
# FLOOD: 	Expected change in return frequencies of river floods between 1971-2000 and 2071-2100 (average for all ancient woodlands in a grid cell) (in years)
# CC:		Average climate change risk for all ancient woodlands in a grid cell. Climate change risk was calculated as the mean of HABSUIT, DROUGHT, FIRE, STORM, FLOOD (after rescaling to [0, 1]). Can vary between 0 (no risk) to 1 (highest risk observed across UK).
# R_CC: 	Average climate change risk rank for all ancient woodlands in a grid cell. Varies from 1 (lowest risk rank) to 10 (highest risk rank).
#
#
#
#
########################################
#                                      #
#~~~~~~~~~~~~ Data sources ~~~~~~~~~~~~#
#                                      #
########################################
#
#### Ancient woodland boundaries in England: 
#### Natural England. Available at https://www.data.gov.uk/dataset/9461f463-c363-4309-ae77-fdcd7e9df7d3/ancient-woodland-england. Natural England copyright. Contains Ordnance Survey data © Crown copyright and database right [2022]. Published under an Open Government License (https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
#
#### Ancient woodland boundaries in Scotland: 
#### Scottish Government. Available at https://www.data.gov.uk/dataset/c2f57ed9-5601-4864-af5f-a6e73e977f54/ancient-woodland-inventory-scotland. Copyright Scottish Natural Heritage. Contains Ordnance Survey data © Crown copyright and database right (2022)
#
#### Ancient woodland boundaries in Wales: 
#### Natural Resources Wales. Available at http://lle.gov.wales/catalogue/item/AncientWoodlandInventory2021/. Contains Natural Resources Wales information © Natural Resources Wales and Database Right. All rights Reserved. Contains Ordnance Survey Data. Ordnance Survey Licence number 100019741. Crown Copyright and Database Right.
#
#### Ancient woodland boundaries in Northern Ireland: 
#### Pers. comm, Woodland Trust.
#
#### Land cover: 
#### Morton, R.D.; Marston, C.G.; O’Neil, A.W.; Rowland, C.S. (2021). Land Cover Map 2020 (25m rasterised land parcels, GB). NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/6c22cf6e-b224-414e-aa85-900325baedbd.
#
#### Habitat suitability: 
#### Derived from Mauri, A., Girardello, M., Strona, G., Beck, P.S., Forzieri, G., Caudullo, G., Manca, F. & Cescatti, A. (2022) EU-Trees4F, a dataset on the future distribution of European tree species. Scientific data, 9(1), pp.1-12.
#
#### Drought: Derived from Robinson, E.L.; Kay, A.L.; Brown, M.; Chapman, R.; Bell, V.A.; Blyth, E.M. (2021) Potential evapotranspiration derived from the UK Climate Projections 2018 Regional Climate Model ensemble 1980-2080 (Hydro-PE UKCP18 RCM). NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/eb5d9dc4-13bb-44c7-9bf8-c5980fcf52a4 and Met Office Hadley Centre (2018) UKCP18 Regional Projections on a 12km grid over the UK for 1980-2080. Centre for Environmental Data Analysis, 15/06/2022. https://catalogue.ceda.ac.uk/uuid/589211abeb844070a95d061c8cc7f604
#
#### Fire: 
#### Derived from Arnell, N.W., Freeman, A. and Gazzard, R., 2021. The effect of climate change on indicators of fire danger in the UK. Environmental Research Letters, 16(4), p.044027. Available at https://uk-cri.org/ under a Creative Commons Attribution 4.0 International License.
#
#### Storms:
#### Derived from Met Office Hadley Centre (2018) UKCP18 Regional Projections on a 12km grid over the UK for 1980-2080. Centre for Environmental Data Analysis, 15/06/2022. https://catalogue.ceda.ac.uk/uuid/589211abeb844070a95d061c8cc7f604
#
#### Flood:
#### Derived from Paprotny, D. & Morales Nápoles, O. (2016) Pan-European data sets of river flood probability of occurrence under present and future climate. 4TU.ResearchData. Dataset. https://doi.org/10.4121/uuid:968098ce-afe1-4b21-a509-dedaf9bf4bd5 
#
#
#
#
##################################################
#~~~~~~~~~~~~~~~~~~~~~~ END ~~~~~~~~~~~~~~~~~~~~~#
##################################################
