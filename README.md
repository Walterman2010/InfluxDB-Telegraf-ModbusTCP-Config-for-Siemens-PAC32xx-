# Modbus Integration for Siemens PAC3200 and PAC3220

the Configurations are nearly simuarl

 Activate the ModbusTCP on the Mesurement Device and Add it to Conroller
 controller = "tcp://xxx.xxx.xxx.xxx:502" 
 You can finde the information about in PAC 3200 in the handbook, its interressting at page 38 following
 https://cache.industry.siemens.com/dl/files/150/26504150/att_906559/v1/A5E01168664A-04_DE_122016_201612221316291494.pdf

 Holding Register:
 measurement: the Name of your Device. it is the name, how you can find it in the InfluxDB as measurement
 name: the name of the Physical Mesurementvalue (in this case in German). seh in the Handbook for more informations
 byte_order: sayed how are the Value ar stored in the adress (and also the Sice)
 data_type: depent what type of value it is. The most types are a kind off Real or floats also FLOAT32-IEEE
 scale: say something about the commerposition
 address: where it is stored. in the Document is only given the start adress and the number oh registers. in the most cases there are 2 registes, also we need to add the following register the the adress
