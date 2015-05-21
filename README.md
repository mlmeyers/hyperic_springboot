## Hyperic HQ SpringBoot Plugin

This project is a Hyperic HQ plugin for monitoring [Springboot](http://http://projects.spring.io/spring-boot/)

Source code is available at [github.com/mlmeyers/hyperic_springboot](https://github.com/mlmeyers/hyperic_springboot)

### Platform Support

Only supports MongoDB running on Windows since it uses a powershell to invoke a rest request to collect the metrics from Actuator.

### Auto-Discovery

The SpringBoot server process (java.exe) is auto-discovered.

### Metrics

The following metrics are available:

* All actuator metrics 
* All server process (java.exe) metrics are also available - CPU Utilization, Resident Memory, etc.

### Log File Tracking

Messages are optionally reported from springboot.log and can be filtered by
regex include/exclude.

### Config File Tracking

The SpringBoot config file can be monitored for changes.

### Control Actions

None yet.

### Dependencies

Actuator enabled for SpringBoot Application +
Powershell scripts must enabled to run on the agents host - Set-ExecutionPolicy RemoteSigned +
Requires Powershell version 3+ on Agent Host  

### SpringBoot Version Support

Tested on Server 2012 R2 with SpringBoot 1.2

### Hyperic HQ Version Support

Tested with [Hyperic HQ](http://www.hyperic.com/) version 5.4.8

### Install

#### Server Installation
* Copy the file springboot-plugin.xml into the following folder under the server installation
<pre>
hq-plugins
</pre>

### Developers
To test any changes prior to deploying

    java -jar hq-pdk.jar -p springboot -t "SpringBoot 1.2" -m metric

### Author

Matthew Meyers :: meyers.matthew@gmail.com :: @mlmeyers
