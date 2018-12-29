-----------------------------
Application: KickButt Catalog 
------------------------------
This app is a fictional online catalog for martial arts supplies. Anyone can
access this catalog for browsing products. Anyone with a Google login can login
with their Google login and then can add, edit, and delete products that they
created while logged in. Only the creator of an item can edit or delete it.

The app is hosted on an Amazon LightSail Ubuntu 18 virtual machine. For more
information on LightSail visit https://lightsail.aws.amazon.com/

-----------------
Launching the App
-----------------
Go to a browser and go to either of the following addresses:

	http://54.145.188.230.xip.io/catalog/
	or
	http://54.145.188.230.xip.io/
	
------------------
Navigating the App
------------------
The navigation is straight forward. Simply click any of the links and you will
be routed to the item category or the item itself. If you want to add a new 
item or edit an item that you previously added, click the Login link in the
top banner at the right and the Add New Item will appear. Edit Item and Delete
Item links will also appear for any items that you created.

--------------------
Accessing the Server
--------------------
Only ssh public key/private key connections are allowed. SSH is disabled on
the default port of 22. Instead ssh is listening only on port 2200. 

The user name to use is named grader and has sudo privileges.

The private key that is needed will be sent via separate communication and is
not available via this GitHub page. 

On my Windows 10 laptop the private key file is located at C:\Users\Terry\.ssh\Udacity_TWA.
You can place the private key file anywhere desired on your workstation and 
rename the file as desired.

For example to connect I use the built-in Windows 10 ssh app as follows:

	ssh grader@54.145.188.230 -p 2200 -i C:\Users\Terry\.ssh\Udacity_TWA
	
Replace the value of the -i parameter above to match the location of the 
private key file you saved on your workstation.

----------------------------
Application Code and Credits
----------------------------
The application is written in python 2.7.15rc1 which came bundled with the
LightSail VM. It is located at /var/www/FlaskApp/FlaskApp/__init__.py. Other
files and folders at this location are also needed by the app. Refer to Flask
documentation for more information on the layout and purpose of the folders.

Other libraries and modules used in this application are as follows:

Flask (http://flask.pocoo.org)

SQLAlchemy (https://www.sqlalchemy.org/)

Oauth2client (https://oauth.net)

Google Oauth2 Login (https://console.developers.google.com)

Apache2 (https://help.ubuntu.com/lts/serverguide/httpd.html)

Xip.io (http://xip.io/)

The folder layout for the app was taken from a Digital Ocean site which 
provided much insight into getting the Apache2 Web Services Gateway Interface
(WSGI) configured to run the __init__.py application. This page can be found
at:

https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
