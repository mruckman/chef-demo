chef-demo
=========

Verification Steps:
See what version of Java is there
$java -version

See if anything is running (get headers)
$curl -I http://localhost:8080

-- BOOTSTRAP WITH CHEF-SOLO ---

Install Git
sudo yum install git

Install Chef (as root)
$cd /tmp
$curl -L https://www.opscode.com/chef/install.sh | sudo bash

Run "Verification Steps:"

Check out this repo to the /var/chef directory
$sudo git clone https://github.com/mruckman/chef-demo.git /var/chef

Run Chef:
$cd /var/chef
$sudo chef-solo -j /var/chef/web.json
