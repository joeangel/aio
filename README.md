# aio
aio = all-in-one & asynchronous I/O

https://docs.google.com/document/d/1ggW4KX9qMU1RgExlDseGVemYB445txJJ6z5fCmOCxm0

## Install Node.js on Mac / Windows

Download and install Node.js 8.11.x from https://nodejs.org/en/download/
Download and install MySQL from https://dev.mysql.com/downloads/mysql/

`$ npm install -g pm2`

## Install Node.js on Ubuntu

`$ sudo apt-get install npm wget mysql-server`

`$ sudo npm install -g n pm2`

`$ sudo n 8.11`

## Usage

`$ git clone https://github.com/KaedeTai/aio.git`

`$ cd aio`

`$ mysql -u root -p < car.sql`

`$ vi config.js`		(and modify the user password)

`$ npm install --python=python2.7`

`$ node www`

`^C`

`$ npm start`

## Test

Open a browser and try these links:
http://localhost:8080/car/get?id=1
http://localhost:8080/car/get?id=2
http://localhost:8080/car/new?name=test&brand_id=1
http://localhost:8080/car/get?id=3
http://localhost:8080/car/delete?id=3
http://localhost:8080/car/get?id=3

## Reference

https://github.com/petkaantonov/bluebird
https://github.com/yortus/asyncawait

## Files(未完)

File Name         | Description
----------------- | -------------------------
app.js            | web server (controller)
io.js             | socket.io server (controller)
models/Car.js     | user model stored in the database
routes/car.js     | user module that serves /user API
utils/DB.js       | database object
utils/FS.js       | utility to access local file system
utils/Facebook.js | utility to call facebook API
utils/Get.js      | utility of HTTP GET
utils/Google.js   | utility to query google
<font color="red">api.js</font> | <font color="red">add res.ok(), res.err(), and res.rtn(), supports rules for req.query</font>
www               | the start script