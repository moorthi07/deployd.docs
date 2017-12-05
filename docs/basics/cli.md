<!--{
  title: 'The "dpd" Command Line Tool'
}-->

Installation

npm install deployd-cli -g

Prerequisites

The CLI requires Node 4 or higher.
Deployd requires MongoDB locally to start sucessfully. Check the Deployd Requirements

Getting started

$ dpd create hello
$ cd hello
$ dpd
To start dpd with Database authentication:

dpd --host "127.0.0.1" -P '27017' -n "mymongodb" -u "myusername" -s "mypassword"

or

dpd --host "127.0.0.1" -P '27017' -n "mymongodb" -a "myusername:mypassword"




## Using the dpd command line tool

### Commands

#### dpd

Start Deployd the current project in development mode with an interactive shell/repl for interacting with the running server.

#### dpd create [name]

Create a Deployd project in a new directory with the given `name`.

#### dpd showkey

Print the app's key for use in a remote dashboard or for making remote authenticated / administrative requests.

#### dpd keygen

Generate a new key for remote access / administration.

#### dpd remote

Open up the remote dashboard in your browser.

### Help

Here is the help output of `dpd -h`:

    Usage: dpd [options] [command]

    Commands:

      create [project-name]
      	create a project in a new directory
      	eg. `dpd create my-app`

      keygen
      	generate a key for remote access (./.dpd/keys.json)

      showkey
      	shows current key for connecting to remote dashboard (./.dpd/keys.json)

      remote
      	open the remote dashboard in your browser


      *
      	[default] start the server in the current project in development mode
      	with an interactive shell/repl for interacting with the running server
      	e.g. dpd (starts server in current directory),
      	     dpd my-app/app.dpd (starts app from file)

    Options:

      -V, --version                      output the version number
    -m, --mongod [path]                path to mongod executable (defaults to `mongod`)
    -p, --port [port]                  port to host server (defaults to 2403)
    -w, --wait                         wait for input before exiting
    -d, --dashboard                    start the dashboard immediately
    -o, --open                         open in a browser
    -e, --environment [env]            defaults to development
    -H, --host [host]                  specify host for mongo server
    -P, --mongoPort [mongoPort]        mongodb port to connect to
    -n, --dbname [dbname]              name of the mongo database
    -a, --auth <auth>                  usesrname:password mongo server credentials
    -u, --username <username>          The user to authenticate as
    -s, --password <password>          The user's password
    -c, --dbconn <dbconnectionstring>  The MongoDB Connection String
        --deploydPath [deploydPath]    allow overriding the path to deployd main script
    -h, --help                         output usage information


  Commands:

    create [project-name]       create a project in a new directory
        eg. `dpd create my-app`
    keygen                      generate a key for remote access (./.dpd/keys.json)
    showkey                     shows current key for connecting to remote dashboard (./.dpd/keys.json)
    *                           [default] start the server in the current project in development mode
        with an interactive shell/repl for interacting with the running server
        e.g. dpd (starts server in current directory),
             dpd my-app/app.dpd (starts app from file)

### Debugging

Deployd uses [debug](https://www.npmjs.com/package/debug) to log requests and show other internal debug info. To activate it you need to set the `DEBUG` env variable to `*`, for example:

    $ DEBUG=* dpd
