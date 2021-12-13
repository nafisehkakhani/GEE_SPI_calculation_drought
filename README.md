# GEE_SPI_calculation_drought
Simple handy script for SPI calculation via Google Earth Engine.

The goal of this process is to build a standardized precipitation index (SPI) timeline using daily CHIRPS data. The SPI is utilized because it exposes differences in mean precipitation over a period of time and so offers information on drought-like situations. The script will run in the Google Earth Engine and will perform two separate SPI computations. The "common" SPI is calculated over a period of n months in the first computation. A SPI calculated for one month is commonly referred to as "SPI-1," for six months as "SPI-6," and so on. The second SPI computation is based on the dates of MODIS acquisition. Because MODIS collects data on vegetation, it may be interesting to compare its vegetation indices to the SPI. As a result, a 16-day SPI is calculated, with the same start date as MODIS.

This code aims to calculate SPI for 3 provinces in Iran: Esfahan, Fars and Khuzestan.
if you want to change the location, you just have to alter these lines:

var Provinces = admin2.filter(ee.Filter.or(
  ee.Filter.eq('ADM1_NAME', 'Esfahan'),
  ee.Filter.eq('ADM1_NAME', 'Khuzestan'),
  ee.Filter.eq('ADM1_NAME', 'Fars')))
  
  for any futhure question please contact me at: nkakhani@mail.kntu.ac.ir
  
  Note: This code is basically inspired from UN-SPIDER recomandation approaches for disaster management. 
  
