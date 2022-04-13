Sumo Logic Backup
=================

In the age of DevOps, why not treat your Sumo Logic content as code?

These tools enable you to extract content supporting a Dev Ops mindset.

Installing the Scripts
=======================

The scripts are CLI based, designed as a stand alone CLI or incorporated in a DevOPs tool such as Chef or Ansible.

Written in python3, all scripts are listed below, and there is a Pipfile to show what modules are required to run.

You will need to use Python 3.6 or higher and the modules listed in the dependency section.  

Please follow the following steps to install:

    1. Download and install python 3.6 or higher from python.org. Append python3 to the LIB and PATH env.

    2. Download and install git for your platform if you don't already have it installed.
       It can be downloaded from https://git-scm.com/downloads
    
    3. Open a new shell/command prompt. It must be new since only a new shell will include the new python 
       path that was created in step 1. Cd to the folder where you want to install the scripts.
    
    4. Execute the following command to install pipenv, which will manage all of the library dependencies:
    
        sudo -H pip3 install pipenv 
 
    5. Clone this repository and change into the directory.

    6. run pipenv to install dependencies (this may take a while as this will download required libraries):

        pipenv install
        
Dependencies
============

See the contents of "pipfile"

Script Names and Purposes
=========================

Scripts and Functions:

    1. ./bin/sumologic-backup.py 

       the script that exports content

    2. ./bin/sumologic-backup.py -h
  
       print a usage message and exit

    3. ./bin/sumologic-backup.py -c <cfgile>

       use a configuration file for the API key name, string, API endpoint, and organization ID

    4. ./bin/sumologic-backup.py -v <integer>

       provide increasingly verbose output on the script execution

    5. ./bin/sumologic-backup.py -t <target>

       Provide either the objectID, the partial name of the content, or "Personal" or "Global"

       *   objectID - backup only one specific content item

       *   <name> - backup all content items that match that name string

       *   "Personal" - backup all your personal folder

       *   "Global" - backup all of the Global content folder

Uncoming Features:
==================

* Provide fixups for the paths and organization ID

* Provide a manifest of the files backed up, and their paths, and dates

License
=======

Copyright 2022 Wayne Kirk Schmidt

Licensed under the GNU GPL License (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    license-name   GNU GPL
    license-url    http://www.gnu.org/licenses/gpl.html

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Support
=======

Feel free to e-mail me with issues to: 

* wschmidt@sumologic.com

* wayne.kirk.schmidt@gmail.com

I will provide "best effort" fixes and extend the scripts.