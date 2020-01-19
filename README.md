# NSFCAREER.IO API Documentation

NSFCAREER.IO provides a brain simulation API that enables sensor users to pass the sensor data and get back brain simulation results. To do this, a python file is executed (simulation.py) that sends and receives the data form the nsfcareer.io cloud platform, This file can be called from the command line (e.g. using cygwin or powershell on windows), or can be called directly from with your sensor software platform. It does not use local computing resources - all simulations are run in the cloud (we currently us AWS). A HTML directory is created in the location from which you run the python file that eventually gets populated the results of the brain simulation. It is provided in a simple iframe so it can easily be incorporated into your own platform.

## Obtain the brain simulation API:
- Git Clone the brain simulation API:
- git clone https://github.com/PSUCompBio/nsfcareer-api
- cd nsfcareer-api

## Prerequisites:
- Python (version 3)
- PIP - package manager for Python
- Requests Module
- - Download it using :
- - - pip install numpy
- - - pip install requests
- - - pip install "requests[security]"
- - - pip install yattag

## API usage example from the command line (or from within your app):
python3 python_file/simulation.py --filename samples/sensor_data.xlsx  --user sensor_company --password tusryd-tuGwud-8kinwu --endpoint https://nsfcareer.io/api/upload/sensor-file

where samples/sensor_data.xlsx is an example sensor data. Some samples are placed in the directory nsfcareeer-api/samples. You can supply your own data as long as we know how to read it. If this is the case contact Reuben Kraft at reuben.kraft@psu.edu. 
