# TP2_devops

Question 1 , 2 ,3
- npm install
- node server.js,

apres je regarde le localhost
dans le terminal 

- docker pull mariadb

Question 4
  Je viens de lancer le MARIA DB 
  j'ai decommenter le code dans le index.js et remplacer par les bonnes variables.
  Pour rebuild une img il faut utiliser la commande CMD +le chemin + -d
  
Question 5 
```yaml
version: '3'
services:
  app:
    image: node:latest
    ports:
      - "3000:3000"
    volumes:
      - ./app:/app
    environment:
      - DATABASE_URL=mongodb://db/myapp
    depends_on:
      - db
  db:
    image: mongo:latest
    volumes:
      - ./data:/data/db
      
 ```
