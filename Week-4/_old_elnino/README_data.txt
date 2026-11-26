# Week 4 Session 1 data provenance

## oni.csv
Source: NOAA CPC Oceanic Nino Index (ONI)
Raw: https://www.cpc.ncep.noaa.gov/data/indices/oni.ascii.txt
Converted from whitespace ascii to CSV. Columns: year, month (middle month of season), season, sst_c, oni
Public US government data.

## roni.csv
Source: NOAA CPC Relative Oceanic Nino Index (RONI)
Raw: https://www.cpc.ncep.noaa.gov/data/indices/RONI.ascii.txt
Columns: year, month, season, roni

## nigeria_city_rainfall_monthly.csv
Source: Open-Meteo Historical Weather API (CC BY 4.0)
Lagos (6.45, 3.39) and Kano (12.00, 8.52), daily precip summed to monthly, 1950-2025.
Attribution: Weather data by Open-Meteo.com
API: https://archive-api.open-meteo.com/v1/archive

## nigeria_staple_prices_monthly.csv / nigeria_north_staple_prices_monthly.csv
Source: WFP via HDX Nigeria food prices (CC BY-IGO)
Raw: https://data.humdata.org/dataset/wfp-food-prices-for-nigeria
Filtered to Rice (local), Millet, Sorghum; Retail; actual prices; converted to per-kg medians by year-month.
North file limits admin1 to northern states often discussed for El Nino dry-spell impacts.

## wfp_food_prices_nga.csv
Full raw WFP file (91k rows) kept for optional advanced filtering demos.
