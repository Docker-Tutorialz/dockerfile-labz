## Dockerfile Labz

1.  Primeira instrucao dentro de um *dockerfile* e o comando *FROM*

```bash
FROM - especifica uma imagem que sirva de base para a app (Java, NGINX, Ubuntu, Node, Debian, Maven, Banco de Dados).
COPY - procura um documento, arquivo que esteja dentro do mesmo nivel do *Dockerfile* e copia ele para dentro do container.
ADD - faz a mesma coisa que o *COPY*, 
RUN -  executa um comando durante a execucao do container (no momento de build da imagem).
CMD = tambem executa comando no container, mas somente quando o container estiver inicializado.
ENTRYPOINT - faz a mesma coisa que o *CMD*, quando estao juntos, o *CMD* entra como parametro dele.
WORKDIR - 
```

2.  Exemplo de *Dockerfile* usando a imagem do *debian*

```dockerfile
FROM debian

RUN apt-get update && apt-get install -y apache2 && apt-get clean
ENV APACHE_LOCK_DIR="/var/lock"
ENV APACHE_PID_FILE="/var/run/apache2.pid"
ENV APACHE_RUN_USER="www-data"
ENV APACHE_RUN_GROUP="www-data"
ENV APACHE_LOG_DIR="/var/log/apache2"

LABEL description="Webserver"

VOLUME /var/www/html/
EXPOSE 80
```
