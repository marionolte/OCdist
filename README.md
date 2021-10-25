# OCdist

$ java -jar OC.jar
Opitz MHService - OC.jar/0.0.4 - Mario Nolte

Options:
		-version 		-	print version information

		-crypt [-max <0..2>] [-custkey <custom key> -usecustkey] <-crypt|-uncrypt> <String|File>
					-	crypt or uncrypt a string or file

		
		-testssl <host> <port>	-	Test SSL Connection to the server and port 

		-sshcomm  [host=<host[localhost]>] [port=<port[22]>] [user=<User [account name]>] [-j <password file>] [-key <key file>] <command>
					-	send a single ssh command
		-portscan [-host <host>] [-pmin <min port>] [-pmax <max port>]	-	port  scanner 

		-testhttp <url> [url1,]	-	Test URL Connection to URL

		-checker  [-f <pattern file>] [-i <include pattern>] [-b <begin time>] [-e <end time>] <FILE|Directory>
       format time: DAY-MONTH-YEAR HH:MIN:SEC - example to use '01-MAR-2013 10:12:45' 

		-ldapsearch  [-h hostname] [-p port] [-D adminDN ] [-j passwordfile] [-a <simple|>] [-b baseDN ] [-f filter]  <attribut list>


		-ldapmodify  [-h hostname] [-p port] [-D adminDN ] [-j passwordfile] [[-f <file for operation of -o>] [-o <add|del|mod>:dn:attribute:value>] [-lf ldiffile] ]


		-ldapbind  [-h hostname] [-p port] [-D adminDN ] [-j passwordfile] [-b baseDN ]

		-ldapcopy  [-h hostname] [-p port] [-ssl] [-D adminDN] [-j passwordfile] [-modh modifyHost] [-modp port] [-modD adminDN] [-modj passwordfile] [-modssl] [-b baseDN] [-bc copyBaseDN] [-f filter] [-t copytemplate] [-pg <page-sizelimit>] [objectlist]
		example template file:
				#template: strict
				dn: ou=People|ou=Users
				objectClass: top person posixAccount inetOrgPerson
				gidNumber: 1000
				sn:
				givenname:
				mail: __givenname__.__sn__@example.com
				uid: __givenname(0,1)__sn(0,5)__
				uidnumber: {autoinc(1000)}
				loginShell: /bin/bash
				homeDirectory: /home/__uid__
				cn: __uid__
				userpassword: 1234

 	Information to the template:
 		__ 			before and after will take a value from a ldap attribute
 		(0,5)  			take a substring from 0 to 5 
 		ou=People|ou=Users 	replace  in the dn the ou=People part with ou=Users
 		autoinc(1000) 	will generate an auto integer incrimental value starting with the base 1000
 		strict in the #template	this with take over only the names attributes


		-ldapuserblk  [-h hostname <def:localhost>] [-p port <def:389>] [-a adminDN <def:cn=orcladmin> [-j passwordfile] [-b baseDN ] [-f filter] [-ssl <set ldaps schema>] [-o ldapCheck ] [ -of ldapCheckFile ] [-create] [-modh <hostname for modificaction>] [-modp <port for ldapserver modification> ] [ -modssl <set ldaps for modification>]| [-help <used per default>]


		-wlsconfig [-dest <script dir [/Users/SuMario/bin]>] [-reconfig] [-silient] <domaindir <domaindir1...>>
					-	Configure Wls Starting scripts in directory <dest>
		-wlsinfo <domainhome> [<-server <servername>]	-
					print domain use information

		-wlsrota  [-minsize <size 4k>] [-minold <days 3d>] [-maxold <days 30d>] [-savefile <pattern>] <domain dir> [<domain dir1> ..]
					weblogic domain logrotation

		-logrota  [-minsize <size 4k>] [-minold <days 3d>] [-maxold <days 30d>] [-savefile <pattern>] <dir> [<dir1> ..]
					apache|ohs logrotation

		-pwfile <filename>	-	store a password in a secure file

		-secure <filename>	-	generate a secure file from filename

		-unsecure <filename>	-	unsecure a secure file back to normal file




 $ ./java -jar OC.jar -version
 Opitz MHService - OC.jar/0.0.4 - Mario Nolte
