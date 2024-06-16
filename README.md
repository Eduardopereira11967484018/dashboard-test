Usando docker compose para executar o aplicativo localmente
Certifique-se de já ter Node, Docker, Docker Compose instalados em sua máquina

https://docs.docker.com/engine/install/
https://nodejs.org/en/download
https://github.com/docker/compose
Execute o seguinte comando:

Este comando é necessário para ser executado na primeira vez ou sempre que alterarmos docker-compose.yaml

docker-compose up --build --no-recreate -d
Na próxima vez, executaremos apenas:

docker-compose up -d
Listar contêineres:

docker-compose ps
Faça login no contêiner e execute o seguinte comando:

docker exec -it vite_docker sh
Depois dessa execução:

npm i && npm run dev
Por fim, abra o navegador e execute:

http://localhost:8080
Como encaixar imagens:
Crie Dockerfile como no repositório.
Dockerizar imagem
docker build -t cc-react-admin-ui:latest .
Execute a imagem do Docker
docker run -d -p 5173:5173 cc-react-admin-ui:latest
Implantar no Github
Configure a base vite.config.ts: "/[REPO_NAME]/"
base: "/cc-react-admin-ui/"
Crie deploy.yml .github/workflows/deploy.yml

Habilitar permissão de fluxos de trabalho

imagem
Visite Ações para visualizar o status da implantação
imagem
Visite as páginas para publicar o aplicativo
imagem
