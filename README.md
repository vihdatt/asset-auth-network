# Auth_Network

This is a school project for Cryptography taught by Dr.Nguyen Tan Khoi at Danang University of Science and Technology.

Implement a hyperledger fabric network named Asset Authentication Network.

The final documentation for this project could be found here: [doccument](MMH_BaoCao_Cuoiki_3.pdf)

# Prerequisites:
- Ubuntu 18
- Docker, docker compose
- npm, node
- Go
- Hyperledger Fabric Binaries and docker images
-> they have to be added into linux path

# Run:
1. Delete all old cryptographic file in api 1.4
2. Regenerate all crypto material in artifact by rerunning ```artifacts/channel/create-artifacts.sh```
3. Start the network by running ```start.sh```
4. Inside api-1.4, run ```npm install``` to install required node packages for the api server
5. Start the api server by running ```node app.js```, the server then start to listening on port 4000
6. Inside asset-authorize, run ```npm install``` to install required node packages for the application
7. Modify the ip address in react application api profile relative to your position in the network. If you access from the same host as the api server, then use localhost. Otherwise, use your IP (public IP and static route - if access through internet or private IP - if access through a LAN network).
8. Start the application server with ```npm start``` , application server will be on port 3000

# Interact with the api server using these endpoints:
1. Import this collection of endpoint using Postman: https://www.getpostman.com/collections/401b1a02ed1330385449
2. Config your collection variable to suitable values.
3. First to register a user to get an access token.
4. Use that access token to trigger all other endpoints.

# Interact with the application 
Using a browser to open port 3000

# Features:
1. Create,
2. Manage ownership,
3. and delete an ownership.
