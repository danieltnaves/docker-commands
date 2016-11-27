![docker-image](https://cloud.githubusercontent.com/assets/1865566/20648336/132e3ec6-b48b-11e6-8738-f4e111cfe335.png)


# Comandos Docker

Comandos mais usados no Docker.

**Inicia um container com Ubuntu e exibe uma mensagem na tela**

`$ docker run ubuntu /bin/echo "Hello Docker"`

**Faz download de uma imagem**

`$ docker pull mysql`

**Lista todas imagens**

`$ docker images`

**Lista os containers incluindo os nomes**

`$ docker ps -a`

**Executa o MySQL**

`$ docker run --name database -e MYSQL_ROOT_PASSWORD=teste123 -d mysql`

**Instala o Wordpress, onde: --name define o nome do container, -e define as variáveis de ambiente, -p define as portas do container, --link faz o link com o container do mysql**

`$ docker run --name blog --link database:mysql -e WORDPRESS_DB_PASSWORD=teste123 -p 80:80 -d wordpress`

****

`$`

****

`$`

****

`$`

****

`$`

****

`$`

****

`$`

****

`$`

****

`$`

****

`$`

****

`$`

****

`$`




