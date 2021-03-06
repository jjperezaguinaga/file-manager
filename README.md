# MyBit-FileManager

## First time setup
* From the root of the folder run ```npm install```
* From **/server** run ```npm install```
* Create two folders ```public``` and ```files``` under **/server**.
* Create an ```.env``` file at the root of the project, like so:
<br/>
REACT_APP_USERNAME=yourusername
<br/>
REACT_APP_PASSWORD=yourpassword
<br/>
REACT_APP_SERVER_DEV=http://localhost:8000
<br/>
<br/>

***Note***: these auth details need to match the ones in the server, defined in the file ```users.htpasswd``` under **/server** (check [http-auth](https://github.com/http-auth/http-auth) for more information about the authentication method used). Currently those credentials are encrypted using bcrypt. Don't encrypt the credentials in the ```.env``` file. The url for the server can be changed. Make sure not to include a forward slash at the end of it. Also make sure the port defined in the ```.env``` file matches the port defined in the server.

## How to build for production and start the server
From **/src** run ```npm run build:prod```<br/>
This command builds the react app and copies the contents of **/build** to **/public** on the server's directory so that the front-end can be served.

## How to run the front-end
From **/src** run ```npm run start```<br/>

## How to run the server
From **/server** run ```npm run start```

### Important notes
Files with over **2GB** are not supported.
