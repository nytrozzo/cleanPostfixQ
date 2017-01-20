Tool of emergency to clean Postfix queues by Sender | email content

```
 ~ Usage : cleanPostfixQ [OPTIONS] [REGEX]

Options:
--------
# Options
-dbs |--deletebysender : Delete queued email when matching sender regex
-dbc |--delbycontent : Delete queued email when matching content regex
-y : Force 'yes' answer before deleting -  can by added on option -dbs while used in crontab or script

NOTES : 
- The option -dbc, if used with no regex, will use a default pattern included in the program.
- -dbc option include by default the deletion of MAILER-DAEMON email
- [REGEX] has the format interpreted by grep -E ''

Example of uses :
cleanPostfixQ -dbs -y MAILER-DAEMON
cleanPostfixQ -dbs 'MAILER-DAEMON|titi@toto.com|loveyou.cz'
cleanPostfixQ -dbc 
cleanPostfixQ -dbc 'sex|easy money|offshore|nice student'


```

