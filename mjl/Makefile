run-autossh: # run on fitzfsc
	# server database mjlo_develop
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 5432:postgres.mjl.svc.fiisoft.net:5432 -f -NT pi@fitznguyen.ddns.net
	# nextcloud
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 9000:localhost:8080 -f -NT pi@fitznguyen.ddns.net
	# ssh to fitzfsc
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 2053:localhost:22 -f -NT pi@fitznguyen.ddns.net
	# ssh to fitznguyen imac FSC
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 2054:10.0.1.3:22 -f -NT pi@fitznguyen.ddns.net
	# server postgrest for database mjl_develop
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 2053:localhost:22 -f -NT pi@fitznguyen.ddns.net

dump-db:
	pg_dump -h postgres.mjl.svc.fiisoft.net -U mjl_develop mjl_develop > /Users/fitznguyen/Documents/Backup/imac-fsc/Database/mjl_develop.dump
# 	pass: peo6bzwyawkl7c7T83yfFYSzddOl7qmr2Lk=

restore-db:
	psql -U fitznguyen mjl_develop < mjl_develop.dump