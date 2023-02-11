# CONCEITO DE COMUNICAÇÃO DE API E ROTAS

## COMUNICAÇÃO:
- Menssageria (MQ): fila
- Socket: tempo real
- Http: não tão real

## API:

O acrônimo API que provém do inglês Application Programming Interface (Em português, significa Interface de Programação de Aplicações), trata-se de um conjunto de rotinas e padrões estabelecidos e documentados por uma aplicação A, para que outras aplicações consigam utilizar as funcionalidades desta aplicação A, sem precisar conhecer detalhes da implementação do software.

Desta forma, entendemos que as APIs permitem uma interoperabilidade entre aplicações. Em outras palavras, a comunicação entre aplicações e entre os usuários.

- nem toda api é web
- Passar get que não aceita campo, apenas parametro na rota.
- Pesquisar URL pattern
 
### API REST:

REST significa Representational State Transfer. Em português, Transferência de Estado Representacional. Trata-se de uma abstração da arquitetura da Web. Resumidamente, o REST consiste em princípios/regras/constraints que, quando seguidas, permitem a criação de um projeto com interfaces bem definidas. Desta forma, permitindo, por exemplo, que aplicações se comuniquem.

- trabalha exclusivamente com http
- via rota

> C reate - POST
>
> R ead   - GET
>
> U pdate - PUT
>
> D elete - DELETE

Em geral utiliza-se o GET para recuperar, o POST para criar, o PUT para alterar e o DELETE para apagar.

[Pegar paper REST](https://ieeexplore.ieee.org/document/8385157)

### RESTFUL(SOAP):

Existe uma certa confusão quanto aos termos REST e RESTful. Entretanto, ambos representam os mesmo princípios. A diferença é apenas gramatical. Em outras palavras, sistemas que utilizam os princípios REST são chamados de RESTful.

- REST: conjunto de princípios de arquitetura
- RESTful: capacidade de determinado sistema aplicar os princípios de REST.

- Capacidaade de implementar o REST (RESTFul) é o conceito REST implementado de forma correta.

***

## Links de ajuda

- [Testando serviços Web API com Postman](https://medium.com/@thi_carva/testando-servi%C3%A7os-web-api-com-postman-874ac81b20a3) - Lista de Status Return Code

- [O que é API? REST e RESTful? Conheça as definições e diferenças!](https://becode.com.br/o-que-e-api-rest-e-restful/) -  API, REST e “RESTful”

***
