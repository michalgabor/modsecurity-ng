# WAF based on ModSecurity v3 Nginx

Based on docker image https://github.com/fareoffice/modsecurity-docker


## ENV
PROXY_UPSTREAM_HOST - upstream (example: http://app-lb:80)
CONFIG1 - custom config in Nginx directive http (example: resolver 169.254.169.250;)
CONFIG2 - custom fonfig in Nginx directive location / (example: access_log off;)
SEC_AUDIT_LOG - security log level, default value: (example: H)
SEC_REQUEST_BODY_LIMIT
SEC_PRCE_MATCH_LIMIT
SEC_PRCE_MATCH_LIMIT_RECURSION
PARANOIA 
SEC_RULE_AFTER_VALUE
SEC_RULE_BEFORE_VALUE
CUSTOM_CONFIG_VALUE


