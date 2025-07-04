- Custom http-header injection, use the * :

`python sqlmap.py -u "{{http://www.target.com/vuln.php}}" -H="Cookie:id=1*" `

- Options Breakdown

`{{--no-cast}} : disables casting/conversion of inferred data types`
`{{--union-cols}} : specifies the amount of columns used for union queries`
