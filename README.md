# hochbeet_SSD21
Tobias Gailhofer, 01629220
Daniela Hell, 11771845

Get started:

how to get software running:

Extract Zip File, run docker-compose on the .yml file, set up hardware with MQTT

get/post examples for testing with values:
 [GET]: tobias-network-storage.synology.me:1880/currentstate
 [GET]: tobias-network-storage.synology.me:1880/weather
 [GET]: tobias-network-storage.synology.me:1880/temperature
 [GET]: tobias-network-storage.synology.me:1880/airhumid
 [GET]: tobias-network-storage.synology.me:1880/soilhumid
 [GET]: tobias-network-storage.synology.me:1880/waterlevel
 [POST]: tobias-network-storage.synology.me:1880/watermanual/{duration}
 [POST]: tobias-network-storage.synology.me:1880/waterschedule/{mode}


we testet the post-examples with the help of swagger.io



Pitfalls:

changing from ZAMG to openweather - openweather provides an easy access to current weather situation,
which fits our needs much better

offering the user to choose between different schedule modes, instead of providing a pattern, so the user
needs so write in all informations about, which days, times, how long ect.... so it's easier
to use for the customer - now he can decide between different presceduled timetables
(and it's also easier to implement ;) )

choose database - decision for influxDB: safes data for free for a amount of 30 days
and safes them with a timestamp - so perfect for our application

choosing grafana to represent the data, safed in the database, so we can show the user
a proper timeline of all parameters like temperature, humidity of raised bed and so on...
