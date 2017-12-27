# Website - A Hedge-Ops DevOps Project

This project is inspired by Hedge-Ops. The full blog post can be found here: [DevOps Project](http://hedge-ops.com/devops-project/).

## Phase 1: Simple Website
1. Create an account on https://github.com/
2. Create a repository named ```website``` on Github
3. Clone your ```website``` repository locally using your terminal (Terminal on a mac or PowerShell on windows)
4. Create a branch called ```feature_index```
5. Add an ```index.html``` to the branch that says ```Hello, World!``` in the text. You’ll want to make the change with Visual Studio Code
6. Check that in
7. Create a pull request for your branch to be merged into ```master```
8. Merge your pull request into ```master``` after it’s approved

## Phase 2: Simple Webserver
1. Create an account on Azure and activate free trial
2. Create an ubuntu virtual machine on Azure
3. SSH to that machine
4. Set up nginx on the machine
5. Clone your git repository to ```/var/www/html``` on the server
6. Using the public ip assigned to your ubuntu server, access the website

*Resources*
* [Create VM](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-portal)
* [Installing Nginx on an Azure Linux Ubuntu 16.04 VM](http://www.gigasacs.net/language/en/2016/05/11/installing-nginx-on-an-azure-linux-ubuntu-16-04-vm/)

## Phase 3: Deploy a Change
1. Create a new branch on your repository named ```feature_myname```
2. Update ```index.html``` to say “Hello, Michael!”
3. Create a pull request, get it reviewed, and merge it
4. On your webserver, update your ```index.html``` file from GitHub.

## Phase 4: Create a Chef Cookbook to Automate Machine Setup
1. On GitHub create a repository called ```my_website```
2. Clone that repository locally and switch to a branch called ```feature_nginx```
3. Set up ```nginx``` using the package resource
4. Use Test Kitchen to make sure your cookbook installs the package. Use kitchen with a Policyfile. There will be a ```Policyfile.rb``` in the cookbook that defines your run list if you’re doing this right.
5. Write an Inspec Test that ensures the package is installed
6. Create a PR and get it merged
7. Create another branch called ```feature_website```
8. Using the git resource clone your repository on GitHub
9. Write another inspec test to make sure that the website is served when you go to ```http://localhost``` and that the contents contain “Hello, Michael!”
10. Make sure that ```kitchen test``` works
11. Create a Pull Request and Merge into master