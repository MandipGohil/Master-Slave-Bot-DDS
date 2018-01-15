Build a Master and Slave Bot capable of generating distributed denial of service attacks on command
from the Bot Master.

Programming Language to use: Java 8
This work will be part of a larger semester long project so try to build the software in an extensible
manner. You will write Bot Master (MasterBot.java) and provide the code for the slaves (SlaveBot.java)
to be commanded by the Bot Master. The master, when started, will present a command line interface
to the user like that provided by the shell in Unix (i.e. present prompt ‘>’). The following commands are
to be supported:
(DO NOT INCLUDE THE HYPEN IN YOUR COMMANFD SYNTAX, ONLY THE COMMAND: i.e. list)

1.-list
Will list all current slaves with the following format:
SlaveHostName IPAddress SourcePortNumber RegistrationDate
USE THE FOLLOWING FORMAT FOR THE DATE: YYYY-MM-DD
Where YYYY is a four digit year, MM is a two digit month, and DD is a two digit day.

2.-connect (IPAddressOrHostNameOfYourSlave|all) (TargetHostName|IPAddress) TargetPortNumber
[NumberOfConnections: 1 if not specified]
Establish a number of connections to the target host.

3.-disconnect (IPAddressOrHostNameOfYourSlave|all) (TargetHostName|IPAddress) [TargetPort:all if
no port specified]
Close a number of connections to a given host
Any violation of name or formatting specified in this document will result in zero grade.

Your program must run via command line execution.
Master will take the following command line argument:
-p PortNumber
This will be the port where master will listen for incoming connections from Slaves.
Slave will take two arguments:
-h IPAddress|Hostname (of Master -p port where master is listening for connections

4.-connect (IPAddressOrHostNameOfYourSlave|all) (TargetHostName|IPAddress) TargetPortNumber [NumberOfConnections: 1 if not 
specified] 
[keepalive] When the keepalive option is given, your client should select that socket option while creating the related 
connection. 

5.- connect (IPAddressOrHostNameOfYourSlave|all) (TargetHostName|IPAddress) TargetPortNumber [NumberOfConnections: 1 if not 
specified] [url=path-to-be-provided-to-web-server]
As an example, if you select to attack the Google search engine you will use:
url=/#q=
The slave will generate a HTTP request equivalent to: https://www.google.com/#q=YourRandomString
Your client must also clean up data provided by the server response. The length of the string being added to the should also be generated at random between 1 char and 10 chars.
