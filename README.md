# OCdist

MHService - macmario-core-io.jar/0.0.7 - Mario Nolte

Options:
                -version                -       print version information

                -crypt [-max <0..2>] [-custkey <custom key> -usecustkey] <-crypt|-uncrypt> <String|File>
                                        -       crypt or uncrypt a string or file


                -testssl <host> <port>  -       Test SSL Connection to the server and port

                -sshcomm  [host=<host[localhost]>] [port=<port[22]>] [user=<User [account name]>] [-j <password file>] [-key <key file>] <command>
                                        -       send a single ssh command
                -portscan [-host <host>] [-pmin <min port>] [-pmax <max port>]  -       port  scanner

                -testhttp <url> [url1,] -       Test URL Connection to URL

                -checker  [-f <pattern file>] [-i <include pattern>] [-b <begin time>] [-e <end time>] <FILE|Directory>
       format time: DAY-MONTH-YEAR HH:MIN:SEC - example to use '01-MAR-2013 10:12:45'

                -wlsconfig [-dest <script dir [/home/sumario/bin]>] [-reconfig] [-silient] <domaindir <domaindir1...>>
                                        -       Configure Wls Starting scripts in directory <dest>
                -wlsinfo <domainhome> [<-server <servername>]   -
                                        print domain use information

                -wlsrota  [-minsize <size 4k>] [-minold <days 3d>] [-maxold <days 30d>] [-savefile <pattern>] <domain dir> [<domain dir1> ..]
                                        weblogic domain logrotation

                -logrota  [-minsize <size 4k>] [-minold <days 3d>] [-maxold <days 30d>] [-savefile <pattern>] <dir> [<dir1> ..]
                                        apache|ohs logrotation

                -pwfile <filename>      -       store a password in a secure file

                -secure <filename>      -       generate a secure file from filename

                -unsecure <filename>    -       unsecure a secure file back to normal file

                -mwinfo                 -       get Middleware information


 $ ./java -jar OC.jar -version
 Opitz MHService - OC.jar/0.0.6 - Mario Nolte
