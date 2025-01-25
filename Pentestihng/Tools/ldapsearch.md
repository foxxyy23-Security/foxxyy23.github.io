# Ldapsearch tool
## usage
Tool is used for querying data from LDAP databases. Can be used for enumeration on a target after getting intial access
- -x
    - simple auth
- -w
    - password
- -D
    - username
- -H
    - URI Identifier (machine your attacking)
    - 'ldap://<IP>'
- -b
    - base dn ('dc=<domain>,dc<identifier>)
- -s sub
    - scope   one of base, one, sub or children (search scope)



## Examples
```
ldapsearch -x -H 'ldap://10.10.10.100' -D 'svc_tgs' -w 'GPPstillStandingStrong2k18' -b 'dc=active,dc=htb' 
```

```
ldapsearch -x -H 'ldap://10.10.10.100' -D 'svc_tgs' -w 'GPPstillStandingStrong2k18' -b 'dc=active,dc=htb' -s sub "(&(objectCategory=person)(objectClass=user)(!(useraccountcontrol:1.2.840.113556.1.4.803:=2)))"1
```
```
ldapsearch -x -H 'ldap://10.10.10.100' -D 'SVC_TGS' -w 'GPPstillStandingStrong2k18' -b "dc=active,dc=htb" -s sub "(&(objectCategory=person)(objectClass=user)(!
(useraccountcontrol=514)))" serviceprinciplename 
```

## Chatsheet
https://gist.github.com/jonlabelle/0f8ec20c2474084325a89bc5362008a7
