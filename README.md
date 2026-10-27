# Resolução - Lista IV

### De: Lauren Manica Conceição - Turma: 1F - Professor: Hewerton Oliveira - Disciplina: Desenvolvimento Web I

1. A diferença entre container e item é que o container é responsável por receber o display: flex; entretanto, a propriedade é refletida nos seus itens, localizados dentro do container.

2. O eixo principal, nesse caso, será o eixo horizontal, e sua direção será horizontal, no formato padrão do flex-direction (row).

3. A sobra de espaço numa faixa flex refere-se ao espaço livre e vazio entre os itens de um determinado container, que muitas vezes ocorre ao utilizarmos o Flexbox. Quando os itens dessa mesma faixa se encontram com flex-grow: 0, o espaço não é utilizado por nenhum deles.

4. O valor padrão de flex-grow é 0, o que significa que o item não ocupará nem usufruirá da sobra.

5. A mesa representa o contêiner-pai, o prato representa cada item e a pizza representa a sobra que ficou na mesa.

6. O valor de flex-grow: 1 faz com que a marca ocupe o espaço vazio da faixa.

7. Os pesos são de 1 + 2 + 3 = 6. Assim, devemos fazer 600 / 6 = 100px. Ou seja, cada item, por padrão, ocuparia 100px. Com isso:

Item com flex-grow: 1 ocupará 100px de largura.

Item com flex-grow: 2 ocupará 200px de largura.

Item com flex-grow: 3 ocupará 300px de largura.

8. Com flex-basis: 100px, cada item possui uma largura inicial de 100px, tendo como sobra 300px e utilizando 100px cada. Com isso, realizamos o cálculo de flex-basis + flex-grow (espaço extra):

Item com flex-grow: 0: 100px + 0px = 100px.

Item com flex-grow: 1: 100px + 100px = 200px.

Item com flex-grow: 2: 100px + 200px = 300px.

9. O flex-shrink é utilizado principalmente para conter a dimensão de um item, evitando que ele ultrapasse o limite de largura estabelecido pelo container. Seu valor padrão é 1, diminuindo os itens com base na medida do flex-basis e no valor de flex-shrink.

10. Com cada item possuindo 400px, eles ocupam 800px de uma faixa de 600px, ou seja, 200px a mais. Ao aplicarmos flex-shrink: 1 aos dois itens, eles perderão 100px cada, tornando-se 300px + 300px = 600px.

11. No caso anterior, se o primeiro item possuísse flex-shrink: 0, ele não encolheria, e o segundo item precisaria encolher para que ambos coubessem na faixa.

12. Um exemplo para o uso de flex-shrink: 0 pode ser um texto cujo espaço não desejamos que seja reduzido.

13. flex-basis é uma propriedade responsável por definir o tamanho do item antes de crescer ou encolher. O flex-basis seria o tamanho de partida, pois possui prioridade sobre a propriedade width quando definido com um valor diferente de auto.

14. Pois, ao adicionarmos flex-basis: 0 aos itens, significa: “parta do zero e reparta a faixa inteira”.

15.
| Atalho | flex-grow | flex-shrink | flex-basis |
| --- | --- | --- | --- |
| `flex: initial` | 0 | 1 | `auto` |
| `flex: 1` | 1 | 1 | 0% |
| `flex: auto` | 1 | 1 | `auto` |
| `flex: none` | 0 | 0 | `auto` |

Foi necessária a ajuda de IA para a formatação desta tabela!

17. Com dois itens de conteúdo de 100px e 300px em uma faixa de 600px, ao utilizarem flex: 1, a largura final de cada item será de 300px, pois, ao dividirmos a faixa pela soma dos pesos de cada um, temos 600px / 2 = 300px.

Já com flex: auto, com 400px de conteúdo no total, devemos reparar que sobram 200px. Nisso:

Item A representa 100/400 (25%) → 25% de 200px = 50px → 50px + 100px = 150px (largura final).

Item B representa 300/400 (75%) → 75% de 200px = 150px → 150px + 300px = 450px (largura final).

17. Falso, pois tudo isso não se limita apenas ao tamanho do conteúdo, mas também, por exemplo, ao peso no flex-grow e ao encolhimento com o flex-shrink.

18. O que pode barrar a propriedade flex-shrink: 1 é principalmente a propriedade min-width: auto. Para resolver esse problema, basta utilizar min-width: 0.

19. Ao criar um container composto por uma imagem e um texto, um deles pode se sobressair, ultrapassando os limites definidos mesmo com o uso de flex-shrink: 1, devido ao min-width: auto.

20.

a. A ordem estabelecida fará com que apareçam, respectivamente, na viewport, os itens C, A e B.

b. Ao apertar a tecla Tab, ela percorrerá os itens com base na estrutura do HTML, ou seja, A, B e C.

c. Devido à falta de funcionalidade da propriedade order na navegação pela tecla Tab, o leitor de tela tende a não seguir a ordem visual da página.

21. O valor padrão de order é 0. Entre order: -1 e order: 2, o primeiro a aparecer será o item com order: -1.

22. Com os itens-filhos sendo (A) align-self: flex-end, o item não se “esticará” para preencher o eixo transversal (vertical). Já com (B) align-self: auto, ele herdará o stretch do pai, passando a ter a altura necessária para preencher o eixo transversal.

23. Utilizamos align-self quando desejamos alterar um único item, enquanto align-items é utilizado para alterar o alinhamento de diversos itens dentro de um container.

24. Os itens de .pagina são header, .miolo e footer. Os itens de .miolo são aside e main.

25. Pois a propriedade display: flex de .pagina funciona apenas com os filhos diretos (header, .miolo e footer), e não com os itens de .miolo.

26. A declaração display: flex torna o container-pai flexível; flex-direction: column fará com que os itens se apresentem em colunas; min-height: 100vh dimensiona a altura mínima da classe .pagina.

A declaração flex: 1 definirá flex-grow como 1, flex-shrink como 1 e flex-basis como 0%. Já flex: 0 0 10rem define flex-grow como 0, flex-shrink como 0 e o valor-base (flex-basis) como 10rem.

E min-width: 0 define a largura mínima como 0, também facilitando o funcionamento do flex-shrink.

27. Quando desejamos modificar os filhos, o ideal é adicionar a propriedade flex-grow: 0 aos itens, e não ao container.

28. Podemos utilizar a propriedade flex-shrink, permitindo assim equalizar a situação dos itens dentro da faixa, ou, como visto na aula passada, utilizar flex-wrap, que leva um item para a linha de baixo, evitando que os limites sejam ultrapassados.

29.

flex-basis: o tamanho dos itens antes de crescer ou encolher.

flex-grow: o peso (favorecimento) de cada item em um container na divisão.

flex-shrink: a regularização da dimensão dos itens com base na dimensão da faixa.

order: a ordem de apresentação visual.

align-self: o alinhamento de um único item com base no eixo transversal.
