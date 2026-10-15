---
tipo: referencia-tecnica
projeto: PokeIdle
atualizado: 2026-10-14
---

# Fórmulas e números-chave

Voltar: [[Pokemon]] · [[Glossario]]. Fonte de cada item: nota do capítulo indicada.

## Progressão e stats
```
xpTotal(L) = arred(50/3 × (L³ − 6L² + 17L − 12))                 [[Níveis e XP]]
stat       = arred((base + 2·IV) × nível/100 × qualidade^exp × multiplicador)
             exp = 0,95 (HP, Speed) · 0,8 (outros 4)             [[Stats, Qualidade e IV]]
hpCombate  = máx(24, arred(hp × 12))   (selvagem ×5)
refino +N  = 500 × N³ pedras no total; degrau N = 500(3N²−3N+1) [[Stats, Qualidade e IV]]
nota       = 10 × (score − pior) ÷ (melhor − pior)               [[Nota, Poder e Calculadora]]
poder ⚔    = arred(nível × 10 × score)
```
- Pokémon só entra se ≤ **5 níveis acima** do treinador (starter é exceção).
- Multiplicadores: potência P1–P5 = 1 / 1,05 / 1,1 / 1,25 / 2 · shiny ×3 · lendário ×4 → máx. ×24.
- Chances de potência: 74,5 / 20 / 5 / 0,5 / 0,005%. Faixas de nota: 10 degraus (Extremamente Fraco → Divino).

## Combate
```
dano = ((2·nív/5 + 2) · power · atk/def)/50 + 2  × STAB(1,5) × efet × rand(0,85–1)   [[Combate]]
recarga(poder): 15→10 s · 40→15,9 · 60→20,6 · 80→25,3 · 100→30 · 150→33 · 300→42 · 600→60 (mega 30)
desconto Speed = potencial × IV_SPD/32 (potencial até 7%) ; Investida 2 s − 0,01 s·IV
```
- Selvagem: HP ×5, dano ×1,8. Vantagem de tipo na hunt: ×2→×2,5 · ×4→×5,5 · ×0,5→×0,333 · ×0,25→×0,167 ([[Tipos- forças e fraquezas]]).
- TM Elemental: power 2800, CD 60 s, 3×3 no alvo · AoE 11×11 ([[TM Disks]]).
- Nível acima de 150 é **comprimido** em Ginásio/PvP/Guerra (nv 1.000 → 352 no ginásio, 219 na guerra); Showdown tem **teto 150**.

## Captura e raridade
```
raridade = log10(máx(100, preçoNpc)) − 1 ; fator = 1 + raridade³/17
chance   = 0,0075 × (eficiência/fator) × (1,4 − hp/hpMax)    limitada a 0,30%–10%   [[Captura]]
```
- Bolas: Poké ×1 (5) · Great ×2 (20) · Super ×3 (50) · Ultra ×4 (130) · Beast ×8 (só 💎).
- Shiny 1/24.000 (1/12.000 com Secret Lure) · Outland: sem shiny.
- Qualidade: 0,8–1,8 (buraco 1,6–1,7; teto ≈0,29%).
- Arena Mística: Poké 0,10% … Beast 0,50% (dobra com Capture Boost).
- Teto de captura: cadeia de 3 → 20·40·100; de 2 → 40·100; sem evolução → 100.

## Drops raros (Outland 1 → ×8 na Outland 8)
| Item | Chance/kill (Outland 1) |
|---|---|
| Bronze Boss Token | 0,05% (~2.000 kills) |
| Fragmento de Chave / Bike / Shiny Stone | 0,0005% (~200.000 kills) |
| Fragmento de Ovo Shiny (Unova+) | 0,00375% (nv 5.000) → 0,0081% (nv 160.300) |

Outlands: nv 150·500·1.000·2.000·4.000·8.000·16.000·25.000 → bônus ×1·1,25·1,5·2·3·4·6·8 ([[Combate]]).

## Bosses
- Entrada: 1 Bronze Boss Token; treinador ≥ nível do boss.
- Penalidade de equipe: `3^máx(0, 5 − Σ mín(1, nívelPkm/nívelEquipeBoss))` — leve **5** pokémon no nível do boss.
- Drops por vitória: peça TM 0,5–6,5%; Mega 0,5–6,5%; Mega Shiny metade; Safari Ticket = Mega Shiny; Mystic Ticket 0,0005–0,0065% ([[Bosses]]).

## PvP e competição
- Ranqueado: nv 150, equipe 1–5, perder = 70% do que a vitória pagaria; reset sábado 23h59; Mestre/Challenger por vaga (21º–50º / top 20) ([[PvP Ranqueado]]).
- Guerra de Guilds: 22h UTC; nota = 60/√(posição de queda) + 40/√(posição de abates); time de 10 ([[Guilds]]).
- Ginásio: 18 tipos, ≤5 pokémon do tipo, sem espécie repetida, nv 150+, espera 24 h; líder +25% na hunt ([[Ginásios]]).
- Mundial (nv 300) / Amador (nv 100) / Showdown (nv 100, quarta 21h) — eliminação dupla ([[Campeonatos]], [[Showdown]]).

## Economia
| Item | Valor |
|---|---|
| Venda pokémon ao NPC | `base × (1 + nível/50) × qualidade × (shiny ? 10 : 1)` (potência não entra) |
| Comissão Mercado (Ouro/item/diamante em Gema) | 15% do vendedor |
| Pokémon em Gema | 13% (≤500) · 10% (≤5.000) · 7,5% (acima), por faixa |
| Pensão pokémon | 100.000 Coins/dia (1–30 dias) |
| Alto-falante | 10.000.000 Coins, espera 30 min |
| Enviar Coins | queima 15%, mín. 1.000 |
| Gema | compra US$ 0,01 · saque US$ 0,009 (mín. 1.000) |
| Anúncios abertos | até 20; retenção 2 min; sorteio de 3 s na liberação |

Detalhe completo em [[Todas as taxas]], [[Mercado da Comunidade]] e [[Loja de Diamantes]].

## Boosts (multiplicam entre si)
XP Boost ×1,5 · XP Boost Pokémon ×1,5 · VIP +50% · Boost da Guild +10% · ranking da guild +1…+10% · Twitch +15% (+2,5% por live extra) · Kick +15%/h · Atrasados ×10 · eventos ([[Níveis e XP]]).
