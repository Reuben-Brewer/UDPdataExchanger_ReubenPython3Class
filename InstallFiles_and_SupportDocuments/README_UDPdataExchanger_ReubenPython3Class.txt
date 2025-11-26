########################  

UDPdataExchanger_ReubenPython3Class

A class for transferring data between programs via UDP. Includes optional Tkinter GUI interface.

Reuben Brewer, Ph.D.

reuben.brewer@gmail.com

www.reubotics.com

Apache 2 License

Software Revision F, 11/20/2025

Verified working on: 
Python 3.12

Windows 11 64-bit

Note: If you have trouble getting the UDP communication to work, two simpler, "BareBones", examples have been include:
Rx_BareBonesUDPtest_ReubenPython3.py and Tx_BareBonesUDPtest_ReubenPython3.py

########################  

########################### Python module installation instructions, all OS's

UDPdataExchanger_ReubenPython3Class, ListOfModuleDependencies: ['LowPassFilterForDictsOfLists_ReubenPython2and3Class']

UDPdataExchanger_ReubenPython3Class, ListOfModuleDependencies_TestProgram: ['CSVdataLogger_ReubenPython3Class', 'keyboard', 'MyPlotterPureTkinterStandAloneProcess_ReubenPython2and3Class', 'MyPrint_ReubenPython2and3Class']

UDPdataExchanger_ReubenPython3Class, ListOfModuleDependencies_NestedLayers: ['future.builtins', 'LowPassFilter_ReubenPython2and3Class', 'numpy', 'pexpect', 'psutil']

UDPdataExchanger_ReubenPython3Class, ListOfModuleDependencies_All:['CSVdataLogger_ReubenPython3Class', 'future.builtins', 'keyboard', 'LowPassFilter_ReubenPython2and3Class', 'LowPassFilterForDictsOfLists_ReubenPython2and3Class', 'MyPlotterPureTkinterStandAloneProcess_ReubenPython2and3Class', 'MyPrint_ReubenPython2and3Class', 'numpy', 'pexpect', 'psutil']

###########################

###########################

In Raspberry Pi (tested 12/27/24 on 4B model running Buster):

Edit this file:
sudo gedit /etc/dhcpcd.conf

Add these lines:

interface eth0
static ip_address=192.168.1.88/24
static routers=192.168.1.1
static domain_name_servers=8.8.8.8
metric 300

#Gets IPV4 settings automatically from DHCPCD, lower metric tells Pi to prioritize eth0
#interface wlan0 DOESN'T WORK
#metric 200 DOESN'T WORK

#CRITICAL LINE
noipv4ll

###########################