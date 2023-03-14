# GitHub-Actions-Importer

## Install instructions

### Prerequisite
- [GitHub CLI installation instructions](https://github.com/cli/cli#installation)

### Authenticate with a GitHub host
> [Windows, Linux & Mac]
>
>```cmd
> gh auth login
>```
>```
>? What account do you want to log into?  [Use arrows to move, type to filter]
>> GitHub.com
>  GitHub Enterprise Server  
>? What is your preferred protocol for Git operations?  [Use arrows to move, type to filter]
>  HTTPS
>> SSH
>? Upload your SSH public key to your GitHub account?  [Use arrows to move, type to filter]  
>> <path>/.ssh/<Key>.pub
>  Skip
>? Upload your SSH public key to your GitHub account? <path>/.ssh/<Key>.pub
>? Title for your SSH key: (GitHub CLI) <Year>-GitHubCli-<OS>-<User>@<MachineName>
>
>? Title for your SSH key: <Year>-GitHubCli-<OS>-<User>@<MachineName>
>? How would you like to authenticate GitHub CLI?  [Use arrows to move, type to filter]
>> Login with a web browser
>  Paste an authentication token
>
>! First copy your one-time code: XXXX-YYYY
>Press Enter to open github.com in your browser... 
>✓ Authentication complete.
>- gh config set -h github.com git_protocol ssh
>✓ Configured git protocol
>✓ Uploaded the SSH key to your GitHub account: <path>/.ssh/<Key>.pub
>✓ Logged in as <GitHub UserName>
>```

### Install the Actions Importer CLI extension
> [Windows, Linux & Mac]
>
>```cmd
> gh extension install github/gh-actions-importer
>```

### Validate installation
> [Windows, Linux & Mac]
>
>```cmd
> gh actions-importer -h
>```
