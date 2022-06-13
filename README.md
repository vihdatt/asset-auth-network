# Auth_Network

This is a school project for Cryptography taught by Dr.Nguyen Tan Khoi at Danang University of Science and Technology.

Sử dụng hyperledger fabric để tạo một mạng xác thực tài sản.
Trong github này có config mạng, config và code api, config và code ứng dụng.

Báo cáo cuối kì có thể xem tại đây: [Báo cáo cuối kì](MMH_BaoCao_Cuoiki_3.pdf)

# Prerequisites:
- Ubuntu-18.04
- Docker, docker compose: https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-18-04, https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04
- npm, node: https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04
- Go: https://www.digitalocean.com/community/tutorials/how-to-install-go-on-ubuntu-18-04
- Hyperledger Fabric Binaries and docker images: ```curl -sSL https://raw.githubusercontent.com/hyperledger/fabric/release-2.2/scripts/bootstrap.sh | bash -s``` and add ```/fabric-samples/bin``` to path

-> they have to be added into linux path

# Run:
1. git clone https://github.com/damtien444/Auth_Network.git
2. cd Auth_Network
3. Delete all old cryptographic file in api 1.4
4. Regenerate all crypto material in artifact by rerunning ```artifacts/channel/create-artifacts.sh```
7. Start the network by running ```start.sh```
8. Inside api-1.4, run ```npm install``` to install required node packages for the api server
9. Start the api server by running ```node app.js```, the server then start to listening on port 4000
10. Inside asset-authorize, run ```npm install``` to install required node packages for the application
11. Modify the ip address in react application api profile relative to your position in the network. If you access from the same host as the api server, then use localhost. Otherwise, use your IP (public IP and static route - if access through internet or private IP - if access through a LAN network).
12. Start the application server with ```npm start``` , application server will be on port 3000

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
