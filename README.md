Big Data Product: Weapons and Drugs (Individual Work 70%)

In the television documentary “Ross Kemp and the Armed Police” broadcast 6th September 2018 by ITV, multiple claims were made regarding violent crime in the UK.

These claims were:
    1. Violent Crime is increasing
    2. There are more firearms incidents per head in Birmingham than anywhere else in the UK
    3. Crimes involving firearms are closely associated with drugs offences

In this assignment you will investigate these claims using real, publicly available data sets that will be made available to you and placed in Amazon S3. These include, but are not limited to:
    1. Street Level Crime Data published by the UK Home Office. This dataset contains 19 million data rows giving a crime type, together with their location as a latitude and longitude.
    2. Land Registry Price Paid Data: This gives the postcode of a property, the property type from an enumeration of D (Detached), S (Semi-Detached), T (Terraced), F (Flats/Maisonettes) and the price paid.
    3. Postcode Data: This data set is based on material provided by the Ordinance Survey. It gives a latitude and longitude to every postcode. This is useful as it relates between the Land Registry Price Paid dataset postcode, and the original crime dataset
latitude/longitude.


-----------------------------------------------------------
Dataset Details:
The Crimes Data:
The data were downloaded from https://data.police.uk/data/. This site offers data by month, and by force. Consequently, 
they have been merged into one file for this assignment. 

You can find out more about the data here (https://data.police.uk/about/#columns). Only ‘street’ files have been included. Outcomes are included.

The header row of the crimes data is:
'Crime ID', 'Month', 'Reported by', 'Falls within', 'Longitude', 'Latitude', 'Location', 
'LSOA code', 'LSOA name', 'Crime type', 'Last outcome category'

Note that Longitude and Latitude are anonymized as described on the police web site here: 
https://data.police.uk/about/#location-anonymisation. Since the police use around 750,000 'anonymous' 
map points it is unlikely that these coincide with the longitudes and latitudes given in the postcode dataset. 
For this reason, it is best to use LSOA (Lower Layer Super Output Area, UK Office for National Statistics) as a region indication. 

The file posttrans.csv will allow the translation of crimes’ longitude and latitude into actual postcodes.

Postcodes Data.
https://www.freemaptools.com/download-uk-postcode-lat-lng.htm

The headers of the postcodes.gz file are:
'Postcode','InUse?','Latitude','Longitude','Easting','Northing','GridRef','County','District','Ward','DistrictCode',
'WardCode','Country','CountyCode','Constituency','Introduced','Terminated','Parish','NationalPark','Population','Households',
'BuiltUpArea','Builtupsubdivision','Lowerlayersuperoutputarea','Rural/urban','Region','Altitude'
