# Ansible rôle: Gitea

Gitea front (no reverse proxy) with embeded let's Encrypt acme use.

In our case, we uses Gitea with a mariadb database witch isn't on the same server. This role doesnot install mariadb.

On templates/gitea.ini file 

    [oauth2]
    JWT_SECRET = 1bBwvwFreUqcVSvPPO7UZ_4ovAGtQI_kIq070ua4Mms

    [security]
    INTERNAL_TOKEN = eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1NjQ0ODU2NTZ9.D5YYxvLXAerBlfq5JKXHLBhhnI4N5KBKW2Mae2EJJb0
    INSTALL_LOCK   = true
    SECRET_KEY     = xdD1yrkDWNq6LNqTx3bfa3kWOLv8Ew0HOCDzb2QfsJLVpsrcOoPjCA7G9bhTUsVv

Delete them the first time you launch Gitea. It will generate others token / keys.