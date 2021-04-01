
## Histórico de versões

| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 29/03/2021 | 1.0 | Criação do documento | Victor Levi |
| 01/04/2021 | 2.0 | Adição dos conceitos e código | Lucas Lopes |



## Introdução

O Singleton deve garantir que uma classe tenha somente uma instância no programa e deve fornecer um ponto de acesso global. Geralmente é utilizado para recursos que são compartilhados, como acesso ao banco de dados,interfaces gráficas e mais. Uma das principais vantages do singleton é proteger a instância com encapsulamento evitando que outro código sobscreva seu valor,

![image](https://user-images.githubusercontent.com/38164895/112779142-71f07480-901c-11eb-8e56-6c983d2ebc57.png)

<ld>
<h3>Vantegens ao utilizar singleton:</h3>
  - Substitui variáveis globais 
  - Acesso controlado a instância única
  - Só é criado no momento do uso     
  
<ld>

Foi utilizado o padrão Singleton para garantir uma unica instância do banco de dados e será utilizada em toda aplicação ou seja, acesso global. [Github](https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-backend/blob/master/src/database/index.js)

![carbon (1)](https://user-images.githubusercontent.com/38164895/113325799-448f1980-92ef-11eb-9822-98d52859900e.png)


## Referências

Introdução aos padrões criacionais. Disponível em: https://www.devmedia.com.br/introducao-aos-padroes-criacionais-abstract-factory-factory-method-prototype-e-singleton/21249. Último acesso em 01/04/2021.

Singleton Teoria - Padrões de Projeto - Parte 4/45. Disponível em: https://www.youtube.com/watch?v=x9h8MgAvi_I. Último acesso em 01/04/2021.