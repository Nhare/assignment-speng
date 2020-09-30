# Support Engineer Test

### The exercise 

Please have a look at the test.html file. This file contains some basic prebid/postbid implementation with some issues. 

Your job is to find and fix any issues you can see as well as implementing/fixing the refreshAd function to load a new ad every given time.

Please publish your solution into a public git repository of your choice, like GitHub or Bitbucket. 

### How to run and dependencies

You will need a webserver to run the test page. You can obviously use any web server you like or the project comes with a prepackaged http server.

To run the project's webserver you will need to install npm and node.js. You can download package for system here: https://nodejs.org/en/

To serve the project run 

`npm install`

`npm run server`

This will launch a webserver on default port 80.

Since the test contains real ad setup you will need to set up your localhost to run under hb-dev.vntsm.com in order to see any bids come through.

To do so you have to edit your hosts file to contain record like this:

`	127.0.0.1       hb-dev.vntsm.com`

You can learn how to edit your hosts in this article: https://www.howtogeek.com/howto/27350/beginner-geek-how-to-edit-your-hosts-file/
