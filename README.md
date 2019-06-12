docker_post_install
=========

`docker_post_install` does some configuration after installing docker.

Requirements
------------

`docker` shall be installed before this.

Role Variables
--------------

Variables shall be defined:

- `docker_proxy` - boolean, defines if set proxy or not.
- `docker_http_proxy` - string, defines the proxy address for HTTP. If defined, one `http-proxy.conf` would be created.
- `docker_https_proxy` - string, defines the proxy address for HTTPS. If defined, one `https-proxy.conf` would be created.
- `docker_no_proxy` - string, defines the host list needing no proxy, separated by comma. By default, `localhost,127.0.0.1`. 

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
---

- hosts: servers
  roles:
    - role: ./docker_post_install
      docker_proxy: true
      docker_https_proxy: http://127.0.0.1:8080
```

License
-------

MIT

