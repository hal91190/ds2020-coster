# microservice_project
Le projet  gére la scolarité(enseignant et cours) avec des microservices pour chaque entité, nous avons utilisé: 
## Outils : 
  - Maven 
  - Spring Boot
  - Docker : pour le déploiement sur des conteneurs
  - Api REST
  - Derby
  - Feign
  - Eureka
  - JPA
  - Boostrap
  
## Mise en oeuvre : 
### projet parent
- docker-compose : 
  - lancer les images
  - création de réseau pour les conteneurs
  - création  de volume 
  
### Microservices : 
- Cours et Enseignant
  - opération CRUD
  - Maven multimodule
  - dependance "docker spotify" :  pour la gestion et exploitation de l'image lors du packaging 
  - fichier xml "assembly" pour l'assemblage du pojet
  - dockerfile : pour la generation de l'image 
  - enrégistrement au serveur eureka
- Microservice "cours-enseignant"
  - microservice pour l'affectation d'un enseignant à un cours
  - enrégistrement sur le serveur eureka
  - dokerfile
  
### Microservice Discovery : 
- "Serveur eureka" : pour permettre aux applications de s’enregistrer pour qu’elles se voient mutuellement. 
![image2](https://github.com/ousmanesn8/Myimages/blob/master/Capture%20du%202020-03-11%2000-18-58.png)
### Client REST
- communique avec les microservices cours, enseignant et cours-enseignant
- interface d'acceuil
![image2](https://github.com/ousmanesn8/Myimages/blob/master/Capture%20du%202020-03-11%2000-39-58.png)
## Execution :
   - > se postionner sur le projet parent 
   - > mvn package
   - > docker-compose up
- Pour acceder au client qui appele les deux services, il faut aller à l'URL suivant :
  - http://localhost:9093/ 
