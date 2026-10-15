---
tipo: wiki
capitulo: Luta e captura
fonte: pokemon.txt (Wiki PokeIdle)
---

# Captura

### As pokébolas

| Pokébola | Eficiência | Chance (corpo caído) | Preço |
| --- | --- | --- | --- |
| Poké Ball | ×1 | 0,99% | 5 ouro |
| Great Ball | ×2 | 1,98% | 20 ouro |
| Super Ball | ×3 | 2,97% | 50 ouro |
| Ultra Ball | ×4 | 3,97% | 130 ouro |
| Beast Ball | ×8 | 7,93% | *só com diamante* |

A chance é no corpo caído, para o tier mais fácil (raridade 1). Cada ficha de espécie na Pokédex mostra a tabela exata — a Beast Ball é sempre **2×** a Ultra Ball.

A **Beast Ball** é a mais forte e não se compra com ouro — só em pacotes na Loja de Diamantes.

### A chance por arremesso

```
raridade = log10(máx(100, preçoNpc)) − 1 fator = 1 + raridade³ / 17 chance = 0.0075 × (eficiência / fator) × (1,4 − hpAtual/hpMáximo)
```

Limitada entre **0,30%** e **10,0%**. Três coisas decidem tudo:

- **Quanto o pokémon vale** (o preço de NPC dele, em escala logarítmica). Um Pidgey sai fácil; um Dragonite, não.
- **A bola.** A eficiência entra multiplicando direto.
- **O HP do alvo.** A bola só vai em quem já caiu, e corpo tem HP zero — que é a ponta boa da fórmula.

> **Capturar é difícil de propósito.** Com a MELHOR bola, num corpo caído, a espécie mais fácil do jogo dá **7,93%** e a mediana dá **3,17%** — e daí para cima cai rápido. A ficha de cada espécie na Pokédex mostra a tabela exata, bola por bola, com quantas derrotas isso significa na média.

### É uma tentativa por corpo

Se a bola falhar num **corpo caído**, ele some do mapa. Não dá para despejar bolas no mesmo alvo até sair — o custo por captura existe justamente por isso. Um selvagem **vivo** continua em campo quando a bola falha, porque ele ainda está lutando.

### O nível do capturado

O selvagem **luta** no nível da hunt; o capturado **nasce** no teto da espécie. O teto sai da cadeia evolutiva dela:

```
cadeia de 3 (Treecko → Grovyle → Sceptile) 20 · 40 · 100 cadeia de 2 (Makuhita → Hariyama) 40 · 100 não evolui (Spinda, variantes de Outland) 100
```

**Até o Nv 100 nada muda** — Kanto e Johto inteiras entregam o bicho no nível em que ele estava caído. Acima disso o teto manda: um Torterra derrubado numa hunt de 3.500 entra na equipe no **Nv 100**, e um Turtwig, no **Nv 20**.

A **evolução das espécies nacionais** segue a mesma escada: quando o destino mora em hunt de Nv 100+, o elo pede o **teto do destino** (40 ou 100), não o nível da hunt onde ele aparece. O caminho é capturar no 20, treinar até 40, evoluir; treinar até 100, evoluir de novo. **Variantes de Outland (#2001+) não entram nessa conta — não evoluem** (ver capítulo Evolução).

> Cada ficha da Pokédex tem a linha **Nível ao capturar**, e o painel dos caídos mostra o "→ Nv" antes de você gastar a bola. O bicho continua valendo o que vale — ele só chega para ser treinado, e não pronto.

### O que aumenta

- **Capture Boost** (Loja) — **dobra** a chance por arremesso, respeitando o teto de 10,0%.
- **Bônus na Kick** — +15% por hora resgatada com pontos do canal, multiplicando com o boost da Loja (ver Bônus de live).
- **Bola melhor** — a Poké Ball é a mais barata *por arremesso*, mas a Ultra e a Beast gastam menos tempo.

> O lendário da Arena Mística não segue esta fórmula: lá a chance é uma tabela por bola, igual para todos, e a tentativa é uma só.

### Automação

As opções **Lançar até Capturar** e **Lançar sem Parar** arremessam sozinhas nos corpos caídos, respeitando um intervalo de 1,2 s — a primeira para na captura, a segunda não. São um **benefício de VIP** — ver Automações.
