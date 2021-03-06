# Intro
NetWorkTrafficApp is a network traffic flow generator available from here . It can be used to generate bidirectional flows, where the first packet determines the forward (source to destination) and backward (destination to source) directions, hence the statistical time-related features can be calculated separately in the forward and backward directions. Additional functionalities include, selecting features from the list of existing features, adding new features, and controlling the duration of flow timeout.

NOTE: TCP flows are usually terminated upon connection teardown (by FIN packet) while UDP flows are terminated by a flow timeout. The flow timeout value can be assigned arbitrarily by the individual scheme e.g., 600 seconds for both TCP and UDP. In this version,we used jnetpcap1.4 to handle the memoery issue which is common on version 1.3.

--------------------------------------------------------------
# Installation and executing:

Extract CICFlowMeterV3.zip

___Note: The only prerequisite is that "libpcap" library or WinPcap on windows systems, be pre-installed___

For Linux

> $ sudo apt-get install libpcap-dev


For windows
> download [winpcap](<https://www.winpcap.org/install/default.htm>)

## executing
Go to the extracted folder and run this command:
```
//linux
sudo java -Djava.library.path="Your jnetpcap-linux folder path" -jar CICFlowMeterV3.jar
//windows
java -Djava.library.path="Your jnetpcap-win folder path" -jar CICFlowMeterV3.jar
```

Example for linux:
```
sudo java -Djava.library.path="/home/CIC/Desktop/jnetpcap" -jar CICFlowMeterV3.jar
```

## Get started
for offline
```
1.Select the folder that include your PCAP files
2.Select the folder that you would like to save you CSV files
3.Click OK button
```

for realtime
```
1 CLick Load button to find the list of network interfaces
2 Select the interface you would like to monitor
3 Click start button and wait for a while
4 Click stop button to stop the process and save the csv in same applcation folder/data/daily
```

--------------------------------------------------------------

Contact us at A.Habibi.L@unb.ca if there are any problems.


For citation in your works and also understanding CICFlowMeter (formerly ISCXFlowMeter) completely, you can find below published papers:

Arash Habibi Lashkari, Gerard Draper-Gil, Mohammad Saiful Islam Mamun and Ali A. Ghorbani, "Characterization of Tor Traffic Using Time Based Features", In the proceeding of the 3rd International Conference on Information System Security and Privacy, SCITEPRESS, Porto, Portugal, 2017

Gerard Drapper Gil, Arash Habibi Lashkari, Mohammad Mamun, Ali A. Ghorbani, "Characterization of Encrypted and VPN Traffic Using Time-Related Features", In Proceedings of the 2nd International Conference on Information Systems Security and Privacy(ICISSP 2016) , pages 407-414, Rome , Italy
