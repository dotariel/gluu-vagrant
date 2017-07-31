# gluu-vagrant
This repository creates a Gluu server with Shibboleth IdP installed. The VM is created with 2 CPUs and 8GB of RAM by default as recommended in the Gluu documentation. [Gluu Installation](https://gluu.org/docs/ce/installation-guide/)

## Getting Started
To get started, create the Vagrant instance:

```
vagrant up
```

Then, create a hostname mapping for `gluu.local` in `etc/hosts`:
```
192.168.2.120 gluu.local
```

Next, login to the Gluu UI at https://gluu.local, and authenticate with the following credentials:
```
username: admin
password: admin123
```

## Configure SAML
[Gluu Documentation](https://gluu.org/docs/ce/admin-guide/saml/)
