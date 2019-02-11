# Projeto - woopPauta
Teste para Desenvolvedor(a) Backend do Woop Sicredi

## Setup´s
==DOCKER + MONGO==

	...Docker (Windows) --> https://hub.docker.com/editions/community/docker-ce-desktop-windows
  		...Validar a instalação:
			docker version
			docker run hello-world
		...Subir um "Mongo", command´s:
			.docker pull mongo
				[Instalar o MongoDB]
			.docker images
				[Visualizar imagem baixada]
			.docker run --name sicredi-mongo -p 27017:27017 -d mongo
				[Subir um contêiner]
			.docker exec -it some-mongo mongo admin
				[Executar o Administrador do MongoDB]
			.docker ps -a
				[Verifica o estado atual dos contêineres]
			.docker stop sicredi-mongo
				[Parar o contêiner criado]
			.docker start sicredi-mongo
				[Iniciar com o comando]
			.docker rm sicredi-mongo
				[Remover um contêiner]

		...MongoDB
			http://localhost:27017 --> Verificar
			...command:
				.show dbs
					[Verificar os bancos criados]
				.use local
					[Determinado banco]
				.show collections
					[Coleções existentes deste banco]
				.exit
					[Sair do administrador]==SPRING INITIALIZR==

## Sites Uteis
	==SPRING INITIALIZR==
	https://start.spring.io/

	==GITIGNORE INITIALIZR==
	https://www.gitignore.io/
	
## Proejeto
	Com o MongoDb rodando com sucesso...
	
	Rodar applicação: 
		Eclipse:
			.Pauta > Botão direitor em cima de "PautaApplication.java" e Selecionar: "Run As..." "Java Application"
	
		Maven:
			.Pauta > No diretorio da aplicação rode a linha de commando: "mvn spring-boot:run"
		
		"No ar" em: http://localhost:8090/
	
	Acessar Swagger:
		.Pauta: http://localhost:8090/swagger-ui.html
	
	Tecnologias: Docker, Mongo, Spring Boot, Spring Cloud, Java8, Rest, ...
		
## ++Para Melhorar++
	.Documentação Swagger
			http://springfox.github.io/springfox/docs/current/

	.Cliente Rest
		Melhorar tipo dados:
			.LocalDateTime
		
	.Adicionar Feign client
			Separar mais granularmente a aplicação.
				.. Exemplo: Separar o Eleitor. Deixar ele Isolado, seu CRUD e usar Spring Cloud (Feign).

	.Adicionar testes unitário
			Junit, Mockito, MockMvc,...

