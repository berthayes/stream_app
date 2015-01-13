This is Bert's Network Profiler App, designed to introduce operational visibility to wire data.

** IMPORTANT **
This app depends on the Splunk App for Stream to get its data:
https://apps.splunk.com/app/1809/

It relies on two internal lookup tables that you will want to populate.

$SPLUNK_HOME/etc/apps/network_profiler/lookups/homenet_hosts.csv
This is a .CSV table that maps MAC addresses to recognizable system names
This can be manually created/edited for smaller networks, or created automatically via CMDB lookup, etc.
This file should help you track hosts as they change IP addresses via DHCP over time.

$SPLUNK_HOME/etc/apps/network_profiler/lookups/nets.csv
This is a .CSV table that maps CIDR blocks to network owners.
Also editable by hand until some sort of whois->.csv python magic is crafted (or stolen)

README.txt continued on back -->
