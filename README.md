# :bookmark_tabs: GitHub-Actions-Importer

## :clipboard: Install instructions

### Prerequisite
- [GitHub CLI installation instructions](https://github.com/cli/cli#installation)

### Authenticate with a GitHub host
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
>```cmd
> gh extension install github/gh-actions-importer
>```

### Validate installation
>```cmd
> gh actions-importer -h
>```

## Configure
>```cmd
> gh actions-importer configure
>```
> NOTE: Selecting each option will prompt for configurations and Personal Access Token (PAT) information.
>```
>? Which CI providers are you configuring?: Hit <space> to select, <ctrl+a> to toggle all, <ctrl+i> to invert selection
>  ◉ Azure DevOps
>  ◉ CircleCI
>  ◉ GitLab CI
>  ◉ Jenkins
>  ◉ Travis CI
>
>```

## Update
>```cmd
> gh actions-importer update
>```

## Usage

### [Audit](https://github.blog/2022-11-10-introducing-github-actions-importer/#1-plan-the-timeline-and-complexity-of-the-migration)
>GitHub Actions Importer provides an audit command that is designed to help analyze the complexity of a potential migration, which can be used to formulate a migration plan. This command will fetch all of the pipelines defined in a specified scope of the existing CI/CD environment, attempt a conversion of these pipelines to their equivalent workflow, and write a summary report with statistics gathered from the audit.
>```cmd
> gh actions-importer audit jenkins --output-dir .
>```

### [Dry-run](https://github.blog/2022-11-10-introducing-github-actions-importer/#4-customize-a-workflows-conversion)

> You can use the dry-run command to convert an existing pipeline to its equivalent GitHub Actions workflow. The console output of the command will list the path to the file or files that GitHub Actions Importer generated. Before migrating, you should perform a dry run of a pipeline and validate the contents are suitable.
> gh actions-importer dry-run jenkins --source-url $SOURCE_URL --output-dir 
>
>```cmd
> gh actions-importer dry-run jenkins --source-url $SOURCE_URL --output-dir 
>```


## :star: Resources
- [Introducing GitHub Actions Importer](https://github.blog/2022-11-10-introducing-github-actions-importer/)
- [Actions Importer for CI/CD migration](https://github.blog/2023-03-01-github-actions-importer-is-now-generally-available/)
