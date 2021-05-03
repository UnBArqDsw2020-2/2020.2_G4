# Versionamento

| Data       | Versão | Descrição                        | Autor          |
| ---------- | ------ | -------------------------------- | -------------- |
| 27/04/2021 | 1.0    | Criado a estrutura do documento  | Lucas Lopes    |
| 29/04/2021 | 2.0    | Adicionado introdução e docker   | Lucas Lopes    |
| 03/04/2021 | 3.0    | Adicionado reutilização back-end | Matheus Filipe |

# Introdução

Reutilização de software trata do uso de software ou conhecimentos de software já existentes para construir novos softwares. Componentes reutilizáveis podem ser tanto software reutilizável quanto conhecimento de software.

A ideia do reuso é evitar retrabalho no desenvolvimento de um novo projeto, sempre levando em consideração trabalhos anteriores, fazendo com que soluções previamente desenvolvidas sejam aproveitadas e implementadas em novos contextos.

# Docker

Uma das formas de reutilização no projeto foi por meio da utilização do Docker. O que ocorre na prática é que o docker destaca recursos e usa bibliotecas de kernel em comum. Os itens empacotados — ou até mesmo um ambiente inteiro — são dispostos no container e se tornam portáveis, o que torna o trabalho conjunto mais eficiente. Ao mesmo tempo, a implantação pode ser feita em ambientes não heterogêneos. Ele possui muitos hot spots, e alguns frozen spots, ambos estão sendo utilizados em nossa aplicação. Além disso, foi utilizado o Docker Compose para orquestrar os containers do Docker.

- Frozen Spots:

  - Formatação do arquivo
  - Nome dos arquivos.

Hot Spots:

    - Imagem para construir o container;
    - Dependências;
    - Comandos no dockerfile
    - Network no docker compose
    - Variáveis de ambiente no dockerfile

## Docker Frontend

Para o Frontend, foi configurado um Docker utilizando as tecnologias do Nodejs alpine(uma versão leve do Nodejs) como base. Além disso, Ele também fica responsável em padronizar as versões das bibliotecas utilizadas, impedindo que haja conflitos de desenvolvimento entre a equipe.

<p align="center"> Dockerfile </p>

![carbon(6)](https://user-images.githubusercontent.com/38164895/116637116-6fde4600-a939-11eb-885c-fcd02941ea34.png)

<p align="center"> <a href="https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-frontend/blob/master/frontend/Dockerfile"> Link </a> </p>

<p align="center"> DockerCompose </p>

![carbon(7)](https://user-images.githubusercontent.com/38164895/116637217-ab791000-a939-11eb-9ef4-2afcf709c184.png)

<p align="center"> <a href="https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-frontend/blob/master/frontend/docker-compose.yml"> Link </a> </p>

## Docker Backend

Para o Backend, foi configurado um Docker utilizando as tecnologias do NodeJs alpine (uma versão mais leve do NodeJs) como base. Além disso, Ele também fica responsável em padronizar as versões das bibliotecas utilizadas, impedindo que haja conflitos de desenvolvimento entre a equipe. No Docker do backend ele disponibiliza uma porta de saída que é possivel se conectar e trocar dados com o frontend.

### Exemplo docker e docker compose

<p align="center">DockerFile</p>

![carbon(4)](https://user-images.githubusercontent.com/38164895/116635410-15db8180-a935-11eb-89f9-157f15230a23.png)

<p align="center"> <a href="https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-backend/blob/master/Dockerfile"> Link </a> </p>

<p align="justify"> DockerCompose </p>

![carbon(5)](https://user-images.githubusercontent.com/38164895/116635494-5509d280-a935-11eb-95de-c1f008088dd7.png)

<p align="center"> <a href="https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-backend/blob/master/docker-compose.yaml"> Link </a> </p>

# Frontend

# Backend

## Mongoose

O <b>Mongoose</b> é uma ferramenta bastante útil para poupar tempo com validações, casting de tipos e lógica de negócios na escrita e organização do banco de dados, optamos por utilizá-lo devido ao curto prazo para o desenvolvimento do projeto e por se apresentar como uma boa escolha para a arquitetura escolhida de um banco de dados não relacional. Também é importante citar que a manipulação de queries em SQL seria pouco produtivo para o cumprimento do escopo do projeto.

Exemplo de criação de uma tabela no <b>Mongoose</b>:

![produc-model-example](https://i.imgur.com/8LaMVJa.png)

Com poucas linhas de código é possível realizar uma consulta no banco de dados e uma validação.

Exemplo de uma query de busca:

![find-query](https://i.imgur.com/IGuuJlH.png)

# Referências

Software Reuse Research: Status and Future. Disponível em: https://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=F81286E552CB9153A6C3AF0C943DCB08?doi=10.1.1.75.635&rep=rep1&type=pdf. Acesso em: 29/04/2021

Reutilização de Software - Revista Engenharia de Software. Disponível em: https://www.devmedia.com.br/reutilizacao-de-software-revista-engenharia-de-software-magazine-39/21956. Acesso em: 29/04/2021
