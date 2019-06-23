# BOCS
Blockchain oriented Cheque Settlements

Requirements
Python 3.X
Flask
$pip install flask
Pusher 
$pip install pusher
Create a pusher ID from Pusher website and add the api key and key to the file. 
## HYPERLEDGER FABRIC FABCAR SAMPLE MODEL
clone the fabcar model
modify the config.yaml file to have banks as the peers and clients as the organization
Architecture is similar to the fabcar python sdk

1. php for generating QR codes

Enter the details as required and check the folder outputQR for the generated and encrypted QR

## BANK SIDE DATABASE
2. Bank dahsboard and login page
Setup and activate venv


Install the software.

* Git.
* Python.
* Pip.

## Install

Clone the git repository on your computer

$ cd dashboard
$ pip install flask
$ pip install pusher
$ python dbsetup.py```
$ export FLASK_ENV=development
```

##Run the application
 
``` $ flask run --PORT 5555```

## Built With

Clone the project,
Start a blockchain node server,

```sh
$ export FLASK_APP=node_server.py
$ flask run --port 8000
```

One instance of our blockchain node is now up and running at port 8000.


To run the application,

```sh
$ python run_app.py
```

Clone the project,
Start a blockchain node server,

```sh
$ export FLASK_APP=node_server.py
$ flask run --port 8000
```

One instance of our blockchain node is now up and running at port 8000.


To run the application,

```sh
$ python run_app.py
```

some of the snapshots can be found in snaps
1. Posting the OTP
2. Requesting the node to mine
3. Resyncing with the chain for updated data
To play around by spinning off multiple custom nodes, use the `add_nodes/` endpoint to register a new node. 
Here's a sample scenario that you might wanna try,

```sh
# already running
$ flask run --port 8000
# spinning up new nodes
$ flask run --port 8001
$ flask run --port 8002
```

You can use the following cURL requests to register the nodes at port `8001` and `8002` with the already running `8000`.

```sh
curl -X POST \
  http://127.0.0.1:8001/register_with \
  -H 'Content-Type: application/json' \
  -d '{"node_address": "http://127.0.0.1:8000"}'
```

```sh
curl -X POST \
  http://127.0.0.1:8002/register_with \
  -H 'Content-Type: application/json' \
  -d '{"node_address": "http://127.0.0.1:8000"}'
```

This will update the newer nodes with the longest chain, and the list of peers, so that they are able to actively participate in the mining process post registration.

To update the node with which the frontend application syncs, change `CONNECTED_NODE_ADDRESS` field in the [views.py]
