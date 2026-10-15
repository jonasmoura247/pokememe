---
tipo: wiki
capitulo: Luta e captura
fonte: pokemon.txt (Wiki PokeIdle)
---

# Tipos: forças e fraquezas

A efetividade é **multiplicativa nos dois tipos** do defensor. Água contra Rocha/Terra é ×2 × ×2 = **×4**.

```
efetividade = tabela[atacante][tipo1] × tabela[atacante][tipo2]
```

### Na hunt a vantagem é 1.5× mais forte

É a mecânica mais específica deste jogo, e vale **nos dois sentidos**: bater no tipo certo compensa muito mais, e bater no errado dói muito mais.

| Normal | Na hunt |
| --- | --- |
| ×0 | ×0 |
| ×0,25 | ×0,167 |
| ×0,5 | ×0,333 |
| ×1 | ×1 |
| ×2 | ×2,5 |
| ×4 | ×5,5 |

> Imunidade (×0) e neutro (×1) **não** mudam. Fogo contra Água vira **×0,33** — é literalmente por isso que um Charmander não encara um Magikarp: com HP ×5 ele simplesmente não morre.

### A tabela completa

Linha = tipo do **golpe**. Coluna = tipo do **defensor**. Célula vazia é neutro (×1). Passe o mouse para ver o valor já amplificado da hunt.

| Golpe ↓ | NOR | FOG | AGU | PLA | ELE | GEL | LUT | VEN | TER | VOO | PSI | INS | ROC | FAN | DRA | SOM | MET | FAD |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| NOR |  |  |  |  |  |  |  |  |  |  |  |  | 0,5 | 0 |  |  | 0,5 |  |
| FOG |  |  | 0,5 | 2 |  | 2 |  |  |  |  |  | 2 | 0,5 |  | 0,5 |  | 2 |  |
| AGU |  | 2 |  | 0,5 |  |  |  |  | 2 |  |  |  | 2 |  | 0,5 |  |  |  |
| PLA |  | 0,5 | 2 |  |  |  |  | 0,5 | 2 | 0,5 |  | 0,5 | 2 |  | 0,5 |  | 0,5 |  |
| ELE |  |  | 2 | 0,5 |  |  |  |  | 0 | 2 |  |  |  |  | 0,5 |  |  |  |
| GEL |  | 0,5 | 0,5 | 2 |  |  |  |  | 2 | 2 |  |  |  |  | 2 |  | 0,5 |  |
| LUT | 2 |  |  |  |  | 2 |  | 0,5 |  | 0,5 | 0,5 | 0,5 | 2 | 0 |  | 2 | 2 | 0,5 |
| VEN |  |  |  | 2 |  |  |  |  | 0,5 |  |  |  | 0,5 | 0,5 |  |  | 0 | 2 |
| TER |  | 2 |  | 0,5 | 2 |  |  | 2 |  | 0 |  | 0,5 | 2 |  |  |  | 2 |  |
| VOO |  |  |  | 2 | 0,5 |  | 2 |  |  |  |  | 2 | 0,5 |  |  |  | 0,5 |  |
| PSI |  |  |  |  |  |  | 2 | 2 |  |  |  |  |  |  |  | 0 | 0,5 |  |
| INS |  | 0,5 |  | 2 |  |  | 0,5 | 0,5 |  | 0,5 | 2 |  |  | 0,5 |  | 2 | 0,5 | 0,5 |
| ROC |  | 2 |  |  |  | 2 | 0,5 |  | 0,5 | 2 |  | 2 |  |  |  |  | 0,5 |  |
| FAN | 0 |  |  |  |  |  |  |  |  |  | 2 |  |  |  |  | 0,5 |  |  |
| DRA |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 0,5 | 0 |
| SOM |  |  |  |  |  |  | 0,5 |  |  |  | 2 |  |  | 2 |  |  |  | 0,5 |
| MET |  | 0,5 | 0,5 |  | 0,5 | 2 |  |  |  |  |  |  | 2 |  |  |  |  | 2 |
| FAD |  | 0,5 |  |  |  |  | 2 | 0,5 |  |  |  |  |  |  | 2 | 2 | 0,5 |  |
