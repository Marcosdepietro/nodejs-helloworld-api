# NodeJs, helloworld API for test propouses.

This is a simple API that returns a welcome message.

## Run your local environment

### Clone the repository
```bash
git clone https://github.com/edgaregonzalez/nodejs-helloworld-api.git
```

### Install dependencies
```bash
npm install
```

### Run the tests
```bash
npm test
```

### Start the server
```bash
npm start
```

### Make a request
```bash
curl http://localhost:3000
```
# Desafio 2:

1. **Ngrok**
-Primero se debe instalar ngrok desde https://ngrok.com/  y crear una cuenta 

Desde una instancia en Ubuntu, clonar el repositorio mediante el comando “git clone https://github.com/edgaregonzalez/nodejs-helloworld-api.git” 

Desde la pagina de ngrok ir a Linux, copiar y pegar el codigo para instalarlo 
curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc \ 
	| sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null \ 
	&& echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \ 
	| sudo tee /etc/apt/sources.list.d/ngrok.list \ 
	&& sudo apt update \ 
	&& sudo apt install ngrok

-Luego correr el siguiente comando para agregar tu token: 
 
ngrok config add-authtoken 2gFVw7zFfzHTbRg184UpZouYbLM_3FJuZaNBvkBDYCBoTxFAx 
 
Para levantar el servicio de ngork ejecutar lo siguiente: 
 
ngrok http http://localhost:8080

-Ir a la URL de Forwarding e iniciar sesión en Jenkins

2. **Configurar el Webhook de Github:**
-En Payload URL escribimos la URL seguido de "github-webhook/"
-En Content Type seleccionamos ”application/json"
-En las acciones seleccionamos Pull request y Pushes

3. **Jenkins**
-Instalar el plugin de NodeJs
-Configurar NodeJS y su respectiva versión en “Tools”

4. **NodeJs**
-Descargar NodeJs con los siguientes comandos (para Linux utilizando NVM): 
 
```bash
# installs NVM (Node Version Manager) 

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash 

# download and install Node.js 

nvm install 20 

# verifies the right Node.js version is in the environment 

node -v # should print `v20.13.1` 

# verifies the right NPM version is in the environment 

npm -v # should print `10.5.2` 
```
