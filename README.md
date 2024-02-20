# ECSSH: AWS ECS Fargate Session Manager

ECSSH is a Bash script designed to facilitate session management for AWS ECS Fargate containers. By utilizing this script, you can easily initiate interactive command execution environments for any task within a specified ECS cluster.

## Prerequisites

Before using this script, ensure the following tools are installed on your system:

- AWS CLI
- jq
- peco

Additionally, **it is crucial that the `enableExecuteCommand` feature is enabled for the ECS tasks and services you wish to connect to**. This script relies on the AWS ECS Execute Command feature to initiate sessions, which will not work if this feature is disabled.

## Installation Instructions

### AWS CLI

For instructions on installing the AWS CLI, refer to the official AWS documentation:

Installing or updating the latest version of the AWS CLI - AWS Command Line Interface

### jq

jq is available for Linux, macOS, and Windows. For installation instructions tailored to your system, visit the jq official website:

jq Download Page

### peco

Install peco using the commands below. If you're on macOS, you can use Homebrew, while Linux users should utilize their respective package managers.

**macOS:**

```
shCopy code
brew install peco
```

**Linux (Debian/Ubuntu):**

```
shCopy code
sudo apt-get install peco
```

## Usage

### Setting Up the Script

First, clone or download this repository, then grant execution permissions to the `ecssh` script.

```
shCopy code
git clone https://github.com/<your-username>/<repository-name>.git
cd <repository-name>
chmod +x ecssh
```

### Executing the Script

The basic usage is as follows:

```
shCopy code
./ecssh -p <AWS Profile Name>
```

The `-p` flag allows you to specify an AWS profile name, which is optional. If not specified, the default profile will be used.

### Displaying Help

To view help information about the script's usage and options, execute:

```
shCopy code
./ecssh --help
```

## Important Note

Ensure that `enableExecuteCommand` is enabled for the ECS tasks and services that you intend to connect with using this script. Without this feature being enabled, the script cannot initiate sessions.

## License

This project is released under the MIT License.