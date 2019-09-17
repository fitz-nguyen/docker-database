run-autossh:
	sudo autossh -R 7010:localhost:7010 -f -NT ttnt2805@35.186.152.112
	sudo autossh -R 3000:localhost:3000 -f -NT ttnt2805@35.186.152.112
	sudo autossh -R 3001:localhost:3001 -f -NT ttnt2805@35.186.152.112
	sudo autossh -R 3002:localhost:3002 -f -NT ttnt2805@35.186.152.112
	sudo autossh -R 3003:localhost:3003 -f -NT ttnt2805@35.186.152.112
	sudo autossh -R 3004:localhost:3004 -f -NT ttnt2805@35.186.152.112
	sudo autossh -R 2053:localhost:22 -f -NT ttnt2805@35.186.152.112

dump-db:
	pg_dump -h postgres.mjl.svc.fiisoft.net -U mjl_develop mjl_develop > /Users/fitznguyen/Documents/Backup/imac-fsc/Database/mjl_develop.dump
# 	pass: peo6bzwyawkl7c7T83yfFYSzddOl7qmr2Lk=

restore-db:
	psql -U fitznguyen mjl_develop < mjl_develop.dump