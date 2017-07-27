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

**Executa um comando dentro do container retornando essas informações para o terminal local**

`$ docker exec -it [id ou nome] ps aux`

**Mata um container que não está respondendo**

`$ docker kill [id ou nome]`

**Cria um container descartável que será delatado no momento do exit**

`$ docker run --rm -it ubuntu bash`

**Comita as alterações feitas em um container para imagem (imagem/apache indica que um fork será feito da imagem principal)**

`$ docker commit -m "instalação do apache" [nome ou id do container] [imagem]/apache`

**Cria um container fazendo o mapeamento de portas 8080 indica a porta local da máquina e 80 a porta para qual será mapeada dentro do container**

`$ docker run -it -p 8080:80 ubuntu/apache bash`

**Exemplo de arquivo Dockerfile (Um arquivo Dockerfile possui uma série de instruções para montagem de uma imagem de forma automatizada)**

FROM ubuntu //indica a imagem base a ser utilizada

RUN apt-get update && apt-get install -y apache2 //comando a ser executado na criação da imagem

EXPOSE 80 //porta que será exposta

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"] //inicialização do processo do Apache

**Realiza build do Dockerfile, o . indicar o diretório onde está o arquivo Dockerfile**

`$ docker build -t ubuntu/apache .`

**Retornar os dados do container**

`$ docker inspect [id ou nome]`

**Lista logs de um container**

`$ docker logs -f [id ou nome]`

**Renomear tag da imagem**

`$ docker tag nome_antigo nome_novo`

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




