# fail to upgrade versions because of reconfigure error
upgrading to upper version with apt-get, got error message like below:
```
Preparing to unpack .../gitlab-ee_11.3.4-ee.0_amd64.deb ...
Malformed configuration JSON file found at /opt/gitlab/embedded/nodes/ubuntu-4gb-nbg1-1.json.
This usually happens when your last run of `gitlab-ctl reconfigure` didn't complete successfully.
```

remove just /opt/gitlab/embedded/nodes/ubuntu-4gb-nbg1-1.json
then it works.
