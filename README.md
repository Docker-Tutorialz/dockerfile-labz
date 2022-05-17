## Dockerfile Labz

1.  Primeira instrucao dentro de um *dockerfile* e o comando *FROM*

```bash
FROM - especifica uma imagem que sirva de base para a app (Java, NGINX, Ubuntu, Node, Debian, Maven, Banco de Dados).
COPY - procura um documento, arquivo que esteja dentro do mesmo nivel do *Dockerfile* e copia ele para dentro do container.
ADD - faz a mesma coisa que o *COPY*, 
RUN -  executa algum comando no container.
CMD = tambem executa comando no container, mas somente quando o container estiver inicializado.
ENTRYPOINT - faz a mesma coisa que o *CMD*, quando estao juntos, o *CMD* entra como parametro dele.

```

2.  Exemplo de *Dockerfile*

```dockerfile
FROM openjdk
COPY
```
