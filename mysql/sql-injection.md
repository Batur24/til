
# Sql Injection

`sql injection` is a common way to break down a system. The concept is pretty simple, people could use `string joint` to let illegal sql statement pass and return data.

for instance:
```c#
String userid = fromInputUserId;
String password = fromInputPassWord;
String sql = @"select * from user where userid='{userId}' and password='{passWord}'";
```
if the user input password: `test' or '1'='1`, this sql statement will return all user data. because `'1'='1'` will always be true.

To Prevent `sql injection`, use sql variable can achieve this.

```c#
set @userid = 'userid';
set @password = 'password';
SELECT * FROM v_user WHERE userid=@userid and password=@password;
```