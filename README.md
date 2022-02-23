Authentik
=========

Installs Authentik server on Ubuntu 20 Focal

Requirements
------------

None

Role Variables
--------------

- **authentik_external_domain**: EXPLANATION
  - Defaults to *default2*
- **authentik_pgpass**: EXPLANATION
  - Defaults to *default1*
- **authentik_secret_key**: EXPLANATION
  - Defaults to *default2*
- **authentik_pgpass**: EXPLANATION
  - Defaults to *default1*
- **authentik_smtp_host**: EXPLANATION
  - Defaults to *default2*
- **authentik_smtp_port**: EXPLANATION
  - Defaults to *default1*
- **authentik_smtp_ssl**: EXPLANATION
  - Defaults to *default2*
- **authentik_smtp_tls**: EXPLANATION
  - Defaults to *default1*
- **authentik_smtp_username**: EXPLANATION
  - Defaults to *default2*
- **authentik_smtp_password**: EXPLANATION
  - Defaults to *default1*
- **authentik_admin_user_email**: EXPLANATION
  - Defaults to *default2*

Notes
-----------
Set authentik_smtp_host to "" to remove SMTP provisioning from the .env file

Dependencies
------------

No role dependencies.

Example Playbooks
----------------

```yaml
# EXPLANATION
    - role: 'formal_role'
      vars:
        var1: "myapp"
```

```yaml
# EXPLANATION
    - role: 'formal_role'
      vars:
        var1: "myapp"
        var2: "myapp"
        var3: "myapp"
        var4: "myapp"
```

```yaml
# EXPLANATION
    - role: 'formal_role'
      vars:
        var1: "myapp"
        var2: "myapp"
        var3: "myapp"
```

License
-------

GPL v3.0

Author Information
------------------

Author is Author
