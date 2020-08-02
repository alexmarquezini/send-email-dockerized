# Envio de Email Dockerizado

__Essa aplicação é baseada no curso da Cod3r Cursos Online:__ _Docker, Essencial Para Programadores_.

Essa aplicação é muito básica, porém contém várias imagens e containers que interagem entre sí. Temos exemplos de proxy reversa com Nginx, fila de e-mails com Redis, e muito mais.

<img src="../master/img/apostila-docker.jpg" alt="Diagrama" width="600"/>

Para rodar esse pequeno sistema que mostra de forma abrangente e ao mesmo tempo muito concisa o uso do Docker, é só executar os seguintes comandos:

```
$ cd ./pasta/da/aplicação
$ docker-compose up -d --scale worker=3
```
_O comando_ `–scale` _cria 3 instâncias de_ `workers`, _que escala nossa aplicação de forma que, se um_ `sender` _está ocupado a tarefa é passada para outro._

Para monitorar os logs da aplicação, execute:

```
$ docker-compose logs -f -t
```
Para parar os containers você pode digitar `CTRL+C` para sair do log e logo após execute:

```
$ docker-compose down
```

<hr>

:exclamation: __Lembre-se que para rodar esse exemplo você precisa instalar o Docker em seu sistema operacional. Você pode encontrar mais informações [clicando aqui](https://www.docker.com/get-started).__ :tada:



