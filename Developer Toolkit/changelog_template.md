# Changelog [EXAMPLE TO CREATE AND USE BY HELK EXAMPLE]

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Alpha] Version 0.0.0-00000000

### [0.00.5] - 2022-06-05 - Changed
 - [BUG] #000
  - [PR] !000

### [0.00.0] - 2022-05-06 - Added
- [US] #000
  - [PR] !000

***

[Full Changelog](https://github.com/Cyb3rWard0g/HELK/compare/v0.1.6-alpha12132018...v0.1.7-alpha02242019)

### Fixed:
**Jupyter [Docker]**
* Access and modification of notebooks by [@TheComitre](insert_github_link_perfil)

**KSQL [Docker]**
* KSQL Commands for Sysmon JOIN recipe

**Nginx [Docker]**
* Updated proxy config to handle SSL better and not block internal HELK files from users

**Logstash [Docker]**
* For builds with elastic trial subscription, I had to move the logstash config out of volumes and add it manually to the docker container to avoid access and read issues from logstash container to local file.

### Added:
**Logstash [Docker]**
* Osquery Filebeat Output by [@TheComitre](insert_github_link_perfil)
* Additional awesome sauce provided by [@neu5ron](https://twitter.com/neu5ron) in details [here](https://blog.neu5ron.com/2019/02/what-in-helk-release.html)

**Kafka [Docker]**
* Osquery Filebeat Topic by [@rrcyrus](https://twitter.com/rrcyrus)
* win_security topic to get win security events parsed back
* win_sysmon topic to get win sysmon events parsed back

**Jupyter [Docker]**
* jupyterlab-manager widgets
* Python package Keras 2.2.4
* Python package s3sf 0.2.0

**Kibana [Docker]**
* Additional awesome sauce provided by [@neu5ron](https://twitter.com/neu5ron) in details [here](https://blog.neu5ron.com/2019/02/what-in-helk-release.html)

### Updated:

**Jupyter [Docker]**

* ES-Hadoop version to 6.6.1
* Notebooks for intro to pandas and python
* Notebooks for intro to Spark SQL via Pyspark
* Notebooks for intro to Spark SQL via Pyspark and Sysmon
* python package altair to 2.4.1
* python package pandas to 0.24.1
* Docker Image to 0.1.1

**ELK Stack [Docker]**
* Version 6.6.1
* Consolidated 
* Additional awesome sauce provided by [@neu5ron](https://twitter.com/neu5ron) in details [here](https://blog.neu5ron.com/2019/02/what-in-helk-release.html)

**helk_install [Docker]**
* Downloads docker via https by [tifkin_](https://twitter.com/tifkin_)
* Additional awesome sauce provided by [@neu5ron](https://twitter.com/neu5ron) in details [here](https://blog.neu5ron.com/2019/02/what-in-helk-release.html)

**helk_update [Docker]**
* Update handling improved by [TheComitre](insert_github_link_perfil)

***
