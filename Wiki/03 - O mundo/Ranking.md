---
tipo: wiki
capitulo: O mundo
fonte: pokemon.txt (Wiki PokeIdle)
---

# Ranking

O placar do mundo inteiro, não do seu servidor. Oito abas:

| Aba | O que ordena |
| --- | --- |
| Treinadores | nível do treinador (desempate por XP) |
| Pokémon Forte | o **poder** de um pokémon, de qualquer treinador |
| Top Catch | **espécies diferentes** capturadas **com bola nesta semana**, não capturas totais; zera toda semana e paga diamante (ver abaixo) |
| Top Coins | ouro acumulado na conta |
| PvP Ranqueado | o rank e o PR (ver PvP Ranqueado) |
| Bosses | vitórias em boss: em **Todos** (o padrão da aba), a soma de todos os bosses; ou as de um boss só, escolhido no seletor |
| Guild Diário | GP da guild, que dá o bônus de XP e loot (ver Guilds) |
| Guild Global | GP somado das guerras do mês, com prêmio em diamantes; zera todo mês |

Clicar num nome abre o perfil público do treinador — stats, Pokédex, o rank do PvP Ranqueado e a equipe dele no PvP, sem dados de conta. O mesmo perfil abre pelo chat e pela lista de amigos.

### Top Catch da semana

O Top Catch conta quantas **espécies diferentes** você capturou **com bola nesta semana**. Se nesta semana você capturou Pikachu, Rattata e Pidgey com bola, o seu Top Catch é **3**; outro Pikachu na mesma semana não muda nada, e uma espécie nova soma mais 1.

- **Zera toda semana**, no mesmo instante da virada do PvP Ranqueado: **sábado, 23h59 (horário de Brasília)**. A semana vai de domingo a sábado.
- **A sua Pokédex não zera.** Quem volta a 0 é só o placar. Por isso vale capturar de novo o que você já tem: na semana nova, a espécie conta outra vez.
- **Conta:** a captura com bola na hunt (jogada por você ou pelas automações **Lançar até Capturar** e **Lançar sem Parar**) e na Arena Mística.
- **Não conta:** evoluir com pedra (nem a Mega), chocar ovo na Chocadeira e comprar no Mercado.

**Por que só a bola?** O Top Catch paga diamante. Se a evolução contasse, daria para subir no placar sem caçar: comprar pré-evoluções no Mercado e evoluir com pedra. Com a bola, cada espécie do placar é uma captura de verdade, na hunt.

> **A semana de estreia.** Na primeira semana do Top Catch semanal, o placar ainda conta a sua **Pokédex inteira** — tudo que você já capturou, como era o Top Catch de antes —, para que quem liderava não perca o lugar no dia da troca. Da primeira virada em diante, o placar zera e passa a valer a regra da bola.

Na virada, a **posição final** da semana paga diamante:

| Posição | Prêmio |
| --- | --- |
| 1º | 50 💎 + selo da Poké Ball no chat |
| 2º–10º | 20 💎 |
| 11º–100º | 5 💎 |

- O resultado sai uns **dois minutos depois da virada**. Quem está online recebe na hora, com a tela de prêmio; quem está fora recebe no **próximo login** — não precisa estar online na virada, e o prêmio não vence.
- Desempate: o **nível** do treinador; se empatar também, fica na frente a **conta mais antiga**.
- Conta banida não recebe, e a posição dela não passa para o seguinte. Quem terminou a semana com 0 espécies não recebe.
- O **1º da semana** usa o **selo da Poké Ball** ao lado do nick no chat. O selo é **ao vivo**: passa para quem ultrapassar (o jogo confere a cada 2 minutos).
- O diamante do prêmio é para usar na Loja: como os outros brindes, ele não vai para o Mercado da Comunidade. Uma semana paga no máximo 680 💎, somando as 100 posições.

O painel da semana — as suas espécies, o relógio até a virada, a sua posição e o pódio — fica na Pokédex, no **Top Catch**; na aba Top Catch do Ranking, um botão leva direto para ele.

### Prêmio do mês: Treinadores, Top Coins e Bosses

No dia 1º de cada mês, às **00:00 de Brasília** (o relógio da Temporada Global de guilds), quem estiver nesses três placares ganha diamante pela posição — no de Bosses, vale o **Todos**, a soma das vitórias em todos os bosses (o Top Catch tem prêmio próprio, toda semana — ver acima):

| Posição | Prêmio |
| --- | --- |
| 1º | 100 💎 + selo no chat |
| 2º–10º | 50 💎 |
| 11º–100º | 25 💎 |

- Quem está em **1º** em cada placar usa um **selo ao lado do nick no chat**: o **Ash** (a primeira logo do jogo) no Top Treinadores, a **moeda** no Top Coins e a **coroa de boss** no Top Bosses — e a **Poké Ball** é do 1º do Top Catch **da semana**. O selo é **ao vivo**: passa para quem ultrapassar (o jogo confere a cada 2 minutos).
- Vale a posição **na hora do fechamento**. Estes três placares não zeram — o jogo não zera nível, ouro nem vitórias —, então o prêmio é de quem segue no topo quando o mês vira.
- Os três mostram até o **100º**. Conta banida no fechamento não recebe, e a posição dela não passa para o seguinte.
- O diamante do prêmio é para usar na Loja: como os outros brindes, ele não vai para o Mercado da Comunidade. No máximo 8.400 💎 por mês, somando os três placares.

### Pokémon Forte — como o ⚔ é calculado

Usa a **mesma força de nascimento** da calculadora (soma dos seis stats, normalizada), mas multiplica pelo **nível** do pokémon. Treinar sobe no placar; a nota da calculadora não. Detalhes em Nota, Poder e Calculadora.

```
score = mesma força da nota (0–1) poder = arred( nível × 10 × score )
```

A exceção é o lendário e o mítico: o ⚔ deles leva o **×4** em todos os stats, que a nota não leva — por isso um lendário sobe no placar muito acima do que a nota escondida dele diria.

A aba mostra essa fórmula no topo do placar.

**A coroa.** O 1º do Pokémon Forte leva a **coroa do Ranks** antes do nome — na placa em cima dele no campo (na hunt do dono), na Equipe e na ficha. É só a coroa, sem outro prêmio, e ela passa para quem ultrapassar em até 2 minutos.

> O placar sai do banco, não da memória do jogo, e é uma foto renovada a cada 10 segundos: o que você vê pode estar até uns **15 segundos** atrasado. Para um ranking, é irrelevante.
