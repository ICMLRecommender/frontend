# frontend

NIPS 2017 Recommendations App Frontend project repository

## Note
This app is in pre-release mode for NIPS 2017. Please send feedback
and bug reports to recsysapp@gmail.com or file an issue on our github project page.

## What is this app?
This app helps navigate the rich program of NIPS 2017. The app provides an easily
navigable schedule, enables users to quickly find interesting papers, publicly
comment them, register their interest using 'like' and 'bookmark', and browse what
others are interested in. In addition, users' preferences feed a personalized paper
recommendation engine.

## Bookmarks and Likes.
Papers you choose to bookmark or like are made available through your
"Library" page.

The difference between bookmarks and likes is that liked papers are fed
into the recommendation engine.

## Recommendations.
Recommendations are available through the "Explore" page and are updated
every two minutes. On that page recommended papers are preceded by
trending papers which shows some of the most popular papers.

The recommendation engine is based on the collaborative topic regression (CTR) model of C. Wang and D. Blei. We also used a few tricks to integrate the model with our app.

## Why are we building it?
There are a few reasons one of which is that it can be challenging to keep up with all of the great work published at conferences. We believe that an easy to use app and a good recommendation engine can help surface interesting papers.

Moreover, we built this app as a service to the community, we will open source the app. We would like others to use and even build on it. We believe that the app can also be used as a test bed for recommender engines. As such the app keeps detailed (and anonymous) logs for future offline analysis and model comparisons.

## Who is involved?
The app was designed and built by a team of machine learning students and
researchers spread across England, France, and Canada.

- Adrien Todeschini, Scorelab.io
- Hoai Phuoc Truong, McGill University
- James Ravenscroft, University of Warwick
- Laurent Charlin, Université de Montréal (HEC)
- Lazar Valkov, University of Edinburgh
- Maria Liakata, University of Warwick, Alan Turing Institute
- Sébastien Doncker, SnarkFactory.fr
- Taimur Abdaal, University of Oxford
- Valerio Perrone, University of Warwick
- Yee Whye Teh, University of Oxford, DeepMind, Alan Turing Institute

# Technical contents section below (for internal development use only):

## Website, detailing the app design:
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
