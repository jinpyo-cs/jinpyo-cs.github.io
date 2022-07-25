---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* B.S. in Computer Science and Engineering, Sogang University, 2014
* M.S. in Computer Science and Engineering, Sogang University, 2016

Work experience
======
* Feb. 2017: Senior Embedded Software Engineer
  * SK Hynix Inc.
  * Duties included: SSD (Solid-State Drive) Firmware development
  * Supervisor: Dr. Dony young Seo
   
* Feb. 2016: Junior Embedded Software Engineer
  * SK Hynix Inc.
  * Duties included: SSD Firmware Performance Analysis
  * Supervisor: Technical Leader Beom Ju Shin
  
* Feb. 2014: Research Assistant
  * Sogang University
  * Duties included: Circuit Simulation Analysis related to Process Variation
  * Supervisor: Professor. Juho Kim
  
Skills
======
* Programming Languages : C, C++, Python, Java, UNIX shell
* Platform : Windows XP/7/8/10, Linux, UNIX
* Debugger : TRACE32 (hardware debugger for embedded systems such as ARM achitecture)

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Patents
======
* US10860227B2 (granted): changes NAND flash program level (SLC, MLC, TLC) based on surrounding environment-sensing data
* US20200126624A1 (granted): determines to remove victim block based on erase count
* US20220050604A1 (granted): provides improved security of storage device by position information generator
* US11269528B2 (granted): reduces internal read by using Host read cmd
* US20220206706A1 (pending): avoids free block shortage during boot up
* US20210133058A1 (pending): minimize power off operation related to read count table of FTL
* US20220043601A1 (pending): changes FTL meta page layout for shutdown process
* US20220171542A1 (pending): compares ages between meta block and PLP block for determining perform recovery operation
* US20220179573A1 (granted): manages two level structure for reducing DRAM access
