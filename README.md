# Sockets-Express-Generator
The complete working project of  chat with Sockets express generator

how to start the project.
1. Clone the project.
2. Install the dependencies by using: npm install --save
3. Run the project by: npm start

Sockets are implemented in the Chat page click on the button to go to chat page. 

Here you go!



Steps to follow to configure sockets.io with express-genertor 

Install Socket.io with the following command:

1. npm install --save socket.io
2. Add the following to app.js:

   var sockIO = require('socket.io')();
   app.sockIO = sockIO;
   
3. In bin/www, 
   after var server = http.createServer(app), add the following:

   var sockIO = app.sockIO;
   sockIO.listen(server);

4. To test functionality, in app.js, you can add the line:

   sockIO.on('connection', function(socket){
   console.log('A client connection occurred!');
   });
   
5. Now in layout.hbs add the following snippet before the body closing tag < /body >:

   <script src="/socket.io/socket.io.js"></script>
   <script>
   var socket = io();
   </script>
