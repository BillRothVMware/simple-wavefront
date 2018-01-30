# simple-wavefront
Simple code for wavefront

This is the simple PHP code to grab the temperature from a Nest thermostat in php

Essentially: 
1. send-temp-wf is called from crontab once a minute
2. in the "echo" which sends a graphit format datapoint to the Wavefront proxy, nestc is called, which is a wapper to call
3. php -f nest-temp-cli.php, which returns the temp in degrees f. Note the included class.

I know its ugly. But it works.

I am pretty sure I got the idea here:

https://33sticks.com/analyzing-home-heating-and-cooling-data-using-nest-collecting-the-data/

To get it working, do the following:
1. download the 2 php files
2. update nest-temp-cli.php with your nest login and password
2. call php -f nest-temp-cli.php, making sure the nest.class.php can be found by the php classloader.

Bill Roth


You can get a free account for wavefront at http://wavefront.com/sign-up/
