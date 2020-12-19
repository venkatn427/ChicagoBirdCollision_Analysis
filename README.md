# ChicagoBirdCollision_Analysis


This script is to read the json file, clean the data and save the comined file in desired format. 

I have used Anaconda version of python for writing this scipt. 

Follow the instructions from the below page to install the anaconda in your local machine. 

MacOS Installation - https://docs.anaconda.com/anaconda/install/mac-os/
	
	-> you can use the above page to install GUI or via terminal

Windows Installtion - https://docs.anaconda.com/anaconda/install/windows/
	-> Download the application and follow instructions to install anaconda. 


If you just want to install pandas use pip install pandas to install pandas library. 

	To validate the pandas installation:
	1) check the python installation with below command
			python --version

	2) you should see the python version if you don't install python using below page. 
		https://www.python.org/downloads/mac-osx/

	3) Once python is installed, open the terminal and run import pandas command to validate pandas installation. 

	4) we'll use logging to write the log file 

I used MacOS Installation to install the Anaconda. 

The library used mostly in this script is Pandas (a Python package that provides fast, flexible, and expressive data structures designed to make working with structured (tabular, multidimensional, potentially heterogeneous) and time series data both easy and intuitive)

Below are the steps included in the development of the script. 

	1) Take the folder path as input and list the json files for the folder. 
		-> List all the json files from the given input folder. 
	2) Read the json files using pandas library and create a dataframe for each json file. 
		-> For each file in the list, create a new dataframe and name it as filename.
		-> check the dataframes to see the data is loaded.
	3) Analyze the data and look for any data discrepencies.
		-> After checking the data data looks different in one table compared to other and need to change column names. 
	4) Since the column names are mismatched and data is not correct, the columns are renamed in inflight file. 
		-> using replace the column names are changes to original names. 
	5) The files are combined to generate the output summarized file. 
		-> After the column name changes, used merge to combine the dataframes on matched columns.

while entering the outputfile path, we can select whether to provide outfilename with extension with yes or no condition. 

if desired file extension is selected then the file will be created based on selected format. 

Based on the file format requested the export function is conditioned to write in the desired output format. 
If no file extension is selected the last name in the folder path is taken as output file path and written in default format in this case is csv. 
CSV is common format to analyze the tabular data, pivoting and also easy for calculations. So chosen the csv as default output file format and also has the flexibility to select the output file format. 

If the desired output fileformat is xlsx, then openpyxl needs to be installed and checked before running. 

run pip install openpyxl to install the required package to write the output file in xlsx format. 

