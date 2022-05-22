
# Evernote Web APP UI Testing using Selenium with Python unittest framework
## Pre-requisites:
#### -Firefox browser
#### -Install required packages from requirement.txt
Change current directory to clone repository location in local system and type following pip command to install required packages:
```
pip install -r requirement.txt
```
### Helper module:
It contains all common import libraries
### Locator module:
It contains all the web elements and their respective locations that are being used in UI testing
### Page Object module:
It contains all the web page classes contains web elements and action methods
### TestSuite script:
It contains all the 4 test scenarios source code in unittest module framework.
### reports module:
It contains html test execution results summary reports
## How to execute automation tests?
Change current directory to clone repository location in local system and type following commands in commandline interface:
```
cd Evernote
python -m TestSuite
```
Once all test cases are exeuted successfull you can check console output from command line and html reports generated from Evernote/reports

## How to import Jenkins job to build and execute automation tests?
## Pre-requisites:
#### -ShiningPanda Jenkins plugin 


### To Import Evernote build job:

#### -Open Jenkins
#### -Navigate to Dashboard
#### -Click on Manage Jenkins
#### -Click on Jenkins CLI under tools and Actions
#### -Download  jenkins-cli.jar
#### -Open command line and navigate to jenkins-cli.jar download location
#### -Copy and paste the Evernote build job xml to the same location as jenkins-cli.jar
#### -execute below commands
```
java -jar jenkins-cli.jar -s http://server -auth username:password create-job NewjobName < Evernotejenkinsjob.xml
```
Once job is imported successfully, open job and click on config 
#### Build -> Custom Python Builder -> Home
#### Change directory path to you local machine python installation directory

Save job and Click on Build Now

