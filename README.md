# gcalendar

## Description

This is a simple java application that will read and list calendars events for a list of calendar ids provided.

## Prerequisites

  * Java runtime
  * You have a valid Google calendar and persmission to access calendars you would like to read

## Getting Started

**Download the java app**
  * Create a working directory
  * Click on the *gcalendar.zip* file, then download the file to your working directory
  * Unzip the contents into the working directory. This will extract the file *gcalendar-<version>.jar*
	```
	mkdir ${HOME}/gcalendar
	cd gcalendar
	unzip gcalendar.zip
	```
	
**Turn on the Google Calendar API**
  * Go to https://developers.google.com/calendar/quickstart/java and follow the instructions for Step 1
	```
	- Any name for project name
	- Configure your OAuth client: Desktop app 
	```
  *  Save the *credentials.json* to your working directory (It must be in same directory as the java application file)

**Create list of calendars to read**
  * Create a file called *calendar-ids.txt* in your working directory
  * Add the calendar ids to the file, one per line. The calendar id is the person's email address
  * e.g. sotudeko@sonatype.com

**Run the application**
  * Ensure the 3 files are in your working directory
       
      - gcalendar.jar
      - credentials.json
      - calendar-ids.txt

  * Determine you start and end periods to provide to the application in yyyy-mm-dd format. Typically, these would be a Monday to Friday.
  * Run the app
	* (on the first run, it will open up the Google accounts list for you to select your Google Calendar to provide access to
	```
	java -jar gcalendar-<version>.jar 2020-07-13 2020-07-20
	```
	- Very important: at the very first execution please pick a date range in the past. This will validate the authentication token for future queries.
	
**Output**
  * As well as the summary count of events displayed to the screen, a file named *<startdate>_<enddate>.csv* will also be created in the current directory.



