# HTTPS SSL

Project on DNS subdomains and HTTPS/SSL configuration for a load-balanced web infrastructure.

## Servers

| Name | Subdomain | IP |
|---|---|---|
| lb-01 | www, lb-01 | 35.179.119.184 |
| web-01 | web-01 | 18.171.170.245 |
| web-02 | web-02 | 18.171.175.36 |

## Files

### 0-world_wide_web

Bash script that displays DNS record information about subdomains of a domain.

Usage:

    ./0-world_wide_web <domain> [subdomain]

- With only `domain`, it shows the records for `www`, `lb-01`, `web-01` and `web-02`, in that order.
- With `domain` and `subdomain`, it shows the record for that subdomain only.

Example:

    $ ./0-world_wide_web mmarvellio.tech web-02
    The subdomain web-02 is a A record and points to 18.171.175.36
