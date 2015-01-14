This is Bert's Network Profiler App, designed to extend operational intelligence to wire data.

** IMPORTANT **
This app depends on the Splunk App for Stream to get its data:
https://apps.splunk.com/app/1809/

** ALSO IMPORTANT **
It relies on two internal lookup tables that you will need to populate.

$SPLUNK_HOME/etc/apps/network_profiler/lookups/homenet_hosts.csv
This is a .csv file that maps MAC addresses to recognizable system names.
This can be manually created/edited for smaller networks, or created automatically via CMDB lookup, etc.
Many of the dashboards and reports in this app will display hostnames from this file rather 
than IP or MAC addresses.
This file will need to be maintained as new systems are added to the network.


$SPLUNK_HOME/etc/apps/network_profiler/lookups/nets.csv
This is a .csv file that maps CIDR blocks to network owners.
Also editable by hand until some sort of whois->.csv python magic is crafted (or stolen)
This file will need to be maintained as you identify known networks over time.  


README.txt continued on back -->
