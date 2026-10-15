---
tipo: wiki
capitulo: O básico
fonte: pokemon.txt (Wiki PokeIdle)
---

# Níveis e XP

Há **dois níveis independentes**: o do **treinador** (você) e o do **pokémon ativo**. Cada derrota paga o mesmo XP para os dois, e cada um sobe na própria conta.

- O nível do **treinador** é o que **destranca as áreas** do Mapa.
- O nível do **pokémon** é o que faz os stats dele crescerem — e ele **cura por completo** a cada nível novo.

### O pokémon passa do treinador em até 5 níveis

Um pokémon só entra em campo se estiver no máximo **5 níveis acima** do seu treinador — o inicial é a exceção e sempre entra. Um Nv 60 pede treinador Nv 55. Com um bicho alto demais (comprado no Mercado, por exemplo), dá para esperar o treinador subir ou usar **Reduzir o nível**, na ficha do pokémon: você escolhe o nível novo — o piso é o **Nível ao capturar** da espécie —, o XP volta para o começo dele e não tem como desfazer.

### A curva

É cúbica, e não tem teto. Subir sempre custa mais que o nível anterior:

```
xpTotal(L) = arred( 50/3 × (L³ − 6L² + 17L − 12) )
```

| Nível | XP total | Só deste nível |
| --- | --- | --- |
| 10 | 9.300 | 2.900 |
| 25 | 204.800 | 25.400 |
| 50 | 1.847.300 | 112.900 |
| 100 | 15.694.800 | 475.400 |
| 200 | 129.389.800 | 1.950.400 |
| 300 | 441.084.800 | 4.425.400 |
| 500 | 2.058.474.800 | 12.375.400 |
| 1.000 | 16.566.949.800 | 49.750.400 |
| 5.000 | 2.080.834.749.800 | 1.248.750.400 |
| 10.000 | 16.656.669.499.800 | 4.997.500.400 |
| 25.000 | 260.354.173.749.800 | 31.243.750.400 |
| 50.000 | 2.083.083.347.499.800 | 124.987.500.400 |
| 100.000 | 16.665.666.694.999.802 | 499.975.000.400 |

> **Não existe nível máximo.** A curva só fica mais cara — Alola, a última aba do Mapa, abre no **nv 25.000** do treinador, e a hunt mais alta de hoje pede **nv 160.300**. Um pokémon nível 1000 já é caro; o topo do Mapa é meta de fim de jogo, não de primeira semana.

### O que multiplica o seu XP

- **XP Boost** — +50% no XP do TREINADOR.
- **XP Boost Pokémon** — +50% no XP do POKÉMON.
- **VIP** — +50% nos dois.
- **Boost da Guild** — +10% nos dois, para a guild INTEIRA: os membros enchem juntos o banco da guild. Ver Guilds.
- **Bônus do ranking da guild** — de +1% a +10% nos dois (e no loot), para os escalados, pela posição da guild no Guild Diário. Ver Guilds.
- **Bônus Twitch** — +15% nos dois enquanto você assiste a uma live oficial, e +2,5% por live a mais aberta junto.
- **Bônus na Kick** — +15% nos dois, por hora resgatada com pontos do canal. Os dois em Bônus de live.
- **Boost dos Atrasados** — ×10 nos dois, até o seu treinador chegar ao nível dos veteranos. Ver Boost dos Atrasados.
- **Eventos** — o buff de XP de um evento entra por cima de tudo isso.

Eles se **multiplicam**, não se somam: VIP + XP Boost dá **2,25×**, e não 2×. São compras separadas, e somar faria a segunda valer menos que a primeira justamente para quem gastou mais. Ver Loja de Diamantes.
