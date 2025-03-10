---
author:
    name: cyberpj
    avatar: https://avatars.githubusercontent.com/u/72292872?s=400&u=f875cb29b4854d0fa41d4a3e2071ce7ef4f62d69&v=4
date: 2024-09-21
category:
    - Active Directory
    - Lab
    - Incident Response
tags: [Active Directory, Lab, Incident Response]
---

# Active Directory Lab

Hello 

After joining the domain, we have to configure few settings to make sure home directory are correctly generated for the domain users, also to make login easier by removing the need of entering domain name along with username (e.g `user` instead of `user@xops.local`).

Edit `/etc/sssd/sssd.conf` and make sure the following line are included, this will allow domain users to ssh login using only their username without the need of specifying domain name.

```bash
use_fully_qualified_names = False

```

Then run the following command to automatically create home directory for domain users.
