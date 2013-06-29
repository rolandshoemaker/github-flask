
============

GitHub-Flask is an extension for authenticating Flask applications with GitHub.
It also provides support for various other requests to the GitHub API.


Installation
------------

	pip install github-flask


Usage
-----

An example application is provided. Getting it up and running should be pretty
straightforward:

1. Create a new application on GitHub (or use an existing one)
2. Enter CLIENT_ID and CLIENT_SECRET in example.py.
3. Start the server: ``$ python example.py``


API Requests
------------

After authenticating, this extension also provides methods for doing
requests to the GitHub API as the authenticated user.

	github = GitHub()
	github.init_app(app)

	# returns the authenticated user resource as a dictionary
	github.get('user')
	
	# returns this repository
	github.get('repos/cenkalti/github-flask')