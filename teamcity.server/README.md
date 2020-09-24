## teamcity.server

#### Role arguments:

```yaml
teamcity_server:
  # a string designating the port to bind
  port: "8111"
  docker:
    # a list of networks to attach to
    networks:
      - web
```
