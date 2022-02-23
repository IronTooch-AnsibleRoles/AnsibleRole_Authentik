Authentik
=========

Installs Authentik server on Ubuntu 20 Focal

Requirements
------------

None

Role Variables
--------------

- **authentik_pgpass**: The password for the built-in Postgres Db
  - Defaults to *Random 40 character alphanumeric string*
- **authentik_secret_key**: The Authentik Secret Key
  - Defaults to *Random 50 character alphanumeric string*
- **authentik_smtp_host**: The SMTP Host to communicate with to send emails
  - Defaults to *smtp.gmail.com*
- **authentik_smtp_port**: The SMTP Port to connect to send emails
  - Defaults to *587*
- **authentik_smtp_ssl**: Whether the SMTP connection should use SSL
  - Defaults to *false*
- **authentik_smtp_tls**: Whether the SMTP connection should use TLS
  - Defaults to *true*
- **authentik_smtp_username**: What username to provide to the SMTP host to send mail
  - Defaults to *my_user@gmail.com*
- **authentik_smtp_password**: What password to provide to the SMTP host to send mail
  - Defaults to *my_password*
- **authentik_admin_user_email**: What email it should appear that Authentik is sending from?
  - Defaults to *authentik_admin@example.com*

Notes
-----------
Set authentik_smtp_host to "" to remove SMTP provisioning from the .env file. SMTP provisioning defaults are set to be correct for Google SMTP, just change **authentik_smtp_username**, **authentik_smtp_password**, and **authentik_admin_user_email**

Dependencies
------------

No role dependencies.

Example Playbooks
----------------

```yaml
# Deploy Authentik without SMTP alerts
    - role: 'irontooch.authentik'
      vars:
        authentik_smtp_host: ""
```

```yaml
# Deploy Authentik with email alerts configured to send from Google
    - role: 'irontooch.authentik'
      vars:
        authentik_smtp_username: "my_email_address@gmail.com"
        authentik_smtp_password: "my_secret_password"
        authentik_admin_user_email: "authentik@my_personal_domain.com"
```

```yaml
# Deploy Authentik and set Postgres Db Information
    - role: 'irontooch.authentik'
      vars:
        authentik_pgpass: "my_db_password"
```

License
-------

GPL v3.0

Author Information
------------------

Author is Author
