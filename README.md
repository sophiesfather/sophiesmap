sophiesmap
==========
The present source represents an alexa skill with a lambda endpoint written in nodejs that queries a local tasmota sensor based on a sonoff device via REST and subsequently speaks out the sensor's value, the temperature in my case.
In order to get it running, you have to write an alexa custom skill (within the browser ide of aws) and paste my code over the template files.
The archticture is straight forward w/o using mqtt or any local webserver. Just a plain home equiment, i.e. router and tasmota sensor device is needed (and an alexa device, of course).
You need configure your router with dyndns in order to let aws/alexa perform a REST call into your network, in order to retrieve the temperature from the sensor (see index.js).
(I am using the AVM FRITZ dyndns service of my router's manufacturer which is traight forward).

The present solution requires you to modify the index.js file, i.e. insert the address of your router into index.js. 
