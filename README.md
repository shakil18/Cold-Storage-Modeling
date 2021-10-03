
## Table of Contents

- [Cold Storage Modeling <a name = "about_the_project"></a>](#online-inventory-system-)
  - [System Overview <a name = "overview"></a>](#overview-)
  - [Requirements <a name = "requirements"></a>](#requirements-)
  - [Contact <a name = "contact"></a>](#contact-)
---

<!-- ABOUT THE PROJECT -->
# Cold Storage Modeling <a name = "about_the_project"></a>

"Cold Storage"- It is a type of storage in which the stored information is required less often. This “cold data” is stored long-term and access requires a large amount of time. Depending on the area of ​​application, storage media are used that are optimized for long storage times, high storage volumes, long service lives and low costs. The data in such a memory is only accessed after months or years, for example.

This project is about to find the probability of a file that the file will survive one year if the repair rates for disks and data-center (dc) gone through a certain time frame. The system model using PRISM tool a file stored persistently by sharding it between 4 data centers using 3/4 coding and each shard should be stored locally in each datacenter sharded using 17/20 coding.

Calculate the file availability i.e., the probability that the file will survive one year, if the repair rates for disks and dc are respectively:
* 1 week, 1 week
* 1 week, 1 day
* 1 day, 1 week
* 1 day, 1 day.

- the file is not replicated and only one copy exists.
- the file is durable if maximum one data center fails --> (failedDC<=1)


<!-- OVERVIEW  -->
## System Overview <a name = "overview"></a>

**Input Model**

Datacenter: 
- fails at rate of dcFR = 0.01% 
- repairs at rate of dcRR.

Disk: 
- fails at rate of diskFR = 5%.
- repairs at rate of diskRR.

Time frame = 1 year


<!-- REQUIREMENTS  -->
## Requirements <a name = "requirements"></a>

- [JavaSE >= 7 <a href="https://docs.oracle.com/javase/8/docs/technotes/guides/install/install_overview.html"> </a>](php_download)
- C/C++ compiler
- [PRISM](http://www.prismmodelchecker.org/manual/InstallingPRISM/Instructions)
- Required files:
	+ model.prism  >  the ctmc model code
	+ props.csl    >  the property to calculate the availability 
	+ ctmc.pdf     >  the ctmc state diagram
	+ 1d1d.txt     >  availability when diskRR=1 day and dcRR=1 day
	+ 1d1w.txt     >  availability when diskRR=1 day and dcRR=1 week
	+ 1w1d.txt     >  availability when diskRR=1 week and dcRR=1 day
	+ 1w1w.txt     >  availability when diskRR=1 week and dcRR=1 week


<!-- CONTACT -->
## Contact <a name = "contact"></a>

**Azizul Hakim Shakil** - [@ShakilAzizul](https://twitter.com/ShakilAzizul) - azizulhakim.shakil18@gmail.com

Project Link: [https://github.com/shakil18/Cold-Storage-Modeling](https://github.com/shakil18/Cold-Storage-Modeling)
