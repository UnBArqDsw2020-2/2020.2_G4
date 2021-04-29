
# Versionamento

| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 27/04/2021 | 1.0 | Criado a estrutura do documento | Lucas Lopes |
| 29/04/2021 | 2.0 | Adição do topico 2.0 | Lucas Lopes |
| 29/04/2021 | 4.0 | Adição do tópico 4.0 | Lucas Lopes |
| 29/04/2021 | 5.0 | Adição do tópico 5.0, 6.1 e 10.0 | Lucas Lopes | 



# 1 - Introdução



## 1.1 - Finalidade

## 1.2 - Escopo

# 2.0 - Representação  Arquitetural
## 2.1 - Tecnologias
### Frontend

<p align="justify"> <b>React JS</b> é uma biblioteca JavaScript para a criação de interfaces de usuário. Foi Criado em 2011 Facebook.O React é uma biblioteca front-end e tem como um de seus objetivos facilitar a conexão entre diferentes partes de uma página, portanto seu funcionamento acontece através do que é chamado de componentes. Foi escolhida essa tecnologia pois existem diversos conteúdos de fácil acesso. Por isso é, uma escolha segura e de fácil aprendizagem pela equipe. </p>


### Backend

<p align="justify"> <b>O Node.js </b> se caracteriza como um ambiente de execução JavaScript. Com ele, o usuário pode criar aplicações sem depender do browser para isso. Com alta capacidade de escalabilidade, boa flexibilidade, arquitetura e baixo custo. Por ser baseada no javascript o que confere uma integração positiva quando usamos juntamente com o  React, que também é feito com Javascript. </p>

<p align="justify"> <b> Express.js </b>é um Framework rápido e um dos mais utilizados em conjunto com o Node.js, facilitando no desenvolvimento de aplicações back-end e até, em conjunto com sistemas de templates, aplicações full-stack. </p>


### Banco de dados

<p align="justify"> <b>O MongoDB</b> é um banco de dados opensource, de alta performance e flexível, sendo considerado o principal banco de dados NoSQL. O MongoDB é orientado a documentos, ou seja, os dados são armazenados como documentos, ao contrário de bancos de dados de modelo relacional, onde trabalhamos com registros em linhas e colunas. Os documentos podem ser descritos como dados no formato de chave-valor, no caso, utilizando o formato JSON (JavaScript Object Notation). O Mongo foi utilizado pois permite executar consultas executando código JavaScript o que é útil ao utilizarmos com o backend em nodejs e frontend em React. Além disso, é de fácil integração e rápido aprendizado. </p>

# 3.0 - Metas e Restrição da Arquitetura
## 3.1 - Metas
## 3.2 - Restrições


# 4.0 - Padrão Arquitetural

<p align="justify"> Padrões arquiteturais expressam formas de organizar a estrutura fundamental do sistema, permitem a construção de uma arquitetura aderente a certas propriedades. Além disso,  fornecem um conjunto de subsistemas pré definidos, especificando suas responsabilidades e incluindo regras e diretrizes para organizar as relações entre eles. O padrão MVC foi escolhido para o projeto. </p>

## MVC

<p align="justify"> O MVC é um padrão de arquitetura de software. O MVC sugere uma maneira para você pensar na divisão de responsabilidades, principalmente dentro de um software web. </p>

<p align="justify"> O princípio básico do MVC é a divisão da aplicação em três camadas: a camada de interação do usuário (view), a camada de manipulação dos dados (model) e a camada de controle (controller). </p>

<p align="justify"> Com o MVC, é possível separar o código relativo à interface do usuário das regras de negócio. Além disso, deixa o código mais manutenível, ou seja, mais fácil de fazer manutenção, já que temos as responsabilidades devidamente separadas. Isso também traz uma facilidade na compreensão do código, além da sua reutilização. Além disso, tem-se um código mais testável, pois ele é mais granular. </p>

### Model

<p align="justify"> É a camada que contem a estrutura de dado atrás de uma parte específica da aplicação,usualmente portada em JSON. Ela é: </p>

- Responsável pela leitura manipulação e validação de dados, e também de suas validações.
- Responsável por tratar as regras de negócio.  
- Obtém os dados e os traduz em informações relevantes para serem exibidas pela View.
- Notifica a view e controler associados quando há uma mudança em seu estado. 

<p align="center"> Exemplo de model aplicado no backend </p> 

![carbon (8)](https://user-images.githubusercontent.com/38164895/116594835-09393800-a8f9-11eb-9a17-d26ad651bc4f.png)

<p align="center"> <a href="https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-backend/blob/master/src/app/models/User.js"> Link</a> </p>


### View

View pode ser qualquer saída de representação dos dados, como uma tabela ou um diagrama.

- É a camada que exibe uma representação dos dados.
- É camada de interface com usuário (view).
- Também conhecida como cliente-side.
- Faz a exibição dos dados, utilizando-se de #HTML e/ou XML.
- É responsável por usar as informações modeladas para produzir interfaces de apresentação conforme a necessidade.

<p align="center"> Exemplo de View (frontend) </p> 

![carbon (9)](https://user-images.githubusercontent.com/38164895/116596592-ef98f000-a8fa-11eb-8b90-4b06a55ddbe3.png)


<p align="center"> <a href="https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-frontend/blob/master/frontend/src/pages/Registro/index.js"> Link</a> </p>



### Controller

- É a camada de controle.
- Exerce o controle de qual model deverá ser aplicado e qual view será mostrado ao usuário.
- Podemos dizer que esta camada faz uma gerência das outras duas camadas.
- O controller manipula e roteia as requisições dos usuários.
- Interpreta as requisições submetidas pelo usuário e traduz em comandos que são enviados para o (Model) e/ou para a View) .
- Valida as requisições dos usuários de acordo com as regras de autenticação e autorização.


<p align="center"> Exemplo de controller aplicado ao projeto </p> 


![carbon (10)](https://user-images.githubusercontent.com/38164895/116599231-33412900-a8fe-11eb-98f5-c9d677fb3cf2.png)


<p align="center"> <a href="https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-backend/blob/master/src/app/controllers/UserController.js"> Link</a> </p>



# 5.0 - Visão de Caso de uso
<p align="justify"> Esse diagrama documenta o que o sistema faz do ponto de vista do usuário. Em outras palavras, ele descreve as principais funcionalidades do sistema e a interação dessas funcionalidades com os usuários do mesmo sistema </p>

<p align="center"> Diagrama de casos de uso geral </p>

![Untitled Diagram(1)](https://user-images.githubusercontent.com/38164895/116618661-b9b53500-a915-11eb-8484-bc21157ad6f0.png)

<p align="center"> <a href="https://unbarqdsw2020-2.github.io/2020.2_G4/modelagem/dinamicos/diagramacasoUso/">Link</a> </p>

# 6.0 - Visão Lógica

<p align="justify"> A visão lógica mostra um subconjunto do modelo de design significativo em termos de arquitetura, ou seja, um subconjunto das classes, subsistemas, pacotes e realizações de caso de uso. </p>


## 6.1 - Diagrama de contexto

<p align="justify"> O diagrama de contexto é um gráfico, composto por um fluxo de dados que mostra as interfaces entre o projeto e a sua relação com o ambiente em que vai ser desenvolvido. </p>

![Untitled Diagram-Page-2(1)](https://user-images.githubusercontent.com/38164895/116625499-1ddcf680-a920-11eb-9f46-ef9e82b866d7.png)



## 6.2 - Diagrama de pacotes

# 7.0 - Visão de processos

# 8.0 - Visão de implantação

# 9.0 - Visão de implementação

# 10.0 - Visão de dados

Aqui, há uma descrição do modelo de persistência de dados persistidos no MongoDB.

## Modelo Usuário

* _id
    - Tipo: Number
    - Obrigatoriedade: Sim

- Nome
    - Tipo: String
    - Obrigatoriedade: Sim

- Email
    - Tipo: String
    - Obrigatoriedade: Sim
    - Único: Sim

- Senha
    - Tipo: String
    - Obrigatoriedade: Sim

- Whatsapp
    - Tipo: Number
    - Obrigatoriedade: Sim
    
- CPF
    - Tipo: Number
    - Obrigatoriedade: Sim


### Exemplo

![carbon (11)](https://user-images.githubusercontent.com/38164895/116627357-5d591200-a923-11eb-98c1-fa91ccfb765a.png)


## Modelo Produto

* _id
    - Tipo: Number
    - Obrigatoriedade: Sim

- Nome
    - Tipo: String
    - Obrigatoriedade: Sim

- imagem
    - Tipo: String
    - Obrigatoriedade: Sim

- Descricao
    - Tipo: String
    - Obrigatoriedade: Sim

- Preco
    - Tipo: Number
    - Obrigatoriedade: Sim

- User_id
    - Tipo: Usuário (ref user)
    - Obrigatoriedade: Sim

- User_favorite
    - Tipo: ArrayList Usuário (ref user)
    - Obrigatoriedade: Não

- Tag
    - Tipo ArrayList Tag (ref tag)
    - Obrigatoriedade: Não

### Exemplo

![carbon (12)](https://user-images.githubusercontent.com/38164895/116628997-af4f6700-a926-11eb-9e85-24a126674656.png)


## Modelo TAG

* _id
    - Tipo: Number
    - Obrigatoriedade: Sim


- Tag
    - Tipo ArrayList String
    - Obrigatoriedade: Sim

### Exemplo

![carbon (13)](https://user-images.githubusercontent.com/38164895/116629555-dbb7b300-a927-11eb-927f-c1d424f8784e.png)


## Referências

React: o que é, como funciona e porque usar e como aprender.  Disponível em: https://kenzie.com.br/blog/react/.  Último acesso em 29/04/2021.


O que é o express js. Disponível em: https://www.treinaweb.com.br/blog/o-que-e-o-express-js/. Último acesso em: 29/04/2021.

O que é MVC. Disponível em: https://www.treinaweb.com.br/blog/o-que-e-mvc/. Ùltimo acesso em: 29/04/2021.

Padrão MVC | Arquitetura Model-View-Controller. Disponível em: https://www.portalgsti.com.br/2017/08/padrao-mvc-arquitetura-model-view-controller.html. Último acesso em: 29/04/2021.

Conceito: Visão Lógica. Disponível em: https://www.cin.ufpe.br/~gta/rup-vc/core.base_rup/guidances/concepts/logical_view_C135365E.html. Último acesso em: 29/04/2021.

Quais os benefícios de criar um diagrama de contexto?. Disponível em: https://robsoncamargo.com.br/blog/Quais-os-beneficios-de-criar-um-diagrama-de-contexto. Último acesso em: 29/04/2021.