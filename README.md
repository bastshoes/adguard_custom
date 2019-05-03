# Adguard Home custom component for Home-assistant

This custom component for Home-assistant.
Component work with Home-assistant startinf 0.92 or later.

# Installation

# Step 1

Create a directory called `adguard` in the `<config directory>/custom_components/` directory on your Home Assistant instance.
Install this component by copying the files in [`/custom_components/adguard/`] from this repo into the new `<config directory>/custom_components/adguard/` directory you just created.

# Step 2

Add this to your `configuration.yaml`

```yaml
adguard:
  host: <IP_ADDRESS> or <HOST_NAME>
  username: <USER_NAME>
  password: <PASSWORD>
```
# Optional config options
This is all the optional configuration options for this component.

```yaml
host:
  description: IP address or Nmae of the host where Adguard Home is running.
  required: true
  type: string
  default: localhost
```

```yaml
port:
  description: The port where GlancesAdguard Home is listening.
  required: true
  type: integer
  default: 80
```

```yaml
username:
  description: Your username for Adguard Home.
  required: true
  type: string
```

```yaml
password:
  description: Your password for Adguard Home.
  required: true
  type: string
```

```yaml
name:
  description: The prefix for the sensors.
  required: false
  type: string
  default: Adguarad
```

```yaml
ssl:
  description: "If `true`, use SSL/TLS to connect to the Adguard Home server."
  required: false
  type: boolean
  default: false
```

```yaml
verify_ssl:
  description: Verify the certification of the system.
  required: false
  type: boolean
  default: false
```

```yaml
monitored_conditions:
  description: Defines the stats to monitor as sensors.
  required: false
  type: list
  default: queries
  keys:
    blocked:
      description: Total number of blocked ads during 24h.
    blocked_percentage:
      description: Percentage of blocked ads during 24h.
    queries:
      description: Total number of DNS queries handled by Adguard Home during 24h.
    version:
      description: Version of Adguard Home.
```

This platform was not made by ADGUARD SOFTWARE LIMITED or the ADGUARD community. They did not provide support, feedback, testing, or any other help during its creation. This is a third party platform which may break if ADGUARD changes their API in a later release. It is not official, not developed, not supported, and not endorsed ADGUARD SOFTWARE LIMITED or the ADGUARD community. The trademark `ADGUARD` and the logo is used here to describe the platform. `ADGUARD` is a registered trademark of ADGUARD SOFTWARE LIMITED.

# Credits

- [ludeeus](https://github.com/ludeeus) for the library

