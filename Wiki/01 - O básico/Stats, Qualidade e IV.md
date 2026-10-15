---
tipo: wiki
capitulo: O básico
fonte: pokemon.txt (Wiki PokeIdle)
---

# Stats, Qualidade e IV

Dois pokémon da mesma espécie e do mesmo nível quase nunca são iguais. O que os separa são três números sorteados **na captura** e que **nunca mais mudam**: **qualidade**, **IV** e **potência**.

```
stat = arred( (base + 2 × IV) × nível/100 × qualidade^expoente × multiplicador ) somaStats = hp + atk + def + spAtk + spDef + speed
```

### IV — 1 a 32 por stat

Seis sorteios independentes, de **1 a 32** cada (máximo somado: 192). Evoluir **não** rerola nada.

### Speed e IV de SPD — recarga, não corrida

O **IV de Velocidade (SPD)** é sorteado separado, como os outros cinco. Nem ele nem o stat de SPD entram na fórmula de dano ou aceleram a corrida na hunt — o pokémon sempre corre um pouco na frente do treinador por design da cena. O que muda é a **recarga**: nos golpes, o **Speed base da espécie** dá até 7% de desconto e o IV de SPD decide quanto disso o pokémon aproveita (IV 32, tudo; IV 16, metade); na Investida e no intervalo entre ataques só o IV conta, **−0,01 s por ponto** (IV 32 → −0,32 s), fixo no nascimento. A conta inteira está em Combate. Sp.ATK e Sp.DEF só entram em golpes **especiais**.

### Qualidade — o número que mais pesa

Ela entra em **cada stat** como expoente (`qualidade^expo`) — por isso muda o bicho inteiro e vale mais que o IV isolado. A linha `somaStats` acima é só a **soma dos seis stats** (útil na Pokédex para comparar potências). A **nota** e o **⚔** usam essa força de nascimento — ver Nota, Poder e Calculadora.

### Como nasce a qualidade

**Não é calculada** a partir dos IVs, da potência, do shiny nem do nível. Na captura o jogo sorteia **uma faixa** (pelas chances da tabela abaixo) e, dentro dela, um valor aleatório entre o mínimo e o máximo — com três casas decimais. Esse número fica para sempre; evoluir não muda nada.

> Um pokémon com IV no teto e potência V pode nascer com q**1,0** (Comum) ou q**1,7** (Lendária): são três sorteios **independentes** na mesma captura. IV alto **não** puxa a qualidade para cima.

| Qualidade | Chance | Rótulo |
| --- | --- | --- |
| 0,8 – 0,9 | 5,00% | Fraca |
| 0,9 – 1 | 5,00% | Fraca |
| 1 – 1,1 | 34,0% | Comum |
| 1,1 – 1,2 | 20,0% | Incomum |
| 1,2 – 1,3 | 10,0% | Incomum |
| 1,3 – 1,4 | 10,0% | Rara |
| 1,4 – 1,5 | 10,0% | Rara |
| 1,5 – 1,6 | 5,00% | Épica |
| 1,7 – 1,8 | 0,67% | Lendária |
| 1,8 | 0,29% | Lendária |

> A faixa **1,6 – 1,7 é um buraco intencional**: nenhum pokémon nasce nela. O teto do sorteio é exatamente **1,8** (~0,29% de chance). O shiny não ganha qualidade extra — ele fica mais forte pelo **×3 nos stats** e pelos IVs rerolados, não por um q maior.

O expoente muda por stat: **0,95** para HP e Velocidade, **0,8** para os outros quatro. O efeito do **Speed** e do **IV de SPD** no combate (recarga, não corrida) está em Combate.

### HP de combate

```
hpDeCombate = máx(24, arred(hp × 12))
```

Um selvagem ainda leva **×5** por cima disso — ver Combate.

### Refino — o “+1” comprado com pedra

É o único jeito de mexer na **base** de um pokémon depois que ele nasceu. Cada degrau soma **+1** permanente a um stat-base, e o ganho entra **antes** de tudo o mais na fórmula lá em cima — ou seja, é multiplicado por nível, qualidade e potência. O mesmo degrau que vale +1 num nível 100 comum vale 6 vezes isso num P5 shiny — e 24 num lendário P5 shiny.

Você paga na **pedra de evolução do tipo do próprio pokémon** — a mesma com que ele evolui, e a comum mesmo se ele for shiny. Forma final também refina: o Dragonite não evolui para lugar nenhum, mas usa Ancient Stone como qualquer outro DRAGON.

Quem tem **dois tipos** aceita a pedra de **qualquer um deles**, e as duas somam: num Charizard, 300 Feather Stone + 200 Fire Stone fecham um degrau de 500. Na tela do refino você **escolhe quanto sai de cada pedra**.

```
ter +N num stat = 500 × N³ pedras, somando tudo custo do degrau N = 500 × (3N² − 3N + 1)
```

| Grau | Custo do degrau | Total investido |
| --- | --- | --- |
| +1 | 500 | 500 |
| +2 | 3.500 | 4.000 |
| +3 | 9.500 | 13.500 |
| +4 | 18.500 | 32.000 |
| +5 | 30.500 | 62.500 |
| +6 | 45.500 | 108.000 |
| +8 | 84.500 | 256.000 |
| +10 | 135.500 | 500.000 |
| +15 | 315.500 | 1.687.500 |
| +20 | 570.500 | 4.000.000 |

> **Não há teto.** Quem quiser continuar subindo, sobe — quem decide o ritmo é o preço. A curva é cúbica, e não exponencial, exatamente por isso: dobrando, o vigésimo degrau custaria 262 milhões de pedras e existiria um teto de fato escondido na fórmula.

> O custo é **por stat**, não por pokémon. Quem colocou quatro degraus no HP paga 30.500 pelo quinto — mas o primeiro de ATK continua custando 500. Refinar é **escolher** onde o bicho vai ser bom, não encher uma barra.

**O SPD não refina**, e não é esquecimento: o stat de SPD não entra em combate nenhum — quem acelera os ataques é o **Speed base da espécie** com o **IV** de Speed, ali em cima, e o refino não mexe em nenhum dos dois. Vender “+1 SPD” seria vender um número que não faz nada.

A **nota N=** e o **⚔** sobem com o refino — usam a base atual (espécie + +N). TM elemental e held items não entram na nota. O selo **+N** ao lado do nome mostra quanto já foi investido; os stats de verdade sobem na ficha.

O “+” fica em dois lugares: no cabeçalho do painel **Em campo** e em cada linha de **Stats-base** na ficha de um pokémon seu. Refinar manda o pokémon para a sua Coleção, fora da venda ao NPC — devolva ao Depot se quiser mesmo vendê-lo.

### O piso do starter

O primeiro pokémon **não** passa pelo sorteio livre. Ele nasce com qualidade **≥ 1,30**, soma de IVs **> 140** e nenhum IV abaixo de **16**. Sem isso, um em cada dez treinadores começaria com um bicho da banda "Fraca" e a primeira hunt seria intransponível.
