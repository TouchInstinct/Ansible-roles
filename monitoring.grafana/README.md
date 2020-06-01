## monitoring.grafana

#### Role arguments:

```yaml
grafana:
  # a string designating the port to bind
  port: "6379"
  # a string used to construct GF_SERVER_ROOT_URL,
  # by default it is also used in the traefik frontend rule
  domain: "grafana.internal"
  ldap:
    # a boolean that switches LDAP authentication on or off
    enabled: false
    # a dictionary of ldap access group mappings
    access_groups:
      admin: "cn=grafana.admin,ou=groups,dc=example,dc=com"
      editor: "cn=grafana.admin,ou=groups,dc=example,dc=com"
      viewer: "cn=grafana.admin,ou=groups,dc=example,dc=com"
  docker:
    # a list of networks to attach to
    networks:
      - web
    # a dictionary of docker labels to add
    labels:
      "traefik.enable": "off"
```
