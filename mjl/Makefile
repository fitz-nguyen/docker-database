run-autossh: # run on fitzfsc
	# server database mjl_develop
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 5432:postgres.mjl.svc.fiisoft.net:5432 -f -NT pi@fitznguyen.ddns.net
	# nextcloud
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 7500:localhost:9000 -f -NT pi@fitznguyen.ddns.net
	# ssh to fitzfsc
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 2053:localhost:22 -f -NT pi@fitznguyen.ddns.net
	# ssh to fitznguyen imac FSC
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 2054:10.0.1.3:22 -f -NT pi@fitznguyen.ddns.net
	# server postgrest for database mjl_develop
# 	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 3000:localhost:3000 -f -NT pi@fitznguyen.ddns.net
# 	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 3001:localhost:3001 -f -NT pi@fitznguyen.ddns.net
# 	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 3002:localhost:3002 -f -NT pi@fitznguyen.ddns.net
# 	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 3003:localhost:3003 -f -NT pi@fitznguyen.ddns.net
# 	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 3004:localhost:3004 -f -NT pi@fitznguyen.ddns.net
# 	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 3005:localhost:3005 -f -NT pi@fitznguyen.ddns.net
# 	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 3006:localhost:3006 -f -NT pi@fitznguyen.ddns.net
# 	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 27017:localhost:27017 -f -NT pi@fitznguyen.ddns.net
	# api mjl develop
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 7010:localhost:7010 -f -NT pi@fitznguyen.ddns.net

dump-db:
	pg_dump -h postgres.mjl.svc.fiisoft.net -U mjl_develop mjl_develop > /Users/fitznguyen/Documents/Backup/imac-fsc/Database/mjl_develop.dump
# 	pass: peo6bzwyawkl7c7T83yfFYSzddOl7qmr2Lk=

restore-db:
	psql -U fitznguyen mjl_develop < /Users/fitznguyen/Documents/Backup/imac-fsc/Database/mjl_develop.dump

ls:
	ls