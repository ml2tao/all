Gospel sdk based on c9.
======================================

#### Installation ####

Follow these steps to install the SDK:

    git clone git@github.com:Gospely/gospel.git
    cd gospel
    scripts/install-sdk.sh
    
To update the SDK to the latest version run:

    git pull origin master
    scripts/install-sdk.sh
    
Please note that Gopsle is currently developed with Node.js 0.12 and 0.10. Newer versions of node should work too.

#### Starting Gospel ####

Start the Gospel as follows:

    node server.js
    
    ./server.js -p 8080 -l 0.0.0.0 -a :  
    
    ./server.js -w /var/www/c9ws/ivy/workspace --settings=standalone -p 8787 -l 0.0.0.0 -a :

The following options can be used:

    --settings       Settings file to use
    --help           Show command line options.
    -t               Start in test mode
    -k               Kill tmux server in test mode
    -b               Start the bridge server - to receive commands from the cli  [default: false]
    -w               Workspace directory
    --port           Port
    --debug          Turn debugging on
    --listen         IP address of the server
    --readonly       Run in read only mode
    --packed         Whether to use the packed version.
    --auth           Basic Auth username:password
    --collab         Whether to enable collab.
    --no-cache       Don't use the cached version of CSS

Now visit [http://localhost:8181/ide.html](http://localhost:8181/ide.html) to load Gospel.

#### Running Tests ####

Run server side tests with:
    
    npm run test
    
Run client side tests with:

    npm run ctest
    
Then visit [http://localhost:8181/static/test](http://localhost:8181/static/test) in your browser.

Happy coding, Gospel
