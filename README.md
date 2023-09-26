# CS520
>>
Work done as a part of CS520 (Data Integration, Warehousing and Provenance) in Fall 2023
>>
Contains Scala, Vizier and Python Codes
>>
Paper-: EDA4SUM: Guided Exploration of Data Summaries for Review
>>
Vizier Assignment-:
>>
Installed Docker from https://docs.docker.com/desktop/install/mac-install/
>>
Executed "docker pull iitdbgroup/vizier_iit_cs520_fall23:arm" command on terminal
>>
docker scout quickview iitdbgroup/vizier_iit_cs520_fall23:arm (To view the summaries of image vulnerabilities and recommendations)
>>
mkdir ~/vizier-520-project-data
>>
cd ~/vizier-520-project-data
>>
docker run  --name vizier --rm -v `pwd`:/vizier.db -p 5001:5001 -p 8089:8089 iitdbgroup/vizier_iit_cs520_fall23:arm -p 5001
