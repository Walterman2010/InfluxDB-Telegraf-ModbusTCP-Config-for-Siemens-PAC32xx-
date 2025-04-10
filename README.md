# ModbusTCP - Telegraf Integration for Siemens Senctron PAC3200 and PAC3220

Here you can find the ModbusTCP plugin for telegraf, to get the Enerymeasurement in the InfluxDB.
sorry the variablenames are in german...

the Configurations are nearly simuarl

 Activate the ModbusTCP on the Mesurement Device and Add it to Conroller
 controller = "tcp://xxx.xxx.xxx.xxx:502" 

# PAC3200
 You can finde the information about in PAC 3200 in the handbook, its interressting a round page 38 following
DE: https://cache.industry.siemens.com/dl/files/150/26504150/att_906559/v1/A5E01168664A-04_DE_122016_201612221316291494.pdf
EN: https://cache.industry.siemens.com/dl/files/150/26504150/att_906558/v1/A5E01168664B-04_EN-US_122016_201612221316360495.pdf
# PAC3220
 You can finde the information about in PAC 3220 in the handbook, its interressting a round page 113 following
DE: https://cache.industry.siemens.com/dl/files/307/109767307/att_984482/v1/MAN_L1V30425208E-01_de_de-DE.pdf
EN: https://cache.industry.siemens.com/dl/files/307/109767307/att_1298442/v1/MAN_L1V30425208F_RS-AA_002_en_en-US.pdf

 Holding Register:
 measurement: the Name of your Device. it is the name, how you can find it in the InfluxDB as measurement
 name: the name of the Physical Mesurementvalue (in this case in German). seh in the Handbook for more informations
 byte_order: sayed how are the Value ar stored in the adress (and also the Sice)
 data_type: depent what type of value it is. The most types are a kind off Real or floats also FLOAT32-IEEE
 scale: say something about the commerposition
 address: where it is stored. in the Document is only given the start adress and the number oh registers. in the most cases there are 2 registes, also we need to add the following register the the adress
