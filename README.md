# Domain Connect DynDNS Python
Domain Connect Dynamic DNS in Python.

## Installation
```bash
pip install git+https://github.com/HeinrichAD/DomainConnectDDNS-Python.git
```

## Usage
```
domain-connect-dyndns [-h] [--config CONFIG] [--ignore-previous-ip]
                      [--force-public-ip FORCE_PUBLIC_IP]
                      [--access-code ACCESS_CODE]
                      [--prevent-browser-auto-open]
                      (--domain DOMAIN | --all)
                      {setup,update,status}


Config domain for DynDNS

positional arguments:
  {setup,update,status}
                        action to be performed on domain(s)

optional arguments:
  -h, --help            show this help message and exit
  --config CONFIG       config file path
  --ignore-previous-ip  Update the IP even if no change detected. Don't use on
                        regular update!
  --force-public-ip FORCE_PUBLIC_IP
                        Update with a given IP.
  --access-code ACCESS_CODE
                        Setup access code.
  --prevent-browser-auto-open
                        Prevent automatic webbrowser opening on setup.
  --domain DOMAIN       domain to keep up to date
  --all                 update all domains in config
```

## Examples
```bash
domain-connect-dyndns --domain [domain] setup
domain-connect-dyndns --domain [domain] update
domain-connect-dyndns --domain [domain] status

domain-connect-dyndns --all update
domain-connect-dyndns --all status

domain-connect-dyndns setup \
    --config [config-path] \
    --domain [domain] \
    --access-code [access-code] \
    --prevent-browser-auto-open
domain-connect-dyndns status \
    --config [config-path] \
    --domain [domain]
domain-connect-dyndns update \
    --config [config-path] \
    --domain [domain] \
    --force-public-ip [ip]
```