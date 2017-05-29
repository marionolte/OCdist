# OCdist

$ java -jar OC.jar 
Options:
		-version 		-	print version information

		-crypt [-max <0..2>] [-custkey <custom key> -usecustkey] <-crypt|-uncrypt> <String|File>
					-	crypt or uncrypt a string or file

		-testssl <host> <port>	-	Test SSL Connection to the server and port 

		-sshcomm  [host=<host[localhost]>] [port=<port[22]>] [user=<User [account name]>] [-j <password file>] [-key <key file>] <command>
					-	send a single ssh command
		-portscan [-host <host>] [-pmin <min port>] [-pmax <max port>]	-	port  scanner 

		-testhttp <url> [url1,]	-	Test URL Connection to URL

		-ldap -D <bindDN> -j <Password File> <-h <Host>> <-p <Port>> -filter <filter> -b <baseDN>

		-wlsconfig [-dest <script dir [.]>] <domaindir <domaindir1...>>
					-	Configure Wls Starting scripts in directory <dest>

		-wlsinfo <domainhome> [<-server <servername>]	-
					print domain use information

		-wlsrota  [-minsize <size 4k>] [-minold <days 3d>] [-maxold <days 30d>] [-savefile <pattern>] <domain dir> [<domain dir1> ..]
					weblogic domain logrotation

		-logrota  [-minsize <size 4k>] [-minold <days 3d>] [-maxold <days 30d>] [-savefile <pattern>] <dir> [<dir1> ..]
					apache|ohs logrotation

		-pwfile <filename>	-	store a password in a secure file

