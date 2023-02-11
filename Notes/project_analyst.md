# PARA ESCREVER OS CARDS

Cada frase começa com um ator que inicia uma atividade: quem (ator) faz o quê (atividade) com o que (objetos de trabalho) com quem (outros atores). A sintaxe básica é: sujeito - predicado - objeto . 5 Sintaxe mais complexa também é permitida. 

***

Theme (Tema): são assuntos nos quais os Epics (épicos) se agrupam, e geralmente são definidos conforme o contexto de negócio em que o épico está. Por exemplo: numa empresa há uma iniciativa de "Diminuir a inadimplência para vendas a prazo". Isso pode ser o tema, e todos os épicos agrupados neste tema são orientados para realizar a visão do tema.

O objetivo de um Épico é realizar um tema de negócio. Podem haver 1 ou mais épicos agrupados sob um tema.

Exemplo: para o tema "Diminuir a inadimplência para vendas a prazo" temos um épico chamado "Implementação de políticas de trava de parcelamento para clientes com nota abaixo de 8".

***

## DICAS

- Não faça: modele os detalhes técnicos de como um usuário interage com um sistema
- Existem vários motivos pelos quais não gostamos tanto desse estilo:
- Não conta uma história convincente. Ele tem pouco potencial para gerar conversas e percepções interessantes sobre o domínio.
- Se o objetivo do modelo é documentar a implementação do sistema, então há melhores maneiras de conseguir isso, por exemplo, um diagrama de sequência UML (Unified Modeling Language).
- Se o objetivo do modelo é projetar a interface do usuário, então existem meios melhores para fazer isso (por exemplo, maquetes e protótipos).
- Como o modelo é específico para a implementação técnica do sistema de software, ele ficará desatualizado se houver alterações na implementação.

***

## DAILY

Há três perguntas que devem ser respondidas na Reunião Diária:

- O que eu fiz ontem que ajudou o time de Desenvolvimento a alcançar a meta da Sprint?
- O que eu farei hoje para ajudar o time de Desenvolvimento a alcançar a meta da Sprint?
- Existe algum obstáculo que impeça o Time de Desenvolvimento de alcançar a meta da Sprint?

***

## GUARDADO

### ARQUIVO FEATURE TRACKER

```
Feature Tracker


- GetDevicesAvailable - retorno somente os devices disponíveis

*obs:* Adicionar uma marcação nos devices da sessão que permita realizar esse filtro

**obs²: Uma ideia para marcação seria usedBy: userId, dessa forma poderiamos realizar um lookup com os usuários


- log
- Controle de timeout
- Sistema de notificação


Ao selecionar um device: dispara o timeout de idle do device

Ao iniciar uma gravação: dispara o timeout da gravação

As notificações são disparadas para informar o tempo que o usuário tem para manter o device em idle e o tempo para gravação
```

***

### Como estimar esforço?

*[1]

Para estimar com qualidade leve emconsideração 3 fatores:
- [x] Complexidade
- [x] Sua Habilidade
- [x] Os Riscos

**Complexidade:**
Considere os Skills técnicos, por exemplo, o conhecimento sobre uma determinada linguagem, ou sobre infra.

**Sua Habilidade:**
Considere quantas vezes você já fez isso? O treino eleva sua habilidade sobre um determinado Skill técnico.

**Os Riscos:**
O que pode atrapalhar o seu desenvolvimento?
- Dependências
- Impedimentos
- Falta de 1 dos itens acima
- Se é chato

|       TABELA DE ESFORÇO      |         NÍVEL        |
| ----------------------------------------- | --------------------- |
|                  (+)SKILLS                 |  (-)COMPLEXO |
|                  (-)SKILLS                  | (+)COMPLEXO |
| (+)HABILIDADE (X) FAZENDO |  (-)COMPLEXO |
|              (-)HABILIDADE             | (+)COMPLEXO |
|                  (+)RISCO                  | (+)COMPLEXO |
|                   (-)RISCO                  |  (-)COMPLEXO |

&nbsp;

### Velocidade da Sprint (Lead Time)

*[4] [5]

Velocidade em termos  Ágeis (Velocity), significa a quantidade média de trabalh que uma equipe pode completar em um "Ciclo de Entrega", normalmnete uma Sprint.

O uso do gráfico de Lead Time para responder algumas perguntas como?
- Quanto tempo a equipe precisa pra desenvolver um novo item?
- A equipe está conseguindo desenvolver as funcionalidades planejadas dentro do Timebox de uma iteração?
- Existe algo afetando a previsibilidade dos itens que são trabalhados pela equipe(por exemplo, tamanho, complexidade, incerteza)? A variabilidade vem aumentando nas últimas semanas?
- Entender as dispersções do Lead Time

&nbsp;

### Throughput Scrum por Sprint

*[2] [3]

De forma bem simples, o throughput ou vazão média é a qualidade de entregas que seu time consegue realizar ao final de uma Sprint ou um período de tempo.

Ao decorrer de cada Sprint seu throughput fica mais acertivo, e podem nos ajudar a responder questões que podem aparecer no início de um projeto. Por exemplo:

- Em um projeto com 16 demandas, quanto tempo eu levo para finalizá-lo?
- Quantas demandas meu time entrega por Sprint?
- Como anda o ritmo de entregas do meu time? Conseguimos melhorar a quantidade de entregas sem influenciar na qualisade do trabalho?

Ou
- Quantos itens de trabalho a equipe entrega por semana?
- O time está criando uma tendência crescente de entrega?
- Algum fator tem bloqueado a capacidade de entrega da equipe?

Geralmente, o Throughput de uma equipe cai pelos seguintes motivos:
- **Requisitos Ruins** - exemplo, baixa qualidade nos critérios de aceite de histórias de usuário
- **Dívidas Técnicas** - exemplo, necessidade de refatoração inesperadas 
- **Gargalos do Processo** - exemplos, especialista de testes sobrecarregado, pipeline de implantação falho
- **Backlog com Baixo nível de itens prontos para desenvolvimento** 
- **Mudança de Escopo** - por exemplo, aumento no escopo de uma história de usuário

&nbsp;

### Priorização de Backlog

*[6]

Vale a leitura e releitura sempre do artigo completo

&nbsp;

### Burnup x Burndown

&nbsp;

### Desafio do Projeto

&nbsp;

### Referências Bibliográficas

[1] [COMO MONTAR UM MODELO DE REFERÊNCIA PARA ESTIMATIVAS USANDO STORY POINTS](https://www.linkedin.com/pulse/como-montar-um-modelo-de-refer%C3%AAncia-para-estimativas-usando-ivonika/)

[2] [THROUGHPUT: ENTENDA A IMPORTÂNCIA DESSA MÉTRICA](https://blog.acelerato.com/artigo/throughput-entenda-o-que-e/)

[3] [Métricas ágeis: Throughput e gráfico de Burnup](https://imasters.com.br/agile/metricas-ageis-throughput-e-grafico-de-burnup)

[4] [O que é Velocity no Agile?](https://www.digite.com/pt-br/agile/o-que-e-velocity/#:~:text=Sprint%2FRelease%20ou%20Velocidade%20Semanal,sprints%20ou%20semanas%20ser%C3%A3o%20necess%C3%A1rios.)

[5] [Principais Métricas que você pode usar para melhorar o seu time](https://pt.linkedin.com/pulse/principais-m%C3%A9tricas-que-voc%C3%AA-pode-usar-para-melhorar-o-analu-brondino)

[6] [5 técnicas de priorização: Organize seu backlog](https://medium.com/empiricustech/5-t%C3%A9cnicas-de-prioriza%C3%A7%C3%A3o-organize-seu-backlog-e636d97222e4)

***
