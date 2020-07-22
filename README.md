## E-Mail Header Analyzer (MHA)
![mha](https://cloud.githubusercontent.com/assets/1170490/18221866/b7b362d6-718e-11e6-9fa0-2e7f8bc2b9d7.png)


## What is E-Mail header analyzer (MHA):
E-Mail header analyzer is a tool written in [flask](http://flask.pocoo.org/) for parsing email headers and converting them to a human readable format and Based on the common practice in e-mail investigation,the developed system provides the following functionalities:       
* Identify hop delays.
* Identify the source of the email.
* Identify hop country.


## Installation
Install system dependencies:  
```
sudo apt-get update
sudo apt-get install python-pip
sudo pip install virtualenv
```
Create a Python virtual environment and activate it:  
```
virtualenv virt
source virt/bin/activate
```
Clone the GitHub repo:  
```
git clone https://github.com/kodjunkie/mail-header-analyzer.git
```
Install Python dependencies:
```
cd MHA
pip install -r requirements.txt
```
Run the development server:  
`python server.py -d`

You can change the bind address or port by specifying the appropriate options:
`python server.py -b 0.0.0.0 -p 8080`

Everything should go well, now visit [http://localhost:8080](http://localhost:8080).

## Docker

A `Dockerfile` is provided if you wish to build a docker image.

`docker build -t mha:latest .`

You can then run a container with:

`docker run -d -p 8080:8080 mha:latest`

## Credits
Built on [github.com/lnxg33k/email-header-analyzer](https://github.com/lnxg33k/email-header-analyzer)
