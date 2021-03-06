<div align="center">
	<img src=".github/logo-w-title.png" width="256">
</div>

---

<h4 align="center">
	A data mining suite for DNA microarrays
</h4>

<p align="center">
	<!--<a href="https://travis-ci.org/HelikarLab/candis">
        <img src="https://img.shields.io/travis/HelikarLab/candis.svg?style=flat-square">
    </a>-->
	<a href="http://candis.readthedocs.io">
		<img src="https://readthedocs.org/projects/candis/badge/?version=latest"/>
	</a>
	<a href="https://saythanks.io/to/achillesrasquinha">
		<img src="https://img.shields.io/badge/Say%20Thanks-🦉-1EAEDB.svg?style=flat-square">
	</a>
	<a href="https://paypal.me/achillesrasquinha">
		<img src="https://img.shields.io/badge/donate-💵-f44336.svg?style=flat-square">
	</a>
</p>

<div align="center">
	<img src=".github/sample.gif" height>
</div>

**candis** is an open source data mining suite (released under the [GNU General Public License v3](LICENSE)) for DNA microarrays that consists of a wide collection of tools you require, right from Data Extraction to Model Deployment. 
**candis** is written by the bioinformaticians at [HelikarLab](http://www.helikarlab.org).

***WARNING***: candis currently is still in `dev` mode and not production-ready yet. In case if you run across bugs or errors, raise an issue over [here](https://github.com/HelikarLab/candis/issues).

### Table of Contents
* [Installation](#installation)
* [Run](#run)
* [Launch](#launch)
* [Dependencies](#dependencies)
* [Usage](#usage)
* [Features](#features)
* [Team](#team)
* [License](#license)

### Installation
```console
$ sudo pip3 install candis
```
#### For Mac OS X (Tested on MacOS Sierra 10.12.6) and Linux OS (Tested on Ubuntu 16.04)

### Run
```console
$ python3 -m candis
```

### Launch
#### [localhost:5000](http://localhost:5000)

* Please make sure that you are using an open port number as shown in the terminal when you execute the program in the above step.
* Store your high-throughput input data (microarray CEL files) in CRES folder on your local machine that will be accessible from candis application on localhost.
* Sample CEL files can be found [here](https://github.com/HelikarLab/CancerDiscover/tree/master/SampleData).

### Dependencies
* Production Dependencies
	* PIP3 [PIP3](https://pip.pypa.io) (Python's Package Manager)
	```console
	sudo apt-get update && sudo apt-get install python3-pip
	```
	* Numpy
	```console
	sudo apt-get install python3-numpy
	```
	* R 3.3+
	```console
	sudo apt install r-base-core
	sudo apt-get install software-properties-common python-software-properties
	sudo add-apt-repository ppa:marutter/rrutter
	sudo apt update && sudo apt full-upgrade
	```
	* Java
	```console
	sudo apt-get install openjdk-8-jdk
	sudo add-apt-repository ppa:webupd8team/java
	```
	* Python 3.6+
	* Graphviz
	```console
	sudo apt-get install graphviz libgraphviz-dev graphviz-dev pkg-config
	```
* Development Dependencies
	* [Node.js](https://nodejs.org)
	* [SASS](http://sass-lang.com)
	
To install candis right from scratch, check out our exhaustive guides:
* [A Hitchhiker's Guide to Installing candis on Mac OS X](https://github.com/HelikarLab/candis/wiki/A-Hitchhiker's-Guide-to-Installing-candis-on-Mac-OS-X)
* [A Hitchhiker's Guide to Installing candis on Linux OS](https://github.com/HelikarLab/candis/wiki/A-Hitchhiker's-Guide-to-Installing-candis-on-Linux-OS) (In Progress)
* [A Hitchhiker's Guide to Installing candis on Windows OS](https://github.com/HelikarLab/candis/wiki/A-Hitchhiker's-Guide-to-Installing-candis-on-Windows-OS) (Contributors Wanted)

### Usage
**Using the CLI (Command Line Interface)**

```
$ candis --cdata path/to/data.cdata --config path/to/config.json
```

### Features
* Converting a CDATA to an **ARFF** file

	```python
	>>> import candis
	>>> cdata = candis.cdata.read('path/to/data.cdata')
	```

	Then, simply use the `CData.toARFF` API:

	```python
	>>> cdata.toARFF('path/to/data.arff')
	```

* Running a `Pipeline`.
	```python
	>>> pipe = candis.Pipeline()
	>>> pipe.run(cdata)
	>>> while pipe.status == candis.Pipeline.RUNNING:
	...     # do something while pipeline is running
	```

### Team
<table align="center">
  <tbody>
    <tr>
		<td align="center" valign="top">
			<img height="150" src="http://newsroom.unl.edu/announce/files/file37859.jpg">
			<br>
			<a href="http://helikarlab.org/members.html">Dr. Tomas Helikar, Ph.D</a>
			<br>
			<a href="mailto:thelikar2@unl.edu">thelikar2@unl.edu</a>
			<br>
			<p>Principal Investigator</p>
		</td>
		<td align="center" valign="top">
			<img height="150" src="https://github.com/akram-mohammed.png?s=150">
			<br>
			<a href="https://github.com/akram-mohammed">Dr. Akram Mohammed, Ph.D</a>
			<br>
			<a href="mailto:amohammed3@unl.edu">amohammed3@unl.edu</a>
			<br>
			<p>Author and Maintainer</p>
		</td>
	 	<td align="center" valign="top">
			<img width="150" height="150" src="https://github.com/achillesrasquinha.png?s=150">
			<br>
			<a href="https://github.com/achillesrasquinha">Achilles Rasquinha</a>
			<br>
			<a href="mailto:achillesrasquinha@gmail.com">achillesrasquinha@gmail.com</a>
			<br>
			<p>Author and Maintainer</p>
    	</td>
     </tr>
  </tbody>
</table>

### License
This software has been released under the [GNU General Public License v3](LICENSE).
