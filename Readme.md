# Shakespeare Passages Recommendation System

This repository holds the code for an intertextual recommendation system that links passages in the Shakespearean dramatic corpus (as digitized by Folger) to one another based entirely on scholarly citations/quotations (as identified by JSTOR Labs in their collection of digitized works, and made available in what was called their Matchmaker API). 

The web interface is currently running at https://theshakespearegame.rice.edu

The Critical Inquiry article is available at https://doi.org/10.1086/715982

(update Jan. 30, 2023) The SQLite database is available in a package submitted to the Rice Research Repository. The MySQL build turned out to have no performance advantages, was more costly to host, and more difficult for other users to set up.

The web application uses

* A SQLite database
* A Python Flask web application and gunicorn service
* jQuery to bind events to page elements

Prior versions of this application used SQLite databases in order to allow users to select between 1-20 line passages, but this greatly increases the amount of data that has to be handled. For smoother deployment, I've restricted the interface to 10-line passages.

The setup is simple (as of 2023) using Python3 and its virtual environment package.

Simply navigate to the application folder (that this Readme is located in), and run the following lines of code.

	python3 -m venv venv
	source venv/bin/activate
	pip3 install -r requirements.txt
	python application.py