# Week 9 Project: Honeypot

Time spent: >20 hours spent in total

> Objective: Learn about Network Security(NetSec) by attacking and being attacked vulnarable networked resources. For this purpose a basic honeypot will be stood up and its effectiveness at detecting and/or collecting data about an attack will be demonstrated.

### The Honeypot Built:
A honeypot is a decoy application, server, or other networked resource that intentionally exposes insecure features which, when exploited by an attacker, will reveal information about the methods, tools, and possibly even the identity of that attacker. For this assignment, Honeypot Dionaea over HTTP is deployed as mhn-honeypot-1. It is a honeypot used to trap malware samples.

In addition, Ubuntu-Snort as mhn-honeyport-3 is stood up.
> An overview of the steps taken includes;
> - Sign up for a Google cloud account
> - Install gcloud in the host machine so that gcloud command can be run from the host machine
> - Set up firewall rule for MHN Admin
> - Create MHN Admin VM and install MHN Admin Application. MHN supports multiple honeypots, each of which has a slightly different purpose. 
> - Create MHN Honeypot VM and install the honeypot application; deploy Dionaea over HTTP, a honeypot used to trap malware samples then wait to be attacked

### Issues Encountered:
The issue that most frequently faced is the session timeout while trying to install MHN admin application. The installation would go half way with some of the parameters set and halt in the middle giving me the message of connection time out. The next time the install command is run, the already set parameters would interfere with the new installations and give some error messageses including database error. The issue was resolved by removing VM instance from the Google cloud and everything else from the host including gcloud and redo the setup instructions again.

### GIF Walkthrough:
      ![GIF](https://github.com/shofi384/CSC.59938---Web-Security/blob/master/Week%239-ProjectHoneypot/week%239.gif)

### Summary of all the Attacks on all Honeypots: 
  ![Summary Statistics](https://github.com/shofi384/CSC.59938---Web-Security/blob/master/Week%239-ProjectHoneypot/summaryStat.jpg)


### [Exported Data](https://github.com/shofi384/CSC.59938---Web-Security/blob/master/Week%239-ProjectHoneypot/session.json)
