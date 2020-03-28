# Devops Coding Challenge

Get this [app](https://github.com/KMK-ONLINE/devops-coding-challenge) up and
running on a [Vagrant VM](https://www.vagrantup.com/) using your known production
best practices as well as the instructions in the guidelines below.

You should use [provisioner](https://www.vagrantup.com/docs/provisioning/) to install and configure everything. Ansible is
preffered. But you can use chef or puppet if you more familiar with those tools.
(please don't use shell provisioner).

When you're done, we should be able to type `vagrant up` and our app will be
running and reachable on http port 80 at `http://10.10.10.20` and `http://devops.kmklabs.dev`

### Guidelines:
  - The provisioner should clone [this github repo](https://github.com/KMK-ONLINE/devops-coding-challenge) into the VM under `/webapps/kmk`
  - You should be able to find what system packages are needed by looking through the app
  - You should not need to change the app code in any way
  - The app should be running as a non-privileged user
  - The app should be automatically restarted if crashes or if killed
  - The app should maximize all of the available CPUs (have
    [Vagrant virtualize multiple CPUs](https://www.vagrantup.com/docs/virtualbox/configuration.html))
  - The related logs should be rotated
  - Timezone should be in UTC

Write your provisioner script in your own private repo and when complete, send
to [us](mailto: cecep.mahbub@kmklabs.com) the contents in a zip or tarball.

You may stick to the default Vagrant image (ubuntu/trusty64) or use another
preferred flavor of Linux.

We'll evaluate the submission on simplicity, code quality, and use of best
practices on the provisioning code. Feel free to be creative and take liberties
where you feel it will improve the deliverable!