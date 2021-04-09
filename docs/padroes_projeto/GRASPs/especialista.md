| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 29/03/2021 | 1.0 | Criação do documento | Victor Levi |
| 09/04/2021 | 2.0 | Explicação dos conceitos e aplicação no projeto | Lucas Lopes |
## Introdução

Especialista é um padrão que visa  atribuir responsabilidades para a entidade mais especialista em um determinado contexto em todos os aspectos do sistema.

    - Quem é o melhor para fazer criptografia?
    - Quem é o melhor para fazer login?

<ld>
<h3>Vantegens ao utilizar o Especialista:</h3>
    Mantém o encapsulamento que favorece o acomplamento fraco
    Comportamento fica distribuido entre as classes que têm a informação necessária o que favorece a alta coesão

<ld>

### Alta coesão


Consisti em atribuir responsabilidades das classes, mantendo os objetos focados, gerenciáveis e compreensíveis. Ao ter alta coesão consequentemente obtemos:

    - Melhoram a  claridade e facilidade de entendimento do projeto
    - Causa impacto positivo na manutenção
    - Com  a granularidade baixa e funcionalidade bem focada, aumenta o reuso

### Acoplamento fraco

Consiste em determinar que as classes  devem depender de objetos de abstrações. O baixo acoplamento é um padrão de avaliação que determina como atribuir responsabilidades de suporte. Com isso, consequentemente obtemos:
    - Uma classe fracamente acoplada não é afetada.
    - Simples de entender isoladamente
    - Reuso mais fácil

## Aplicação no projeto

Foi usado o padrão Especialista nos métodos de cadastro de usuário usuário. Onde a classe criptografia é especialista em criptografar a senha do usuário em 16 hash.

[Código](https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-backend/blob/master/src/app/services/crypto.js)

[Código](https://github.com/UnBArqDsw2020-2/2020.2_G4-Meubrecho-backend/blob/master/src/app/services/CadastrarUsuarioService.js)

![carbon(1)](https://user-images.githubusercontent.com/38164895/114240476-f36dce00-995d-11eb-86df-76eec5b3ff91.png)

##

## Referências

GRASP: PADRÕES PARA ATRIBUIÇÃO DE RESPONSABILIDADES Disponível em: https://edisciplinas.usp.br/pluginfile.php/2186358/mod_resource/content/1/Aula09_GRASP.pdf. Último acesso em 09/04/2021  
