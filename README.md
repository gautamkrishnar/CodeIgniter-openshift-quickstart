CodeIgniter on OpenShift
===================
CodeIgniter is an Application Development Framework - a toolkit - for people who build web sites using PHP. Its goal is to enable you to develop projects much faster than you could if you were writing code from scratch, by providing a rich set of libraries for commonly needed tasks, as well as a simple interface and logical structure to access these libraries. CodeIgniter lets you creatively focus on your project by minimizing the amount of code needed for a given task.

Learn more about CodeIgniter:http://www.codeigniter.com/

This catridge lets you deploy CodeIgniter to Openshift with the click of a single button.

### Install with one click
Create an account at http://openshift.redhat.com/

[![Click to install OpenShift](http://launch-shifter.rhcloud.com/launch/light/Click to install.svg)](https://openshift.redhat.com/app/console/application_types/custom?cartridges[]=php-5.4&cartridges[]=mysql-5.5&initial_git_url=https://github.com/gautamkrishnar/CodeIgniter-openshift-quickstart&name=codeigniter)

### Installing via the command line

Create a php application with mysql (you can call your application whatever you want)

    rhc app create codeigniter php-5.3 mysql-5.1

Add this upstream codeigniter repo

    cd codeigniter
    git remote add upstream -m master git://github.com/gautamkrishnar/CodeIgniter-openshift-quickstart.git
    git pull -s recursive -X theirs upstream master
    # note that the git pull above can be used later to pull updates to codeigniter
    
Then push the repo upstream

    git push

That's it, you can now checkout your application at:

    http://codeigniter-$yournamespace.rhcloud.com

### Spread the word
Liked using CodeIgniter in openshift! Don't forget to spread the word by starring this repo.
