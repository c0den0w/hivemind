MID Server is a Java application that runs a Windows service or as a UNIX daemon. It is now necessarily a web server, such that it is not readily open to receive any HTTP requests. It is always connected to the ServiceNow instance and listening to the ECC queue for instructions.

It can act as an Orchestrator, with sufficient permissions can execute commands on a remote machine.

An extension can be added to the MID server for it to listen to external HTTP requests, this extensions starts a [[MID Web Server]]