# Ansible Role: Certbot

[![Build Status](https://travis-ci.org/kawaz/ansible-role-certbot.svg?branch=master)](https://travis-ci.org/kawaz/ansible-role-certbot)

Install the certificates of Let's Encrypt.

## Requirements

- httpd for proxy routing of acme process.

## Role Variables

```
certbot_email: ''
```

If set, you will receive maintenance/expire/etc notification from Let's Encrypt.

```
certbot_domains: []
```

At least one is required. These are used for the CN and DNS values of the certificate.
Especially the first value is also used for path name of the ceriticate and key.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - { role: kawaz.certbot, certbot_domains: [ example.com ] }

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Yoshiaki Kawazu](https://twitter.com/kawaz).

