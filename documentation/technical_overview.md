#About

This documentation refers to the project [Sequencer](https://github.com/Micka33/sequencer) published under the licence[BSD 3-Clause](https://github.com/Micka33/sequencer/blob/master/LICENSE).
More explanations available [here](http://choosealicense.com/licenses/) about the [BSD 3-Clause](https://github.com/Micka33/sequencer/blob/master/LICENSE)

#Technologies

##Back-End

###Nginx
Nginx is used as a reverse proxy as well as a caching proxy.  
 - As a reverse proxy: It allows to set it later as a load balancer if needed.  
 - As a caching proxy: It is the best option available to serve static files, so it is used to server the assets.  

###Rails
Rails is used to implement the server logic, and if needed will be used to handle users accounts.  
Each png convertion request passes through rails, to then be saved into Redis waiting to be treated.  

###Sidekiq
Sidekiq is used to launch the convertion jobs saved into Redis.

###NodeJs
NodeJs is used to provide to the user a real-time conversion state of the png.

###Python
Python is used to convert the pngs into one using [anim_encoder](https://github.com/sublimehq/anim_encoder)

##Front-End

###Yeoman
Yeoman is the workflow used to develop the front-end.

###AngularJs
AngularJs is used to provide an asynchronous, user-friendly interface as well as moving the user-logic data manipulation to the user interface.  

###WebSocket
An unknown yet library will be used to implement the communication with NodeJs.

