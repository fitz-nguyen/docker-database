run-autossh: # run on fitzfsc
	# server database fsc_develop
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 5433:localhost:5433 -f -NT pi@fitznguyen.ddns.net
	autossh -o "ServerAliveInterval 60" -o "ServerAliveCountMax 180" -R 8011:localhost:8011 -f -NT pi@fitznguyen.ddns.net

sync:
	sudo rsync -a --delete -e 'ssh -p 2053' fitzfsc@fitznguyen.ddns.net:/home/fitzfsc/Workspace/FSC