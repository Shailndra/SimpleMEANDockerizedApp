SimpleMEANDockerizedApp

1. I consider that you already have Docker, Angular and Nodejs installed in your system. Mongo and Nginx images will be pulled from Dockerhub.

2. Run docker-compose.yml ```#sudo docker-compose.yml up -d``` from the directory where you have docker-compose.yml.

3. Once all the containers are up which can be checked from ```#sudo docker ps``` you can go to the defined ports in the local machine to access them.

- Port ``4200`` for Angular
- Port ``3000`` for Nodejs
- Localhost for Nginx

4. Execute ```#sudo docker exec -it "container id" bash``` to go to the shell of the container. Once in it,

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

5. Displays the result of the query.
