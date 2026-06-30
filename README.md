# Jenkins

## Inledning

Tanken med labben var att labba med tekniker som är "buzzwords" i branschen.

## Utförande

Installera [Jenkins](https://www.jenkins.io/doc/book/installing/docker/)

Skapa en dockerfile

## Lärdommar

* Lägg till `--volume jenkins-data:/var/jenkins_home` i `docker run` för att koppla lagring mellan värddatorn och Docker-containern. Så att det lagras i volymen istället för bara i containern.

* Lägg även till den här raden `--volume jenkins-docker-certs:/certs/client:ro` så att Jenkins kan läsa certifikaten för säker anslutning till Docker-daemonen.

* Öppna vald port mellan värddatorn och containern med `-p 8080:8080`
