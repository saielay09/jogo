# Projeto Jogo da Velha
Este é um projeto de um jogo da velha onde 2 usuários podem competir escolhendo os símbolos "X" ou "O",
com a finaalidade de completar uma sequência de 3 símbolos iguais na horizontal, vertical ou diagonal

## Tecnologias utilizadas
- **HTML**: estrutura do site
- _CSS_: estilização do site
- *_JS_*: Funções do site
- ~~BootStrap~~: Não foi utilizado

### Melhorias possíveis
 1. [X] Subir para GitHubPages;
 2. [ ] Adicionar mensagens na tela;
 3. [ ] Adicionar a função da "velha" caso dê empate.

 
 ### Disponibilizado em 
 [GitHubPages](https://saielay09.github.io/jogodavelhaEberCiely/)
 
 
 ### Prints da tela
| ID | Primeira Tela | Segunda Tela |
|----|---------------|----------------|
| 1 | Jogo da velha Limpa| Jogo da Velha preenchida |
| 2 | ![image](https://user-images.githubusercontent.com/101192829/162212084-553c796c-3319-4234-b904-34a34dd1d9de.png)|![image](https://user-images.githubusercontent.com/101192829/162212232-64dc077a-4d79-4a16-bccc-0570b2039257.png)|


### Função principal
```
make_play(position) {
        if (this.gameover || this.board[position] !== '') return false;

        const currentSymbol = this.symbols.options[this.symbols.turn_index];
        this.board[position] = currentSymbol;
        this.draw();

        const winning_sequences_index = this.check_winning_sequences(currentSymbol);
        if (this.is_game_over()){
            this.game_is_over();
        }
        if (winning_sequences_index >= 0) {
            this.game_is_over();
            this.stylize_winner_sequence(this.winning_sequences[winning_sequences_index]);
        } else {
            this.symbols.change();
        }

        return true;
    },
```

### Links usados para o projeto
[Tic Tac Toe](https://www.youtube.com/watch?v=M258B1b_pMs)

### Descrição das alterações
Primeiramente foi feito o Jogo da Velha básico. E depois foi criado alguns recursos novos, como a função de recomeçar e colorir os quadrinhos do ganhador.

