# iaconn

Este projeto utiliza Quarkus, o Framework Java Supersônico Subatômico.

Se você quiser aprender mais sobre Quarkus, por favor visite o site: <https://quarkus.io/>.

## Executando a aplicação em modo de desenvolvimento

Você pode executar sua aplicação em modo de desenvolvimento, o que permite live coding, usando:

```shell script
./mvnw quarkus:dev
```

> **_Nota:_**  Quarkus agora vem com uma Dev UI, que está disponível apenas no modo de desenvolvimento em <http://localhost:8080/q/dev/>.

## Empacotando e executando a aplicação

A aplicação pode ser empacotada usando:

```shell script
./mvnw package
```

Produz o arquivo `quarkus-run.jar` na pasta `target/quarkus-app/`.
Este não é um _über-jar_, pois as dependências são copiadas para a pasta `target/quarkus-app/lib/`.

A aplicação pode ser executada usando: `java -jar target/quarkus-app/quarkus-run.jar`.

Se você quer compilar um _über-jar_, execute o comando:

```shell script
./mvnw package -Dquarkus.package.jar.type=uber-jar
```

A aplicação empacotada estará disponível em `target/*-runner.jar`.
A aplicação pode ser executada usando: `java -jar target/*-runner.jar`.

## Criando um executável nativo

Você pode criar uma execução nativa usando:

```shell script
./mvnw package -Dnative
```

Ou, se você não tiver o GraalVM instalado, você pode rodar o executável nativo no container usando:

```shell script
./mvnw package -Dnative -Dquarkus.native.container-build=true
```

Você pode então executar seu executável nativo com: `./target/iaconn-1.0.0-SNAPSHOT-runner`

Se você quiser aprender mais sobre a construção de executáveis nativos, por favor consulte <https://quarkus.io/guides/maven-tooling>.

## Guias Relacionados

- REST ([guia](https://quarkus.io/guides/rest)): Uma implementação Jakarta REST que utiliza processamento em tempo de build e Vert.x. Esta extensão não é compatível com a extensão quarkus-resteasy, nem com quaisquer extensões que dependam dela.

## Código Fornecido

### REST

Inicie facilmente seus Serviços Web REST

[Related guide section...](https://quarkus.io/guides/getting-started-reactive#reactive-jax-rs-resources)
