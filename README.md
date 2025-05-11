# Inferno-Builder

This is a bash script to install a copy of the Caldera ([https://github.com/mitre/caldera](https://github.com/mitre/caldera)) server locally on Kali Linux. While the official Caldera installation instructions on GitHub are minimal, they often require additional workarounds and troubleshooting. This script was designed to streamline the setup process and reduce the complexity involved.

## Prerequisites:

Update APT 

```
sudo apt update
```

Node.js

```
https://nodejs.org/en/download
```

Python3.11 (Simple script I created to install from source - https://github.com/cmurphy06/RescalePy)

## Usage:

For best results, run the script from a directory that does not require elevated privileges. You’ll also need to provide the server IP address - this should be the IP of the machine where the Caldera server will be hosted.

Usage: ./Caldera-Install.sh [SERVER_IP]

During execution, you will be prompted to enter your sudo password. Upon completion, the script will display the credentials generated for the initial Caldera login. Two user accounts—`red` and `blue`—will be shown, as defined in the `caldera/conf/local.yml` configuration file.

Now cd to the caldera directory, run `source venv/bin/activate`, then `python server.py`. The server will be ready when you see 'All systems ready' above a colorful and bold output of CALDERA in the terminal. Now browse to http://[Server-IP]:8888 and log in.

Note: installing Caldera with this script currently only allows you to log in using the IP address ran with the script. If you try to login using [http://127.0.0.1:8888](http://127.0.0.1:8888/) or [http://localhost:8888](http://localhost:8888/), you will be prompted for username and password, but you will not be able to login. No error comes back.

This is the first public script I’ve developed, created to support my current role’s use of Caldera.
