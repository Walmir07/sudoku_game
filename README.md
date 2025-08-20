# 🔢 Jogo sudoku

Este projeto é um jogo de Sudoku para o terminal desenvolvido em Java. O jogo permite uma experiência de jogo dinâmica e intuitiva, pois além de possuir a grade de números, ele também apresenta as ações que o jogador poderá fazer durante a partida, permitindo o jogador iniciar a partida, colocar ou apagar um número, verificar os números de forma interativa, dentre outras ações que serão apresentadas posteriormente.  O objetivo principal deste projeto é a aplicação prática e o aprofundamento nos quatro pilares da Programação Orientada a Objetos (POO), como abstração, encapsulamento, herança e polimorfismo.

## 🗂 Estrutura do projeto

Para o desenvolvimento deste jogo de Sudoku, o projeto foi organizado de forma modular, com classes e enums que representam as principais entidades e lógicas do jogo. A estrutura foi pensada para manter o código limpo e organizado, facilitando a sua compreensão.

- model: Diretório que contém as classes que representam o "modelo" do jogo, ou seja, as entidades e suas relações, abstraindo a lógica principal.

    - Board: A classe principal que gerencia a grade do Sudoku. Ela armazena as casas (Spaces), verifica o status do jogo e gerencia as ações do jogador.
      
    - GameStatusEnum: Um enum que define os possíveis estados do jogo (NON_STARTED, INCOMPLETE, COMPLETE), ajudando a manter a clareza sobre o andamento da partida.
      
    - Space: Representa uma única célula na grade do Sudoku. Cada Space armazena o número atual, o número esperado e se a célula é fixa (não pode ser alterada pelo jogador).
      
- util: Diretório responsável por armazenar classes utilitárias que não fazem parte da lógica central do jogo, mas são importantes para o seu funcionamento.

    - BoardTemplate: Contém o template visual do tabuleiro do Sudoku, usado para a exibição no terminal. Isso separa a lógica do jogo da interface visual, tornando o código mais legível e fácil de modificar.

- Main: Classe principal responsável por rodar, permitindo:

    - Apresentar o menu de opções ao usuário.
    - Gerenciar a interação do jogador, recebendo entradas.
    - Delegar as ações para a classe Board.
    - Exibir o estado atual do jogo na tela, usando o template da classe BoardTemplate.

## ⚙️ Funcionalidades

- Criar um novo jogo: Inicia uma nova partida de Sudoku, configurando o tabuleiro a partir de um conjunto de posições iniciais.

- Inserir números: Permite ao jogador escolher uma posição (coluna e linha) e um número para ser inserido na grade. O jogo verifica se a posição pode ser alterada.

- Remover números: Oferece a funcionalidade de limpar um número de uma célula, desde que não seja uma célula fixa do tabuleiro original.

- Visualizar o jogo: Exibe o estado atual da grade do Sudoku no terminal, mostrando os números inseridos e as células vazias.

- Verificar o status do jogo: Avalia e informa o estado atual do jogo (se está incompleto, completo ou se contém erros), ajudando o jogador a saber onde precisa corrigir.

- Limpar o jogo: Reseta todos os números inseridos pelo jogador, voltando o tabuleiro ao seu estado inicial (apenas com os números fixos).

- Finalizar o jogo: Verifica se o jogo foi concluído com sucesso e sem erros, parabenizando o jogador pela vitória.
  
## 🛠️ Tecnologias e Conceitos Abordados

- **Java** (JDK).
- **Orientação a Objetos** (`Classes, métodos, encapsulamento`).
- **Estrutura de dados com lista de listas** (`List<List<Space>>`).
- **Entrada/Saída via console** (`Scanner`).
- **Lógica de jogo** (`Validações para checar o status do jogo e se os números inseridos estão corretos`).

## 💻 Demonstração

Exemplo de execução no console:

  ```console
Selecione uma das opções a seguir:

1 - Iniciar um novo Jogo  
2 - Colocar um novo número
3 - Remover um número     
4 - Visualizar jogo atual
5 - Verificar status do jogo
6 - limpar jogo
7 - Finalizar jogo
8 - Sair
   ```

## 💭 Futuras melhorias

Meu objetivo é aprimorar o jogo de Sudoku com novas funcionalidades e tornar a experiência de jogo mais rica. Algumas das melhorias que planejo implementar incluem a criação de uma interface gráfica, o que tornaria a experiência ainda mais intuitiva e prática. Além disso, outra implementação interessante seria a de níveis de dificuldade para o jogo, como por exemplo: iniciante, intermediário e vançado.

## 🚀 Como executar?

### Pré-requisitos

1. Possuir instalação do JDK em sua máquina.
   
2. Possuir uma IDE que permita a utilização do Java, como por exemplo o VSCode ou IntelliJ.

### Execução

1. Clone o repositório em sua máquina local:
   ```bash
   git clone https://github.com/Walmir07/sudoku_game.git
   ```
2. Compile o arquivo principal (Main.java):

   ```bash
   javac src/br/com/walmir/Main.java
   ```
3. Execute o arquivo principal (Main.java), passando a configuração do tabuleiro como argumentos de linha de comando, com cada par entre aspas duplas (""):
   
   ```bash
   java -cp src br.com.walmir.Main "0,0;5,true" "0,1;3,true" "0,4;7,true" "1,0;6,true" "1,3;1,true" "1,4;9,true" "1,5;5,true" "2,1;9,true" "2,2;8,true" "2,7;6,true" "3,0;8,true" "3,4;6,true" "3,8;3,true" "4,0;4,true" "4,3;8,true" "4,5;3,true" "4,8;1,true" "5,0;7,true" "5,4;2,true" "5,8;6,true" "6,1;6,true" "6,6;2,true" "6,7;8,true" "7,3;4,true" "7,4;1,true" "7,5;9,true" "7,8;5,true" "8,4;8,true" "8,7;7,true" "8,8;9,true"
   ```

## 📜 Licença

Este projeto está licenciado sob a **MIT License** - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👤 Autor
- **Walmir Lima** – [@Walmir07](https://github.com/Walmir07)
