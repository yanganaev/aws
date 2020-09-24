# aws
Installing, updating, and uninstalling the AWS CLI version 2 on Linux
For the latest version of the AWS CLI, use the following command block:
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64-2.0.30.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```
Install the AWS CLI version 1 using the bundled installer with sudo
The following steps enable you to install the AWS CLI version 1 from the command line on any build of Linux or macOS.

To install the AWS CLI version 1 using the bundled installer

Download the AWS CLI version 1 bundled installer using one of the the following methods.

Download using the curl command.

```$ curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"```

Download using the direct link: ```https://s3.amazonaws.com/aws-cli/awscli-bundle.zip```

Extract the files from the package. If you don't have unzip to extract the files, use your Linux distribution's built-in package manager to install it.

```$ unzip awscli-bundle.zip```
Run the install program. The installer installs the AWS CLI at /usr/local/aws and creates the symlink aws at the /usr/local/bin directory. Using the -b option to create a symlink eliminates the need to specify the install directory in the user's $PATH variable. This should enable all users to call the AWS CLI by entering aws from any directory.

```$ sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws```
By default, the install script runs under the system default version of Python. If you have installed an alternative version of Python and want to use that version to install the AWS CLI, run the install script with that version by absolute path to the Python executable, as follows.

```$ sudo /usr/local/bin/python3.7 awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws```
Verify that the AWS CLI installed correctly.

```$ aws --version```
