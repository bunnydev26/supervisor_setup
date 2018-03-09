# supervisor_setup
We setup a simple supervisor configuration to run a simple node app

We first need to install the supervisor
- sudo apt-get install supervisor
- sudo service supervisor status
  If the service is not started kindly start it..
- Go to the director /etc/supervisor/
  Here when you do an ls you will find two items:
  * conf.d     supervisord.conf
  If you try to go through the supervisord.conf file you will know that it reads any *.conf file located in the conf.d file and start the process basically.
- We will copy the webhook.conf file mention in the reposiotry in to the /etc/supervisor/conf.d
- Once successfully copied following are the steps to get started with running our first supervisord
   - supervisorctl help (This is a command that will give different commands associated with supervisorctl)
   - supervisorctl status (This will display the number of confs running on supervisor)
   - supervisorctl reread (This will kind of compile the conf file and show that it is available Note: you need to create the respective directory for the logs)
   - supervisorctl reload (THis will reload your conf file and run the newly added supervisor confs)
- Following are the useful commands
   - supervisorctl restart <program:name> In our case it would be webhook. This names are defined in the .conf file)
   
To complete this tutorial kindly place the files in the respective directories and make your changes:
My working directory where i have placed mine http.js file is:
/home/amit/tempre/supervisor_learn/http.js (Since we have given an absoulte path in the .conf file make the necesseray changes)

Refrences:
https://serversforhackers.com/c/process-monitoring-with-supervisord
https://www.youtube.com/watch?v=8ZVf0T1I2vw&t=30s 
