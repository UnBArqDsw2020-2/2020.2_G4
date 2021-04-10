| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 29/03/2021 | 1.0 | Criação do documento | Victor Levi |
| 09/04/2021 | 2.0 | Explicação dos conceitos e da aplicação no projeto | Lucas Lopes |

## Introdução

O façade é um padrão de projeto estrutural que fornece uma interface unificada para um conjunto de interfaces em um subsistema. É recomendado usar o padrão façade quando:
    - Deseja fornecer uma interface mais simples para um sistema mais complexo
    - Criar pontos de entrada para determinadas partes do sistema.

Ao utilizarmos o façade obtemos:
    - Isolar o código do cliente do código complexo
    - Facilitar o uso do sistema
    - Criar pontos de entrada para camadas da aplicação e serviços de terceiros

## Aplicação no projeto

Facade pode ser visto em uma classe que possui uma interface simples e essa classe delega a maior parte do trabalho para outras classes. Em nossa aplicação, criamos uma fachada para as rotas onde em uma classe reunimos todas as rotas da aplicação. No app.js, reunirá todas essas rotas.


[Código](https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-backend/blob/master/src/routes.js)

![carbon(2)](https://user-images.githubusercontent.com/38164895/114247619-e9eb6280-996b-11eb-99bd-b1f773ec7b89.png)


[Código](https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-backend/blob/master/src/app.js)

![carbon(3)](https://user-images.githubusercontent.com/38164895/114247713-2d45d100-996c-11eb-9f42-c4697e0ef057.png)



## Referências

Facade Disponível em: https://refactoring.guru/design-patterns/facade. Acesso em: 09 de Abril 2021.

Façade Teoria e Prática - Padrões de Projeto - Parte 22/45. Disponível em: https://www.youtube.com/watch?v=A7mNiaBACYs&list=PLbIBj8vQhvm0VY5YrMrafWaQY2EnJ3j8H&index=22. Acesso em: 09 de Abril de 2021
