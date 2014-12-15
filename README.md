# fssh

A minimal ssh manager

## Features

- Store connections in json file
- Push ssh key to server

## Connections

Connections are stored in `~/.config/fssh/connections.json` file. You have to create it by yourself. See an example:

	{
		"connections":
		{
			"foo": {"host": "foo.bar.org",     "user": "frostyx"},
			"bar": {"host": "bar.example.org", "user": "frostyx", "vnc": {"slot": "4"}},
			"baz": {"host": "qux.example.org", "user": "jakub",  "port": "2222"}
		}
	}

## Usage

	# List all connections
	fssh list

	# Connect
	fssh connect <connection-name>

	# Push ssh key
	fssh key <connection-name>

	# Open vnc window
	fssh vnc <connection-name>
