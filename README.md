# internode.py

Python script for retrieving your Internode account usage and outputting as JSON
files.

__Work in progress__.  
This script was created by studying [cafuego/internode-php](https://github.com/cafuego/internode-php).
There is no guarantee that it is functional for all account types. Please raise 
an issue or pull-request if you encounter problems.

## Setup

Install the required packages with _pip_ (_virtualenv_ is recommended)    

```pip install -r requirements.txt```

Add your username and password to `export.py` by replacing the `USERNAME` and
`PASSWORD` variables with your Internode account details (do not include
`@internode.on.net`), then execute by running `python export.py`.

If you want to write your own script to handle your account information, you can
simply import the `internode` package and interact with the classes directly.

## Output

Each service tied to your account is output as a JSON file, named after your
service ID. i.e. `1234567.json`.

An additional JSON file, `account.json`, is also generated that contains a list
of each of the aforementioned files.

By default, JSON files are output to the `data` directory in the script's
working-directory. If this directory does not exist, the script will attempt to
create it.

## Wishlist

- Python 2\3 compatibility
- A nice static site which can display this information
