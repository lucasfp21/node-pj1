cltr + shift + p
    para comecar a setar o ambiente

escolher a opcao dev containers
    
    * escolher a imagem base
    *
Customiar os arquivos:
    devcontainer.json
    docker-compose.yaml
    Dockerfile

rebuild em container

customizar o devcontainer.json com as info de indentificador de extensoes
    "customizations": {"vscode": {"extensions": [
		"ms-azuretools.vscode-docker"
	]}}

comando de inicializacao:
    no devcontainer.json
        "postCreateCommand": "npm install"

Add debug
    ctrl + shift + p
    debug add configuraions
        nodejs
            ele vai criar um arquivo launch.json
    f5 para iniciar o debug e f10 para pular os breakpoints
    
Criando o ambiente de PRD
    criamos um novo Dockerfile e um compose.yaml
    voltamos rodar localmente e usamos o compose para subir
        docker compose up -d --build
    