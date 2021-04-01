## Versionamento

| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 29/03/2021 | 1.0 | Criação do documento | Victor Levi |
| 01/04/2021 | 2.0 | Adição dos conceitos e da aplicação no projeto | Lucas Lopes |



## O que são padrões de projeto

<p align="justify"> Design Patterns ou padrões de projetos são soluções generalistas para problemas recorrentes durante o desenvolvimento de um software. Não se trata de um framework ou um código pronto, mas de uma definição de alto nível de como um problema comum pode ser solucionado. Desigin Patters é um template (modelo) de como resolver um problema que pode ser usado em muitas situações diferentes. </p>

<p align="justify"> Sendo assim, padrões de projetos podem representar um bom ganho de produtividade,organização e manutenção de projetos, pois os padrões se baseam em baixo acoplamento entre classes e as padronizações do código. </p>

## O que é o GRASP?

<p align="justify"> O GRASP consiste em diretrizes para atribuir responsabilidade a classe e objetos em padrões orientados a objetos. Há diversos padrões e príncipios utlizados no GRASP, alguns deles aplicados ao projeto foram: </p>


## Controlador

<p align="justify"> O padrão controlador atribui a responsabilidade de lidar com um evento do sistema. Esse evento pode  representar o cenário global ou cenário de caso de uso. 

Este padrão, funciona como uma camada de indireção para eventos do sistema. Deixando os eventos gerados pela Interface desacoplados dos objetos responsáveis por tratar a requisição, tornando o sistema mais flexível de de fácil manutenção. </p>

## Aplicação no  projeto:

Para o tratamento das regras de négocio, foram utilizados os controllers, que são os responsáveis por receber e tratar dados das requisições. Cada controller trata somente as requisições específicas. No exemplo abaixo, é o controller de  login na aplicação.

![carbon (2)](https://user-images.githubusercontent.com/38164895/113331522-748deb00-92f6-11eb-8234-60923618b72c.png)



<ld>
<h3>Vantegens ao utilizar o Controller:</h3>
    Possibilidades de reutilização das classes
    Possibilidades de interfaces “plugáveis”
    Conhecimento do estado do caso de uso  
    Manter um estado de um caso de uso durante uma sequência de operações.
  
<ld>


## Referências

<p align="justify"> Controller – Padrões GRASP. Disponível em:  https://www.ramonsilva.net/post/controller-padr%C3%B5es-grasp. Último acesso em 01/04/2021 </p>

<p align="justify"> GRASP: Designing Objetos com Responsabilidades - MC 426 IC Unicamp – M. Cecilia C. Baranauskas - https://www.ic.unicamp.br/~ariadne/mc436/1s2017/Lar16GRASP.pdf. Último acesso em 01/04/2021 </p>

<p align="justify"> Desenvolvimento com qualidade com GRASP. Disponível em:  https://www.devmedia.com.br/desenvolvimento-com-qualidade-com-grasp/28704. Último acesso em 01/04/2021 </p>