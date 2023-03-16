<h1 align="center">Discovery Server</h1>

<p>O Discovery Server é uma parte essencial da arquitetura de microservices, pois é usado para gerenciar os diferentes serviços. Ele atua como um intermediário entre os serviços, indicando as instâncias disponíveis e suas respectivas localizações. Quando uma nova instância de serviço é iniciada, ela é registrada automaticamente no Discovery Server, que a adiciona à lista de serviços disponíveis. Da mesma forma, quando uma instância é encerrada, o servidor a remove automaticamente da lista. Isso garante que todos os serviços sejam mantidos atualizados e que as solicitações sejam encaminhadas para as instâncias corretas. Em resumo, o Discovery Server é responsável por manter um registro atualizado dos serviços disponíveis e seus locais, garantindo a comunicação adequada entre eles.<p>

## Instalação

1. Clone o projeto
```bash
git clone https://github.com/JG-OLIVEIRA/discovery-server
```
2. Vá até à pasta raiz do projeto
```bash
cd discovery-server
```
3. Use `mvn package` para gerar a pasta `target` contendo o execultável da aplicação
```bash
mvn package
```
4. Agora rode a aplicação que vai estar disponível no url http://localhost:8761/eureka

```java
package com.programming.techie.discoveryserver;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.netflix.eureka.server.EnableEurekaServer;

@SpringBootApplication
@EnableEurekaServer
public class DiscoveryServerApplication {
    public static void main(String[] args) {
        SpringApplication.run(DiscoveryServerApplication.class, args);
    }

}
```
## Tela da aplicação

<img src="https://live.staticflickr.com/65535/52751204101_7e1f12e2eb_b.jpg">
