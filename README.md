# Hyperledger
1.	Start docker toolbox terminal
2.	In docker terminal, Run the command - docker-compose -f sawtooth-default.yaml up
3.	Open another docker terminal, Run this command - docker exec -it sawtooth-shell-default bash
4.	To check the connectivity to confirm that a validator is running and reachable from inside docker container - curl http://rest-api:8008/blocks or from host machine - curl http://localhost:8008/blocks
5.	In this step we must generate keys for users, to generate private key and public key for user named userA - sawtooth keygen userA
6.	For userB follow above command - sawtooth keygen userB
7.	Now, to start the tic-tac-toe game run - xo create game  --url http://rest-api:8008  -- userA
8.	To display information for game in states - xo list  --url http://rest-api:8008  -- userA
9.	Now userA will make the first move - xo take game 5  --url http://rest-api:8008  --userA . Here, userA will mark “X” at position 5 in the grid of 9.
10.	For userB, step g, h and i will be same.
