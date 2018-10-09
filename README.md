# WAF based on ModSecurity v3 Nginx

Based on docker image https://github.com/fareoffice/modsecurity-docker


## ENV
PROXY_UPSTREAM_HOST - upstream (example: http://app-lb:80)  
CONFIG1 - custom config in Nginx directive http (example: resolver 169.254.169.250;)  
CONFIG2 - custom fonfig in Nginx directive location / (example: access_log off;)  
SEC_AUDIT_LOG - security log level, default value: ABIJDEFHZ (example: H)  
SEC_REQUEST_BODY_LIMIT - maximum request body size in bytes, default 524288 (example: 52428800)  
SEC_PRCE_MATCH_LIMIT  - adjust this to fight PRCE Limit errors, default 1000000  
SEC_PRCE_MATCH_LIMIT_RECURSION  adjust this to fight PRCE Limit errors, default 1000000  
PARANOIA - security level 1 - 4, default 2  
SEC_RULE_AFTER_VALUE - exclude rules (example: SecRuleRemoveById 942430 SecRuleRemoveByTag "attack-sqli")  
SEC_RULE_BEFORE_VALUE  update rules 
CUSTOM_CONFIG_VALUE  - add custom modsec config (example: SecAction  "id:900200, phase:1, nolog, pass, t:none, setvar:'tx.allowed_methods=GET POST PUT DELETE'")  


