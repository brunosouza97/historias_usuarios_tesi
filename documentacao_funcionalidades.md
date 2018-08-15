# Documentação de Funcionalidades

#### Quem?
* Estamos desenvolvendo este aplicativos para aqueles que são adeptos a Cultura Pop.

#### O que?
* Este é um aplicativo que tem por função tocar música em 8 bits.

#### Por que?
* 

# Funcionalidades
### Enviar comandos para o Arduino:
    SENDO o botão de play apertado
    POSSO enviar comandos para o Arduino
    PARA reproduzir o som
 
 #### Cenário 1: atuar com sucesso (reproduziu o som)
    Dado que a activity do media player está aberta
    E o estado do som consta como pausado
    Quando atuo reproduzindo o som
    Então o sistema transmite comandos ao Arduino
    E o equipamento recebe as informações dos comandos
    E reproduz o som
    
 #### Cenário 2: falha na atuação (não reproduziu o som)
    Dado que a activity do media player está aberta
    E o estado do som consta como pausado
    Quando atuo reproduzindo o som
    Então o sistema transmite comandos ao Arduino
    E o equipamento não recebe as informações dos comandos
    E transmite um erro informando que não pode atuar por já estar reproduzindo o som
    E o sistema atualiza o estado do equipamento
    
### Enviar comandos para o Firebase:
    SENDO o botão de play apertado
    POSSO enviar comandos para o Firebase
    PARA armazenar o histórico

#### Cenário 1: atuar com sucesso (armazenou o histórico)
    Dado que a activity do media player está aberta
    E o estado do som consta como pausado
    Quando atuo reproduzindo o som
    Então o sistema transmite comandos ao Firebase
    E o equipamento recebe as informações dos comandos
    E armazena os dados no database
    
#### Cenário 2: falha na atuação (não armazenou o histórico)
    Dado que a activity do media player está aberta
    E o estado do som consta como pausado
    Quando atuo reproduzindo o som
    Então o sistema transmite comandos ao Firebase
    E o equipamento não recebe as informações dos comandos
    E o sistema atualiza o estado do equipamento
