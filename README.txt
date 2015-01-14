This is Bert's Network Profiler App, designed to extend operational intelligence to wire data.

** IMPORTANT **
This app depends on the Splunk App for Stream to get its data:
https://apps.splunk.com/app/1809/

** ALSO IMPORTANT **
It relies on two internal lookup tables that you will need to populate.

$SPLUNK_HOME/etc/apps/network_profiler/lookups/homenet_hosts.csv
	This is a .csv file that maps MAC addresses to recognizable system names.
	This can be manually created/edited for smaller networks, or created 
	automatically via CMDB lookup, etc.
	Many of the dashboards and reports in this app will display hostnames from this 
	file rather than IP or MAC addresses.
	This file is used by a saved search (hostmap_gen) that generates a lookup table 
	that lists MAC address, IP, and hostname.  By default, this search runs every 
	10 minutes so MAC,IP, andhostname pairings should always be pretty fresh.  If 
	you can't wait 10 minutes for this search to run on its own, you can run it 
	manually from Settings->Searches,Reports, and Alerts->hostmap_gen
	This file will need to be maintained as new systems are added to the network.


$SPLUNK_HOME/etc/apps/network_profiler/lookups/nets.csv
	This is a .csv file that maps CIDR blocks to network owners.
	Editable by hand until some sort of whois->.csv python magic is crafted 
	(or stolen)
	This file will need to be maintained as you identify known networks over time.  

This app was designed to monitor internal LAN traffic as it heads to a border gateway 
and the Internet beyond.  It also relies on DHCP traffic to map MAC addresses to IP 
addresses and system names, as well as to report on new/unseen systems.  If your border 
router is not also your DHCP server, you will want to watch the wire at two different 
locations.


README.txt continued on back -->
