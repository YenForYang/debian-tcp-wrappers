SUMMARY OF MANUAL LABOR


fakeroot debian/rules clean
mkdir shared
icc -g -Wformat -march=native -pipe -Wformat-security -D_FORTIFY_SOURCE=2 -DFACILITY=LOG_DAEMON -DHOSTS_ACCESS  -DNETGROUP    -DDAEMON_UMASK=022 -DREAL_DAEMON_DIR=\"/usr/sbin\" -DPROCESS_OPTIONS -DACLEXEC -DKILL_IP_OPTIONS -DSEVERITY=LOG_INFO	 -DRFC931_TIMEOUT=10  -DHOSTS_DENY=\"/etc/hosts.deny\" -DHOSTS_ALLOW=\"/etc/hosts.allow\"   -DSYS_ERRLIST_DEFINED -DHAVE_STRERROR -DHAVE_WEAKSYMS -DINET6=1 -Dss_family=__ss_family -Dss_len=__ss_len -fpic  hosts_access.c options.c shell_cmd.c rfc931.c eval.c hosts_ctl.c refuse.c percent_x.c clean_exit.c weak_symbols.c fromhost.c fix_options.c socket.c tli.c workarounds.c update.c misc.c diag.c percent_m.c myvsyslog.c -o shared/libwrap.so.0.7.6 -Bsymbolic-functions -shared -Wl,-soname=libwrap.so.0 -Wl,--version-script=libwrap.lds -lnsl
ln -sf libwrap.so.0.7.6 shared/libwrap.so.0
ln -sf libwrap.so.0 shared/libwrap.so

icc -g -Wformat -march=native -pipe -Wformat-security -D_FORTIFY_SOURCE=2 -DFACILITY=LOG_DAEMON -DHOSTS_ACCESS  -DNETGROUP    -DDAEMON_UMASK=022 -DREAL_DAEMON_DIR=\"/usr/sbin\" -DPROCESS_OPTIONS -DACLEXEC -DKILL_IP_OPTIONS -DSEVERITY=LOG_INFO	 -DRFC931_TIMEOUT=10  -DHOSTS_DENY=\"/etc/hosts.deny\" -DHOSTS_ALLOW=\"/etc/hosts.allow\"   -DSYS_ERRLIST_DEFINED -DHAVE_STRERROR -DHAVE_WEAKSYMS -DINET6=1 -Dss_family=__ss_family -Dss_len=__ss_len -o tcpd tcpd.c -Lshared -lwrap
icc -g -Wformat -march=native -pipe -Wformat-security -D_FORTIFY_SOURCE=2 -DFACILITY=LOG_DAEMON -DHOSTS_ACCESS  -DNETGROUP    -DDAEMON_UMASK=022 -DREAL_DAEMON_DIR=\"/usr/sbin\" -DPROCESS_OPTIONS -DACLEXEC -DKILL_IP_OPTIONS -DSEVERITY=LOG_INFO	 -DRFC931_TIMEOUT=10  -DHOSTS_DENY=\"/etc/hosts.deny\" -DHOSTS_ALLOW=\"/etc/hosts.allow\"   -DSYS_ERRLIST_DEFINED -DHAVE_STRERROR -DHAVE_WEAKSYMS -DINET6=1 -Dss_family=__ss_family -Dss_len=__ss_len -o tcpdmatch tcpdmatch.c fakelog.c inetcf.c scaffold.c -Lshared -lwrap
icc -g -Wformat -march=native -pipe -Wformat-security -D_FORTIFY_SOURCE=2 -DFACILITY=LOG_DAEMON -DHOSTS_ACCESS  -DNETGROUP    -DDAEMON_UMASK=022 -DREAL_DAEMON_DIR=\"/usr/sbin\" -DPROCESS_OPTIONS -DACLEXEC -DKILL_IP_OPTIONS -DSEVERITY=LOG_INFO	 -DRFC931_TIMEOUT=10  -DHOSTS_DENY=\"/etc/hosts.deny\" -DHOSTS_ALLOW=\"/etc/hosts.allow\"   -DSYS_ERRLIST_DEFINED -DHAVE_STRERROR -DHAVE_WEAKSYMS -DINET6=1 -Dss_family=__ss_family -Dss_len=__ss_len -o try-from try-from.c fakelog.c -Lshared -lwrap
icc -g -Wformat -march=native -pipe -Wformat-security -D_FORTIFY_SOURCE=2 -DFACILITY=LOG_DAEMON -DHOSTS_ACCESS  -DNETGROUP    -DDAEMON_UMASK=022 -DREAL_DAEMON_DIR=\"/usr/sbin\" -DPROCESS_OPTIONS -DACLEXEC -DKILL_IP_OPTIONS -DSEVERITY=LOG_INFO	 -DRFC931_TIMEOUT=10  -DHOSTS_DENY=\"/etc/hosts.deny\" -DHOSTS_ALLOW=\"/etc/hosts.allow\"   -DSYS_ERRLIST_DEFINED -DHAVE_STRERROR -DHAVE_WEAKSYMS -DINET6=1 -Dss_family=__ss_family -Dss_len=__ss_len -o safe_finger safe_finger.c
icc -g -Wformat -march=native -pipe -Wformat-security -D_FORTIFY_SOURCE=2 -DFACILITY=LOG_DAEMON -DHOSTS_ACCESS  -DNETGROUP    -DDAEMON_UMASK=022 -DREAL_DAEMON_DIR=\"/usr/sbin\" -DPROCESS_OPTIONS -DACLEXEC -DKILL_IP_OPTIONS -DSEVERITY=LOG_INFO	 -DRFC931_TIMEOUT=10  -DHOSTS_DENY=\"/etc/hosts.deny\" -DHOSTS_ALLOW=\"/etc/hosts.allow\"   -DSYS_ERRLIST_DEFINED -DHAVE_STRERROR -DHAVE_WEAKSYMS -DINET6=1 -Dss_family=__ss_family -Dss_len=__ss_len -o tcpdchk tcpdchk.c fakelog.c inetcf.c scaffold.c -Lshared -lwrap



icc -g -Wformat -march=native -pipe -Wformat-security -D_FORTIFY_SOURCE=2 -DFACILITY=LOG_DAEMON -DHOSTS_ACCESS  -DNETGROUP    -DDAEMON_UMASK=022 -DREAL_DAEMON_DIR=\"/usr/sbin\" -DPROCESS_OPTIONS -DACLEXEC -DKILL_IP_OPTIONS -DSEVERITY=LOG_INFO	 -DRFC931_TIMEOUT=10  -DHOSTS_DENY=\"/etc/hosts.deny\" -DHOSTS_ALLOW=\"/etc/hosts.allow\"   -DSYS_ERRLIST_DEFINED -DHAVE_STRERROR -DHAVE_WEAKSYMS -DINET6=1 -Dss_family=__ss_family -Dss_len=__ss_len -ipo-c hosts_access.c  options.c  shell_cmd.c  rfc931.c  eval.c  hosts_ctl.c  refuse.c  percent_x.c  clean_exit.c  weak_symbols.c  fromhost.c  fix_options.c  socket.c  tli.c  workarounds.c  update.c  misc.c  diag.c  percent_m.c  myvsyslog.c -o libwrap.o

xiar crvs libwrap.a libwrap.o

touch debian/.stamp-build

fakeroot debian/rules binary
