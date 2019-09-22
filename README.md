**SimpleMEANDockerizedApp**

I consider that you already have Docker, Angular and Nodejs installed in your system. Mongo and Nginx images will be pulled from Dockerhub. 

Run docker-compose.yml 
```#sudo docker-compose.yml up -d``` from the directory where you have docker-compose.yml.

Once all the containers are up which can be checked from ```#sudo docker ps``` you can go to the defined ports in the local machine
to access them. 
1. Port ``4200`` for Angular
2. Port ``3000`` for Nodejs
3. Localhost for Nginx

Execute ```#sudo docker exec -it "container id" bash``` to go to the shell of the container. Once in it, 
```
#mongo (runs Mongodb environment).
#show dbs  (displays dbs).
#use database1  (create databse1)
*(write query)
#db.people.save({ firstname: "Nic", lastname: "Raboy" })
#db.people.save({ firstname: "Maria", lastname: "Raboy" })
#db.people.save({ firstname: "Joseph", lastname: "Martin" })
#db.people.save({ firstname: "Rick", lastname: "Dolhert" })
#db.people.save({ firstname: "Jon", lastname: "Doe" })
*(query for data)
#db.people.find({ firstname: "Nic" })
```
Displays the result of the query. 
