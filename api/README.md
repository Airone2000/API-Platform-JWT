# How to install

- First, make sure I have jwt-auth imported as dependencies and registered/enabled in bundles.php

- Then, generate SSH keys:
	* `openssl genrsa -out var/jwt/private.pem -aes256 4096`
	* `openssl rsa -pubout -in var/jwt/private.pem -out var/jwt/public.pem`
	* For both, choose the same *passphrase*
	
- Add the route to routes.yaml:
`api_login_check:path: /api/login_check`

- /!\ Be cautious : first firewall matching is the winner! Be sure the main firewall is at the end. Or removed.

- Next step : `https://github.com/gesdinet/JWTRefreshTokenBundle`
