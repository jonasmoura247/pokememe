---
tipo: wiki
capitulo: O básico
fonte: pokemon.txt (Wiki PokeIdle)
---

# Nota, Poder e Calculadora

São **duas métricas diferentes** que o jogo mostra na ficha — e confundir as duas é a origem de quase todo mal-entendido sobre “pokémon bom”.

### Nota N= (0–10) — alinhada ao ⚔@100

Mede o quão forte o pokémon **nasceu dentro da espécie**. Usa a **mesma força (score)** do ranking ⚔, como se todo mundo estivesse no **nível 100** — subir de nível não muda a nota, só o ⚔ que aparece no placar.

```
score = força de nascimento (0–1), mesma base do ⚔ nota = 10 × (score − pior possível) ÷ (melhor − pior) ← só dentro da espécie
```

- **0** = pior nascimento possível *daquela* espécie; **10** = P5 + shiny + IV máximo.
- **Evoluir sempre SOBE a nota** — nunca derruba e nunca empata. Cada espécie tem a sua régua, e a forma nova mede o mesmo nascimento de outro jeito; por isso a nota depois de evoluir é, no mínimo, a da forma anterior **+0,1** por evolução (o piso da linhagem). Megaevoluir segue a mesma regra. O único limite é o teto: 10 continua sendo 10.
- Refino (+N) **sobe** a nota e o ⚔ — usa a base atual (espécie + refino).

> O Mercado da Comunidade exige faixa mínima de nota na calculadora. **Shiny, P5 e lendário entram** mesmo abaixo da faixa.

### A Calculadora na prática

Abra pelo quadradinho da **calculadora**, na coluna do seu retrato, ou pela ficha de um pokémon (aí ela já vem com os números dele). São duas abas.

**Calcular Pokémon.** Escolha a **espécie primeiro** — 0 e 10 são o pior e o melhor nascimento *daquela* espécie — e preencha o nascimento: o **IV de cada stat** (seis campos, de 1 a 32), a qualidade, a potência, o shiny e, se quiser, o TM elemental. Sai:

- a **nota** grande, no pedestal com o holofote na **cor da faixa** (tabela abaixo), e quanto falta para a faixa seguinte;
- **De onde vem a nota**: quanto cada eixo (IV, qualidade, potência, shiny) pesa na força total — não são 25% fixos, e um P5 brilhante puxa mais que um comum fraco;
- **Peso de cada stat na nota**: qual stat a espécie mais valoriza. Dois bichos com a mesma soma de IV podem ter notas diferentes se os pontos caírem em stats diferentes;
- **Em combate**: o multiplicador de stats, o HP de combate, o **Poder (ranking)** — o ⚔ no nível da ficha — e o **Poder (ginásio)**;
- **Potencial na evolução final** e **Potencial na Mega Evolução**: a nota N= que o mesmo nascimento teria nas formas finais alcançáveis (Eevee e ramificações inclusive) e na Mega, avisando se cada uma atinge a faixa do Mercado.

> **Lendário e Mítico não têm nota.** Eles são **×4 em todos os stats** (ver Potência), e esse ×4 passa do topo da régua de 0 a 10. Com um deles escolhido, a calculadora "quebra" — aparece **INESTIMÁVEL** no lugar do número. O cartão **Em combate** continua valendo, já com o ×4.

**Comparar Pokémons.** Monte dois lados (espécie, nível e nascimento) e a calculadora simula um **duelo 1×1 de desgaste**, com a tabela de tipos, o STAB e o melhor golpe de cada um contra o outro. Sai quem vence e em que fração dos duelos simulados — a faixa varia com a sorte do dano, e por isso dois pokémon parecidos raramente dão 0% ou 100%.

A cor da caixa sobe um degrau a cada ponto de nota — são dez faixas. Uma nota bem no limite fica na faixa de baixo.

| Nota | Faixa | Cor |
| --- | --- | --- |
| 0–1 | **Extremamente Fraco** | cinza |
| 1–2 | **Fraco** | vermelho |
| 2–3 | **Mediano** | laranja |
| 3–4 | **Razoável** | verde |
| 4–5 | **Bom** | verde-claro |
| 5–6 | **Forte** | verde vibrante, brilho pulsando |
| 6–7 | **Poderoso** | lilás, brilho leve |
| 7–8 | **Mítico** | roxo reluzente, moldura pulsando |
| 8–9 | **Lendário** | rosa-claro, com brilho |
| 9–10 | **Divino** | rosa reluzente, moldura pulsando |

### Poder (⚔) — ranking “Pokémon Forte”

É um **número único** no placar e na ficha. **Não é a nota** e **não muda combate** — só ordena quem aparece no ranking. Sobe com nível, refino e evolução.

```
score = mesma força da nota (0–1) poder = arred( nível × 10 × score ) → no nv 100: ⚔ ≈ 1000 × score
```

No **combate**, qualidade ainda entra como expoente em cada stat; potência, shiny e o ×4 do lendário ainda multiplicam os stats. O ⚔ do ranking é outra conta — e também leva o ×4, que a nota não leva.

### O que muda no combate

- **HP de combate** = máx(24, arred(hp × 12)). Selvagem leva ×5 por cima.
- **Dano** usa ATK ou Sp.Atk vs DEF ou Sp.Def reais, tipo, STAB e efetividade — não usa o número “poder” diretamente.
- O **Speed base** com o **IV de SPD** encurta a recarga dos golpes (até 7%), e o IV ainda tira −0,01 s a −0,32 s da Investida — nada disso acelera a corrida na hunt.
- **Defesa** reduz o dano recebido na fórmula clássica; mais DEF/Sp.Def = aguenta mais hits.

### A ficha do seu pokémon

Clicar num pokémon seu abre a ficha. O que ela mostra, de cima para baixo:

- o pokémon num **pedestal com holofote** na cor da faixa da nota — o shiny ganha um halo dourado que brilha;
- embaixo do pedestal, a **placa da nota** — num lendário ou mítico ela vem "quebrada": **INESTIMÁVEL** no lugar do número e a faixa **GLITCH**, porque o ×4 dele passa do topo da régua;
- o **apelido** da Name Tag, quando tem, com a espécie logo abaixo — e a **skin** que ele estiver vestindo;
- a fileira **Potência · Qualidade · IV** e, lado a lado, o **Poder no PvE** — a força de luta na caça — e o **Poder no PvP**, com o nível comprimido acima do Nv 150 como no ginásio e no PvP ranqueado ("conta como Nv X"), mais o **HP de combate**;
- os selos **P · IV · Q · N**, que do azul para cima viram metal — o dourado de P5 se lê de relance numa grade cheia;
- **quem capturou** o pokémon — o nome fica mesmo depois que ele troca de dono, e é link para o perfil de quem capturou;
- a **Medalha de Guerra** (Guilds) e o **Troféu** de campeonato (Campeonatos), que também vão junto numa venda;
- a **evolução** e a **Mega** da espécie como link para a Pokédex — numa forma final que tem Mega, a ficha mostra a Mega Evolução no lugar do "não evolui". Enquanto o pokémon não chega ao nível, a seta diz **Precisa de Nv X/N**; o N é só o mínimo, e evoluir mantém o nível dele;
- o botão **Copiar p/ ChatGPT**: copia a ficha em texto — espécie, stats-base, IV de cada stat, potência, qualidade, shiny e como o jogo calcula — para colar no ChatGPT.
