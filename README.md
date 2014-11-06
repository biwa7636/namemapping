namemapping

====================================
This is a Python library used to map company names to its company website 


This package is still under development and there are some work you have to do to make it work.

(1) You have to run the following pip command to install:
```
pip install --pre namemapping
``` 

(2) You can use it either as a command line tool like 'wget' or import in your python code as 'import urllib2'
To use it as a command line:
Create a file '.credential' in your working directory with the first line to be consumer_key and the second line to be consumer_secret 
Create the input file and name it as 'input.txt'  

(3) Then you can run command 
```
namemapping
```

What is happening under the hood:
The code will read in `input.txt` and make API requests to yahoo-BOSS and write the raw responses to the file `data.json`, 
After it finish all the searches, it will read in the `data.json` and group all the input search key words based on their domain. 
And write the result to a file called `output.txt` and the result will look like this

```
domain1 ['input1', 'input3', 'input4']
domain2 ['input2', 'input5']
```
