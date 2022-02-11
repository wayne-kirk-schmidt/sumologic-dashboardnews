Sumo Dashboard News
===================

Ever wanted to be able to get your sumo Logic dashboard output, delivered where you want, when you want?
Sumo Dashboard News is here to help you do just that; deliver your Sumo Logic Newspaper to you.

We do this by using three APIs: Sumo Logic, Microsoft, and Google.

*     Sumo Logic - we extract the news you want, the news you need from your dashboards using the dashboard API
*     Microsoft - we create, page by page, your newspaper in Microsoft docx format
*     Google - we publish the report, and convert this into Google and PDF format

The result? The options and freedom to review your Dashboards when you want.

Use Cases
=========

Since we can schedule the Newspaper creation, and we have the freedom to include any Sumo Logic dashboard,
we can immediately accomplish the following:

*     archive dashboard output for compliance purposes
*     archive dashboard output for auditing purposes

And, since to can include any dashboard Sumo Logic can field, then you can provide compliance and audit for:

*     security
*     software delivery and deployment
*     site reliability
*     operational excellence
*     service level agreement compliance

Just to name a few areas of focus.

Installing the Scripts
=======================

The scripts are designed to be used within a batch script or DevOPs tool such as Chef or Ansible.
Each python3 script has complete list of python modules to aid people using a pip install.

You will need to use Python 3.6 or higher and the modules listed in the dependency section.  

The installation steps are as follows: 

    1. Download and install python 3.6 or higher from python.org. Append python3 to the LIB and PATH env.

    2. Download and install git for your platform if you don't already have it installed.
       It can be downloaded from https://git-scm.com/downloads
    
    3. Open a new shell/command prompt. It must be new since only a new shell will include the new python 
       path that was created in step 1. Cd to the folder where you want to install the scripts.
    
    4. Execute the following command to install pipenv, which will manage all of the library dependencies:
    
        sudo -H pip3 install pipenv 
 
    5. Clone this repository. This will create a new folder
    
    6. Change into this folder. Type the following to install all the package dependencies 
       (this may take a while as this downloads all of the libraries necessary):

        pipenv install
        
Dependencies
============

See the contents of "pipfile"

Script Names and Purposes
=========================

The scripts are organized into sub directories:

    1. ./bin - 
           ./bin/sumodashboardnews.py - this script drives the process to extract, build, and publish.

NOTE: this script required three items. 

    1. A Sumo API key name
    2. A Sumo API secret string 
    3. A Sumo Dashboard ID

NOTE: Please make sure that the ID that owns the API key also owns the dashboard you try to access

*   [Dashboard-Links](https://help.sumologic.com/Visualizations-and-Alerts/Dashboards/Get-Started-with-Dashboards-and-Panels/Add-a-Dashboard-Link)
*   [Manage-API-Keys](https://help.sumologic.com/Manage/Security/Access-Keys)

NOTE: Please make sure that the ID that owns the API key also owns the dashboard you try to access

RECOMMENDATION: A configuration file can provide these and the list of dashboards you want in your newspaper.

To Do List:
===========

License
=======

Copyright 2022 Wayne Kirk Schmidt

Licensed under the Apache 2.0 License (the "License");

You may not use this file except in compliance with the License.
You may obtain a copy of the License at

    license-name   APACHE 2.0
    license-url    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Support
=======

Feel free to e-mail issues to: 

- wschmidt@sumologic.com

- wayne.kirk.schmidt@gmail.com

I will provide "best effort" fixes and extend the scripts.
