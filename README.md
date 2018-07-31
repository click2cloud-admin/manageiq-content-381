# ManageIQ Content #381

This repository provides a standalone dmoain with the code for ManageIQ/manageiq-content#381.

__WARNING__ - The examples below consider that you are running an appliance, not from source code.

There are two options to import the domain.

1. Import as Git backend domain. It requires _Git Repositories Owner_ role to be enabled on the appliance.

```
# cd /var/www/miq/vmdb
# bundle exec rake evm:automate:import GIT_URL=https://github.com/fdupont-redhat/manageiq-content-381.git PREVIEW=false ENABLED=true
```

2. Import from a exported ZIP file.

```
# curl -o /tmp/v2v-automate-master.zip https://codeload.github.com/fdupont-redhat/manageiq-content-381/zip/master
# cd /tmp/
# unzip manageiq-content-381-master.zip
# cd /var/www/miq/vmdb
# bundle exec rake evm:automate:import DOMAIN=GH381 IMPORT_DIR=/tmp/manageiq-content-381-master PREVIEW=false ENABLED=true
```

Unless you want to contribute to this domain, you probably only need the Git backed approach.
