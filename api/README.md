# How to install

- First, make sure I have jwt-auth imported as dependencies and registered/enabled in bundles.php

- Then, generate SSH keys:
	* openssl genrsa -out var/jwt/private.pem -aes256 4096
	* openssl rsa -pubout -in var/jwt/private.pem -out var/jwt/public.pem
	* For both, choose the same *passphrase*