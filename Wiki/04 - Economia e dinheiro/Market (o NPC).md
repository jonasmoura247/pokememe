---
tipo: wiki
capitulo: Economia e dinheiro
fonte: pokemon.txt (Wiki PokeIdle)
---

# Market (o NPC)

O balcão do jogo. Compra e venda com o **NPC**, em **ouro**, sem taxa nenhuma e em quantidade ilimitada. Três abas.

### Compra

- **Pokébolas** — as compráveis, aos preços da tabela.
- **Poções** e **Revives** — todas as variantes, ao preço de catálogo.
- **Ovos** — os três Mystery Eggs da Chocadeira.

O **Bronze Boss Token** (entrada de boss) **não** se compra aqui — é drop raro na Outland (0,0500% por kill) e prêmio do Passe de Batalha. Essa é a chance na Outland 1 — os degraus de cima multiplicam até **×8** (ver Bosses).

### Venda

Tudo que os pokémon dropam, pelo valor de catálogo (**100%** do preço de NPC — não há desconto). Há um botão de **vender todo o loot** para o inventário inteiro.

- O **cadeado** no card **tranca** um item: ele fica fora do "vender todo" até você destrancar.
- A **Venda Automática**, ao lado do botão, vende sozinha o loot que cai na hunt — e, ao ligar, já vende o que está na bolsa. Os itens trancados ficam de fora.

> **Consumível que o NPC vende, o NPC não recompra.** Poção e revive entram nessa regra. O Bronze Boss Token também **não** pode ser vendido ao NPC — anuncie no Mercado da Comunidade se quiser passar adiante.

Bola e poção sobrando na bolsa? A **Lixeira**, na aba **Treinador** da Bolsa, joga fora a quantidade que você escolher (ou **Tudo**). Ela só aceita bolas, poções e revives, e o que vai para ela **some para sempre** — não há como desfazer.

### Venda de Pokémon

```
preço = valorBase × (1 + nível/50) × qualidade × (shiny ? 10 : 1)
```

- O **valorBase** é o da espécie, do catálogo.
- Nível e qualidade valorizam; **shiny vale 10×**.
- Repare que a **potência não entra** nesta conta — o NPC não paga por ela. Um P4 ou P5 vale muito mais no Mercado da Comunidade, com outro jogador.

O **Ordenar por** da lista arruma por nível, qualidade, potência, nota da calculadora, **Maior IV Total** (a soma dos seis IVs), cada IV separado, tipo, **Nº da Pokédex** ou captura mais recente. A mesma lista serve à escolha da Oferenda e ao anexo do chat.

Não dá para vender quem está lutando, nem o último pokémon. "Vender todo o Depot" nunca toca em quem está na equipe. Com um filtro ligado (busca por nome ou apelido, tipo, shiny, ou o funil de potência, qualidade e IV mínimo de cada stat), o botão vira **Vender todo o Depot (Filtrado)** e vende só o que a lista está mostrando — a confirmação avisa quem não está na Coleção e seria perdido.

### A Coleção

Os pokémon que você quer **guardar** vão para a **Coleção**: eles saem desta lista e do "vender todo o Depot", e o NPC não os compra.

- A **setinha** no canto do card manda o pokémon para a Coleção. No Depot (Centro de Cerulean), os guardados têm duas abas, **Depot** e **Coleção**, e a mesma setinha leva de uma para a outra. A Coleção também abre de qualquer lugar, na aba **Coleção** da Bolsa.
- Mover não troca o pokémon de lugar nenhum: é uma marca. Ele continua valendo no Mercado da Comunidade, na Oferenda e nas equipes, com uma **★**. Nesses seletores, o filtro **Local** mostra só a Equipe, o Depot ou a Coleção.
- Cada pokémon espera alguns segundos antes de mudar de lado de novo.
- **Auto Coleção** manda sozinho para a Coleção os shinys, os P5 e quem tem nota a partir da que você escolher (interruptores ao lado do "vender todo"). Pokémon comprado no Mercado da Comunidade e pokémon refinado também chegam na Coleção.
- **Pastas**: dentro da Coleção você cria até **5 pastas**, com nome e ícone ("PvP", "GvG", "Torneio", "Evoluir para Mega"…) — a Coleção de sempre é a **Geral**, e a aba Coleção da Bolsa mostra uma pasta de cada vez. No **⋮** da ficha de um pokémon seu, **Mover para** leva ele a uma pasta (do Depot, isso já o guarda na Coleção). É só organização: em qualquer pasta ele continua fora da venda ao NPC, e apagar uma pasta devolve os pokémon dela à Geral.
