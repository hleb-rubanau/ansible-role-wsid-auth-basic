# ansible-role-wsid-auth-basic
Installs dockerized service to perform WSID authentication

# Parameterization:

By default, single service is run, but it's possible to alternate default settings

```
wsid_auth_instances:
  - settings_dir: /usr/local/etc/wsid/auth
    installation_dir: /opt/wsid_auth 
    port: 8001
    name: wsidauth
```

Settings directories are not filled with files -- it's responsibility of 
your playbook to add configuration files there and restart the application if needed

# Logging

if `wsid_auth_logging_options_inline` is set to any defined value, 
logging option for journald would be added to containers' compose template.
