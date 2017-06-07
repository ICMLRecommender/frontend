# frontend
ICML 2017 website Frontend project repository

Website, detailing the app design:
http://icml2017spec.s3-website-us-west-2.amazonaws.com
 
# To setup the front end:
 
- Install Polymer, v1, not v2
- Download the code for the frontend from github
- Open terminal and enter
    
    ```
    bower install
    ```
  which would install the needed bower components
 
To start the server:
 
1. 
```
ssh -L 8000:localhost:8000 username@icml.papro.org.uk
```
 
2. Launch server
```
cd /home/icmlapp/backend/server/icml/icml
cp settings.py.no_https settings.py
```
 
3. 
```
cd /home/icmlapp/backend/server/icml
/home/icmlapp/env/bin/python manage.py runserver
```
