![docker-image](https://cloud.githubusercontent.com/assets/1865566/20648336/132e3ec6-b48b-11e6-8738-f4e111cfe335.png)


# Comandos Docker

Comandos mais usados no Docker.

**Inicia um container com Ubuntu e exibe uma mensagem na tela**

`$ docker run ubuntu /bin/echo "Hello Docker"`

**Faz download de uma imagem**

`$ docker pull mysql`

**Lista todas imagens**

`$ docker images`

**Lista os containers em execução**

`$ docker ps`

**Lista os containers criados**

`$ docker ps -a`

**Executa o MySQL**

`$ docker run --name database -e MYSQL_ROOT_PASSWORD=teste123 -d mysql`

**Instala o Wordpress, onde: --name define o nome do container, -e define as variáveis de ambiente, -p define as portas do container, --link faz o link com o container do mysql**

`$ docker run --name blog --link database:mysql -e WORDPRESS_DB_PASSWORD=teste123 -p 80:80 -d wordpress`

**Entra dentro de um container em execução e executa o bash**

`$ docker exec -i -t blog bash`

**Cria um container realizando o exec**

`$ docker run -it ubuntu bash`

**Realiza a destruição de um container**

`$ docker rm [id ou nome]`

**Para um container**

`$ docker stop [nome]`

**Iniciar um container**

`$ docker start [nome]`

**Remover mais de um container ao mesmo tempo**

`$ docker rm $(docker ps -qa)`

**Lista todos id dos containers ativos**

`$ docker ps -qa`

**Remover imagem do container**

`$ docker rmi [id ou nome]`

****

`$`

****

`$`

****

`$`




