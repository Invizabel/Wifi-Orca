# Wifi Orca contains free and open source tools!
# 
# requirements:
# * iw (linux package)
# * linux
# * monitor mode
# * nmap (linux package)
# * root privileges
# * sqlmap
# * TheSilent
# 
# client usage:
# python3 -m WifiOrca.main
# make sure to have the server.txt file present in the same directory as WifiOrca for the packet_fox_client.py script to work
# make sure to have the mode.txt file present in the same directory as WifiOrca for the packet_fox_client.py script to work
# make sure to have the ports.txt file present in the same directory as WifiOrca for the packet_fox_client.py script to work
# make sure to have the payloads.txt file present in the same directory as WifiOrca for the packet_fox_client.py script to work
# 
# main client start at boot:
# On linux in a terminal:
# crontab -e
# then add the following to the file:
# @reboot /usr/bin/python3 path/to/WifiOrca/main.py
# 
# packet fox server:
# import WifiOrca.packet_fox_server
# 
# packet fox modes:
# 0 | off | lan_sniff
# 1 | internal to internal | lan_sniff
# 2 | internal to external but not internal to internal | lan_sniff
# 3 | all | lan_sniff
# 
# packet fox ports:
# ports must be separated by new lines
# only one port per line
# use "all" if you don't care what ports are recorded
# 
# packet fox recommended ports for red team assessments:
# 20,21,23,25,53,67,68,80- clear text
# 1194,1725,9050,19132,19133- potential policy violation
# 
# packet fox payloads:
# 01 | lan only
# 10 | wlan only
# 11 | both lan and wlan
# 
# venv:
# $ sudo python3 -m venv WifiOrca
# $ source WifiOrca/bin/activate
# $ sudo pip3 install WifiOrca
# 
# Notes:
# openwrt currently doesn't support venv
# WifiOrca will automatically detect interfaces and assign them accordingly
# 
# todo
# add interface manual override
