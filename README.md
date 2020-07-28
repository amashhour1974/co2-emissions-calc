# CO2 Emissions Calculator
Calculates your CO2 carbon dioxide emission when you travel from one place to another, depending on your distance and mode of transporation. The Carbon Footprint Calculator is your go-to tool for looking up and comparing modes of transportation before you go use Google Maps to obtain your travel route. You can choose among several transporation modes like driving, carpooling, using public transport, biking, and walking to see the comparisons in CO2 carbon dioxide emissions.

## How It Works
Enter your starting location and destination (e.g. *Berlin* and *Hamburg*), along with your miles per Kilometers input if you are driving. We'll use this information to calculate the average carbon dioxide emission from your car or mode of transport, display this to you, and give example context to help you understand the application.


Gif created with [Recordit](http://recordit.co/) <br />
<img src="https://s3.amazonaws.com/img0.recordit.co/4FLuMH8LGr.mp4?AWSAccessKeyId=AKIAINSRFOQXTN4DT46A&Expires=1539549370&Signature=Wr5VYIs8VuH0LO5K6LpwRMdjSCg%3D" width=200><br>

## Prerequisites & Dependencies for local runtime

    -   Create a virtual environment and install dependencies:

        python3 -m venv venv
        source venv/bin/activate
        pip install -r requirements.txt

    -   Then set the FLASK_APP environment variable to the app's entry module and run the Flask development server:

        export FLASK_APP=application.py
        flask run

    - Open a web browser, and go to the sample app at http://localhost:5000/
## Deploy on Mircosfot Azure Cloud

    -    Create New GitHub Repository for the Application (e.g : co2-emissions-app)
    -    Push All Application to Github Repository
            
            git init
            git add .
            git commit -a -m “first commit”
            git remote add origin 'Repository_url' 
            git push -u origin master

    -   Deploy the code in your local folder (co2-emissions-calc) using the az webapp up command:
          
          az webapp up --sku F1 -n <app-name> --resource-group <resource-group> -l westeurope

    -   If the az command is not recognized, be sure you have the Azure CLI installed as described in Set up your initial environment.
        Replace <app_name> with a name that's unique across all of Azure (valid characters are a-z, 0-9, and -). 

        The --sku F1 argument creates the web app on the Free pricing tier. 

    -   You can optionally include the argument -l <location-name> where <location_name> is an Azure region such as westeurope
    -   Browse to the deployed application in your web browser at the URL http://<app-name>.azurewebsites.net.

    - Build GitHub CI Workflow Actions to publish the application changes from local environment to Azure App service 
        --  Either to build it from Azure App Deployment center 
        --  Or Build it from Github Repository from actions tab (location: ./github/workflows/master_co2-emission-app.yml)


## Images from the CO2 Emissions Calculator

### Home page
<img src="https://github.com/amashhour1974/co2-emissions-calc/blob/master/display%20images/1.png" width=500><br>
### About page
<img src="https://github.com/amashhour1974/co2-emissions-calc/blob/master/display%20images/2.png" width=500><br>
### CO2 Emission Calculator
<img src="https://github.com/amashhour1974/co2-emissions-calc/blob/master/display%20images/3.png" width=500><br>
### Results page
<img src="https://github.com/amashhour1974/co2-emissions-calc/blob/master/display%20images/4.png" width=500><br>


## References

[General Google Maps API Documentation](https://developers.google.com/maps/documentation/)


[Maps API Distance Matrix Documentation](https://developers.google.com/maps/documentation/distance-matrix/start)
