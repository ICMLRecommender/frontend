# frontend

ICML 2017 website Frontend project repository

Website, detailing the app design: 
http://icml2017spec.s3-website-us-west-2.amazonaws.com

Start the server
---------------

1. SSH connect to the server and forward port 8000
  ```
  ssh -L 8000:localhost:8000 username@icml.papro.org.uk
  ```
 
2. Modify settings
  ```
  cd /home/icmlapp/backend/server/icml/icml
  cp settings.py.no_https settings.py
  ```
 
3. Launch server
  ```
  cd /home/icmlapp/backend/server/icml
  /home/icmlapp/env/bin/python manage.py runserver
  ```
  
Setup the frontend
-----------------
 
- [Install nodejs and npm](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions)

- Install Polymer v1 (not v2)

  ```
  sudo npm install -g polymer-cli
  ```
  
- Download the code for the frontend from github
- Open terminal and enter
    ```
    cd path/to/frontend
    bower install
    ```
  which would install the needed bower components

- Serve the frontend 

  ```
  polymer serve
  ```
