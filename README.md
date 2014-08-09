webkeepass-docker
=================

Docker container for WebKeePass

This project is a container for the WebKeePass project created by sukria found here: https://github.com/sukria/WebKeePass

More information on his project can also be found on his blog post below:
http://blog.sukria.net/2013/08/27/webkeepass-or-how-to-build-your-own-cloud-aware-keyring/

The port that the server will run on by default is 5001 and a reverse proxy should be set up to run this under SSL.

There is one volume referenced as /keepass and this should contain your KeePass database file, in this setup named MyKeePass.kdbx. The production.yml file can be modified however if building from source to refer to a name of your choosing.

This container can be run by issuing the following command:

docker run -d --name webkeepass -p 5001:5001 -v /path/containing/keepassfile:/keepass  velocity303/webkeepass-docker


