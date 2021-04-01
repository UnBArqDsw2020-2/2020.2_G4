| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 01/04/2021 | 1.0 | Criação do documento | Lucas Lopes |
| 01/04/2021 | 2.0 | Adição dos conceitos e exemplos aplicados ao projeto | Lucas Lopes |

## Introdução

<p align="justify"> O padrão   de serviço é um padrão relativamente antigo que era muito popular com o Java EE. Martin Fowler o descreveu em 2004 em seu blog . O objetivo deste padrão é melhorar a modularidade da aplicação removendo a dependência entre o cliente e a implementação de uma camada de serviços . Com as camadas de serviços, podemos  desacoplar componentes de software e melhorar a capacidade de manutenção do código.</p>


<p align="center"> O fluxo de service funciona da seguite forma </p>

<ld>
    <li> 1 - Os controladores recebem solicitações de clientes de entrada e aproveitam os serviços.</li>
    <li> 2 - Os serviços contêm toda a lógica de negócios e também podem fazer chamadas para a  camada de acesso a dados. </li>
    <li> 3 - A camada de acesso a dados interage com o banco de dados realizando consultas. </li>
    <li> 4 - Os resultados são repassados ​​para a camada de serviço. </li>
    <li> 5 - A camada de serviço pode então devolver tudo ao controlador. </li>
    <li> 6 - O controlador pode então responder ao cliente!. </li>
</ld>

<ld>
<h4>A camada de serviço deve:</h4>
    Conter lógica da regra de negócios
    Aproveitar a camada de acesso a dados para interagir com o banco de dados
<ld>

 

<ld>
<h4> A camada de serviço não deve: </h4>
    Fazer requisições diretas 
    Lidar com a resposta aos clientes
    Fornece qualquer coisa relacionada à camada de transporte HTTP; códigos de status, cabeçalhos, etc.
    Interagir diretamente com o banco de dados
</ld>



## Aplicação no projeto:

<p align="justify"> No projeto  foi abstraido as validações e as regras de négocio do controller de cadastro de usuário. Foi criando um serviço externo para o  controller, causando assim maior legibilidade  e manutenção do código. No exemplo abaixo, temos a abstração das validações e das regras de négocio  </p>


### Abstraindo a validação do controller


![carbon (3)](https://user-images.githubusercontent.com/38164895/113356528-c2b3e600-9318-11eb-9ae3-6916b7d07e6d.png)



### Abstraindo nas regras de négocios do controller



![carbon (4)](https://user-images.githubusercontent.com/38164895/113356806-41108800-9319-11eb-804c-49f9ff141597.png)


### Resultado final

![carbon (6)](https://user-images.githubusercontent.com/38164895/113357801-f55ede00-931a-11eb-9dbf-8792a186b32d.png)



<p align="justify"> O padrão em resumo consiste em abstrair as regras de négocios e validações afim de facilitar a manuteção,legilidade e testabilidade do código. É recomendado usar em 2 principais situações: Código muito extenso ou quando o  código contém muitas validações.</p>

<p align="justify"> Com o controller acima, podemos concluir que ficou mais limpo e organizado. Pois, toda a validação e as regras de négocios foram separados em uma camada de serviços. Antes, o controller tinha toda as validações de campos, de buscar no banco de dados se já existia um usuário com o mesmo email por exemplo. Portanto, ao aplicarmos o service pattern, o controller apenas recebe os dados do cliente e manda para a camada de serviços. A camada de serviços faz todas as verifições e validações e devolve ao controller o usuário criado. O controller, por fim devolve ao cliente as informações do usuário criado. </p>



## Referências


Node Service-oriented Architecture. Disponível em:https://www.codementor.io/@evanbechtol/node-service-oriented-architecture-12vjt9zs9i. Último acesso em: 01/04/2021.

Service Layer. Disponível em: https://java-design-patterns.com/patterns/service-layer/. Último acesso em: 01/04/2021.

