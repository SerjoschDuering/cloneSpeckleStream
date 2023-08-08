# Speckle Stream Cloning

This notebook demonstrates how to clone a Speckle stream from one to another. It uses the Speckle SDK to interact with a Speckle Server and perform operations like fetching branches and commits, and cloning them into a target stream.

## Requirements

- Speckle SDK: You can install it using pip (`pip install specklepy`)
- A Speckle account: You'll need an account to access a Speckle Server. You can create one [here](https://speckle.systems/).
- A Speckle Server URL and Personal Access Token: These are required to authenticate with the server.

## Usage

The main function for cloning a stream is `clone_stream()`, which takes the following arguments:

- `source_stream`: The URL of the stream that you want to clone.
- `target_stream`: The URL of the stream where you want to clone the source stream.
- `server_url`: The URL of your Speckle Server (optional if you're using the default account stored on your machine).
- `token`: Your Personal Access Token for the Speckle Server (optional if you're using the default account stored on your machine).
- `max_commits`: The maximum number of commits that you want to clone from each branch (default is 1).
- `max_branches`: The maximum number of branches the script iterates through (default is 100)

Here's how you can use the function:

```python
SERVER = 'your_server_url'
TOKEN = 'your_token'
source_stream = 'source_stream_url'
target_stream = 'target_stream_url'

clone_stream(source_stream, target_stream, max_commits=1, max_branches=100, server_url=SERVER, token=TOKEN)
