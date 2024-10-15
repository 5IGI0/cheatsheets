# MySQL Cheatsheet

## Create User
sources: [CREATE USER statement](https://dev.mysql.com/doc/refman/8.4/en/create-user.html), [User Syntax](https://dev.mysql.com/doc/refman/8.4/en/account-names.html)
```sql
-- without host whitelist
CREATE USER '<USER>' IDENTIFIED BY '<PASSWORD>';
-- with host whitelist
CREATE USER '<USER>'@'<HOST(domain/addr[/CDIR]>' IDENTIFIED BY '<PASSWORD>';
```

## Grant Permission
sources: [GRANT statement](https://dev.mysql.com/doc/refman/8.4/en/grant.html), [Privilege List](https://dev.mysql.com/doc/refman/8.4/en/privileges-provided.html), [User Syntax](https://dev.mysql.com/doc/refman/8.4/en/account-names.html) \
short privilege list: ``ALL``, ``ALTER``, ``CREATE``, ``DELETE``, ``DROP``, ``INSERT``, ``SELECT``, ``UPDATE`` 
```sql
GRANT <PRIVILEGES, ...> ON <DATABASE>.<TABLE (or * for all)> TO <USER>;
FLUSH PRIVILEGES;
```
