# Versionamento Semântico 2.0

Independente da linguagem utilizada na APLICAÇÃO, e além de ter seu código versionado por sistema como o git,
possuímos mais um nível de controle de versão: o versionamento semântico.
Que ajuda o usuário final a entender novas features implementadas,
bugs resolvidos e garantir compatibilidade de código sem ter quer ler o código do último pull request.

É dividido em:

| MAJOR                                        | MINOR                                                                 | PATCH                                                                      | PRE-RELEASE                                                                              |
| -------------------------------------------- | --------------------------------------------------------------------- | -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| [+Evolução de API]                           | [+Nova funcionalidade]                                                | [+Coreção de BUG]                                                          | [+Aviso de Incompatibilidade]                                                            |
| Alterações incompatíveis com a versão da API | Funcionalidades implementadas compatíveis com a versão anterior MAJOR | Resolução de bugs compatível com as versões anteriores MINOR ativa e MAJOR | Sinalização de não cumprimento do padrão de compatibilidade (ex: prefixos -alpha, -beta) |

NOTA: Rótulos adicionais para pré-lançamento e compilação de metadados estão disponíveis como 
extensões para o formato MAJOR.MINOR.PATCH. Saiba mais em: [Versão semântica 2.0.0](https://semver.org/)

***
