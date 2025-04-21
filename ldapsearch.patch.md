## LDAP SEARCH ##

- Acquire domain information for queries
`ldapsearch -x -H ldap://$IP -s base namingcontexts`

- Auth search
`ldapsearch -x -H ldap://$IP -D '$DOMAIN_NAME\$USER' -w '$PASS' -b $QUERY`
`ldapsearch -x -H ldap://$IP -D 'cn=$USER,cn=Users,dc=$DOMAIN_NAME,dc=$DOMAIN' -w '$PASS' -b $QUERY`

- Dump LDAP...essentially. All subtrees of a child domain
`ldapsearch -x -H ldap://$IP -s sub -b '$DOMAIN'`
