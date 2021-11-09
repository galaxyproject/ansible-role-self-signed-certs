# Ansible Role for Self Signed Certificates

This is designed to work with `galaxyproject.nginx` to generate self-signed certificates as-needed. So something like

```
- name: Install and configure nginx
  hosts: webservers
  vars:
    nginx_servers:
      - vhost1
      - vhost2
    nginx_ssl_servers:
      - vhost1_ssl
      - vhost2_ssl
    nginx_ssl_role: galaxyproject.self_signed_certs
    openssl_domains:
      - vhost1.example.org
      - vhost2.example.org
  roles:
    - galaxyproject.nginx
```

## License

GPLv3

## Author Information

This role was written and contributed to by the following people:

- [Helena Rasche](https://github.com/hexylena)
