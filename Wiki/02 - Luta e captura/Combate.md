---
tipo: wiki
capitulo: Luta e captura
fonte: pokemon.txt (Wiki PokeIdle)
---

# Combate

O pokémon ativo anda até o selvagem **mais próximo** e só troca golpes quando **encosta** nele. Nada de dano voando de um lado a outro do mapa.

### O dano

```
base = ((2 × nível/5 + 2) × power × atk/def) / 50 + 2 final = base × STAB × efetividade × aleatório(0,85–1,00)
```

- **power** é o do golpe usado — ver **Os golpes**, logo abaixo.
- **STAB** é **×1,5** quando o golpe é de um dos tipos do próprio pokémon.
- **atk/def** usa Ataque e Defesa em golpe físico, e Sp.Atk / Sp.Def em especial.
- **efetividade** vem da tabela de tipos, já amplificada.

### Os golpes

O pokémon escolhe sozinho, a cada ataque, o golpe de **maior dano esperado** contra aquele alvo entre os que já recarregaram — pesando o poder, o STAB, a efetividade de tipo e o Ataque (ou Sp.Atk) dele contra a defesa do alvo. Enquanto todos recarregam, vem a Investida (abaixo).

A **recarga** de cada golpe sai do **poder** dele, numa curva única para o catálogo inteiro. Até 100 de poder o golpe paga a recarga quase na proporção; acima disso o golpe caro fica cada vez mais barato — é o que mantém o golpe de 600 valendo a pena.

| Poder do golpe | Recarga |
| --- | --- |
| 15 | 10 s |
| 40 | 15,9 s |
| 60 | 20,6 s |
| 80 | 25,3 s |
| 100 | 30 s |
| 120 | 31,2 s |
| 150 | 33 s |
| 300 | 42 s |
| 600 | 60 s |
| 600 (golpe de mega) | 30 s |

- **Toda última evolução tem dois golpes de 600** — um de cada tipo nas de tipo duplo, dois do mesmo tipo nas de tipo único —, com 60 s de recarga. A categoria (física ou especial) segue o lado de ataque mais forte da espécie, a não ser que a planilha dela escolha outra. A Mega ganha um terceiro, na metade da recarga (ver Mega Evolução).
- Os lendários e míticos vão além: **14 golpes, quatro de 600** — dois de cada tipo, ou os quatro do tipo único. Phione e Poipole, que evoluem (para Manaphy e Naganadel), ficam com dez golpes e dois de 600. O clone de Orre herda a lista.
- Cada golpe libera num **nível**; nas espécies refeitas pelas planilhas de balanceamento, todos liberam no nível 1. A ficha da Pokédex mostra a lista inteira.
- O **Speed** encurta a recarga dos golpes em até 7%: o Speed base da espécie com o IV de SPD (abaixo).

### O ataque básico

Enquanto todos os golpes estão carregando, o pokémon dá uma **Investida**: power **30**, a cada **2 s**, no tipo dele. Sem ela um Caterpie daria dois golpes e ficaria dez segundos parado. Se o alvo for imune aos dois tipos dele, só um golpe de verdade resolve.

- Ela é **física**: entra na fórmula com **Ataque** contra a **Defesa** do alvo, nunca com Sp.Atk / Sp.Def. Quem tem ATK baixo e Sp.Atk alto (um Alakazam tem **50** contra **135**) quase não arranha com o básico e vive dos golpes de verdade.
- Como ela sai no tipo do próprio pokémon, o **STAB ×1,5 vale sempre**: os **30** de power rendem como 45.
- Em pokémon de dois tipos ela tenta o **primeiro**, e só passa para o segundo se o alvo for **imune** ao primeiro — não é o melhor dos dois contra aquele alvo.
- Os **2 s** encurtam só com o **IV de SPD**: −10 ms por ponto, até 1,68 s com IV 32 (abaixo).

### Speed — a recarga dos golpes e o ataque básico

O stat **SPD** da ficha **não** entra na fórmula de dano nem acelera a corrida na hunt. Quem acelera os ataques são o **Speed base da espécie** e o **IV de SPD** (1–32, sorteado na captura), cada um no seu lugar:

- **Golpes** (skills e ultimates): o Speed base dá um **potencial** de desconto — cada 20 de Speed vale 1%, até 6% no 120; acima disso, cada 40 vale mais 1%, até o teto de 7%. O IV de SPD decide quanto desse potencial o pokémon aproveita: IV 32 aproveita tudo; IV 16, metade.
- **Investida e intervalo entre ataques**: só o IV de SPD, **10 ms por ponto** (até −320 ms), com piso de 400 ms — a Investida de 2 s vira 1,68 s com IV 32, e o intervalo entre os seus golpes, de 0,9 s, vira 0,58 s.

```
potencial = Speed ÷ 20 (Speed até 120) = 6 + (Speed − 120) ÷ 40 (acima de 120; teto de 7%) desconto = potencial × IV de SPD ÷ 32 recarga = recarga × (1 − desconto ÷ 100)
```

Um Jolteon (Speed 130) tem 6,25% de potencial; com IV 24 ele aproveita 75% disso — 4,69% a menos —, e o golpe de 60 s recarrega em 57,2 s. Com IV 32:

| Espécie | Speed base | Potencial (IV 32) | Golpe de 600 (60 s) |
| --- | --- | --- | --- |
| Snorlax | 30 | 1,5% | 59,1 s |
| Tyranitar | 61 | 3,05% | 58,2 s |
| Zoroark | 105 | 5,25% | 56,9 s |
| Jolteon | 130 | 6,25% | 56,3 s |
| Ninjask | 160 | 7% | 55,8 s |

A regra é a mesma na hunt, nos bosses, no PvP Ranqueado e na Guerra de Guildas.

### A recarga é do pokémon

A recarga de um golpe só corre com o pokémon **em campo**. Trocar o ativo **pausa** o que falta, guardado com ele; quando ele volta, a recarga continua de onde parou. Trocar por tática (tipo contra tipo) não custa nem rende um décimo de segundo — o que deixou de existir foi soltar o golpe de 600 de cinco pokémon seguidos e voltar ao primeiro com a recarga já vencida.

- A cura da Enfermeira, no Centro, **não** zera a recarga.
- Só as arenas pagas zeram: entrar num Boss ou na Arena Mística começa com tudo pronto.
- PvP, Guerra de Guilds, ginásio e campeonato são lutas simuladas à parte: todo mundo entra com a recarga limpa.

### Movimento na hunt

O pokémon ativo corre um pouco **na frente** do treinador — é ritmo da cena (260 ms vs 290 ms por tile), não stat SPD. Com IV alto você **ataca** mais rápido e passa mais tempo correndo entre alvos, o que pode parecer que “disparou”, mas a velocidade de passo não mudou.

### O selvagem joga com vantagem

| Regra | Valor |
| --- | --- |
| HP do selvagem na hunt | ×5 |
| Dano do selvagem por golpe | ×1.8 |
| Intervalo mínimo entre golpes seus | 0,9 s |
| Intervalo mínimo entre golpes dele | 1,4 s |

Não é injustiça: é o que faz uma hunt no seu nível ser uma luta, e não uma fila.

### Ondas e corpos

Os selvagens nascem em **ondas**, nos pontos de spawn da área. Quando o campo esvazia, a onda seguinte entra em poucos segundos. Quem cai **fica no chão por 30 segundos** — e é nele que se joga a bola.

De **Unova em diante**, toda área tem o **mesmo ritmo**: os selvagens nascem em **bandos** espalhados pelo mapa, calibrados para o mesmo time limpar a onda no mesmo tempo em qualquer hunt dali — e para a bicicleta render o mesmo em todas.

### Drop na Outland

Na **Outland**, o loot da espécie é **só pedra de evolução** (tabela na **Pokédex**) — os itens comuns, que só serviam para vender ao NPC, não caem lá. Além das pedras, selvagens derrotados na Outland podem soltar **1× Bronze Boss Token** — entrada de boss — e os fragmentos de Chave, Shiny Stone e Bicicleta. Kanto e Orre não dropam o token. O ouro de cada abate é o mesmo; só a venda automática não tem mais o que vender lá.

| Item | Chance | Quando |
| --- | --- | --- |
| Bronze Boss Token | 0,0500% · 1 / 2.000 | kill na Outland |

> Média de ~2.000 derrotas por token na Outland 1 — as outras Outlands multiplicam essa chance (tabela logo abaixo). O Loot Boost da Loja, o bônus de ranking da guild e os eventos de farm aumentam a chance. O NPC não compra — preço só no Mercado da Comunidade.

### As 8 Outlands

A aba **Outland** do Mapa tem um seletor com as **8 Outlands**. É o **mesmo mapa**, os **mesmos pokémon** e o mesmo nível 150 em todas — o que muda é a chance dos quatro drops raros da área (Bronze Boss Token, Fragmento de Chave, Fragmento de Shiny Stone e Fragmento de Bicicleta):

| Região | Nv treinador | Bônus |
| --- | --- | --- |
| Outland 1 | 150 | ×1 |
| Outland 2 | 500 | ×1,25 |
| Outland 3 | 1.000 | ×1,5 |
| Outland 4 | 2.000 | ×2 |
| Outland 5 | 4.000 | ×3 |
| Outland 6 | 8.000 | ×4 |
| Outland 7 | 16.000 | ×6 |
| Outland 8 | 25.000 | ×8 |

> O degrau vale para os **quatro raros ao mesmo tempo** e multiplica **depois** do Loot Boost. XP, ouro, captura e as pedras da espécie não mudam — quem sobe de Outland está comprando raridade, não velocidade.

### Evolução

Variantes de Outland **não evoluem** — um Ancient Pupitar não vira Ancient Tyranitar. Ver Evolução e pedras.
