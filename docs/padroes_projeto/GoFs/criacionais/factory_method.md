| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 29/03/2021 | 1.0 | Criação do documento | Victor Levi |

## Introdução
O Factory é um padrão criacional de projeto que fornece uma interface para criar objetos em uma superclasse, mas permite que as subclasses alterem o tipo de objetos que serão criados.

  O padrão Factory sugere que seja substituido chamadas diretas de construção de objetos por chamadas para um método especial. A mudança de chamada do construtor passa de uma parte do programa para outra, agora pode sobrescrever o método em uma subclasse e alterar as classes que estão sendo criados pelo método.

![estruturaGofCriacional](https://user-images.githubusercontent.com/54318472/114221950-58b4c580-9944-11eb-972c-abfa10a62b1f.png)

## Aplicação No Projeto 
    A responsabilidade da criação de instâncias dos produtos esta no metodo "productCreate", da classe "ProductService", e não na controller "ProductController", retirando a responsabilidade de criação de produto
![Criacional-ProductController](https://user-images.githubusercontent.com/54318472/114223187-e2b15e00-9945-11eb-8bed-bdf00e979960.png)

![Criacional-ProductService](https://user-images.githubusercontent.com/54318472/114223243-f361d400-9945-11eb-8d1d-a5a18f1c5836.png)

## Referências
-REFACTORING.GURU. Strategy. Disponível em: https://refactoring.guru/pt-br/design-patterns/factory-method . Acesso em: 26 de outubro. 2020.


