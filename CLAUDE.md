# Fábrica do Caos — Guia do Projeto

## Conceito Central
Jogo de sobrevivência em ondas infinitas, estilo **Cuphead / desenho animado anos 30** (rubber hose animation).
O personagem principal é o **Jorbe Guarna** — garrafão verde com rosto humano real (óculos, barba).

## Regra de Ouro: Tudo deve fazer sentido com o Jorbe
**Todo elemento do jogo deve ter coerência temática com o universo de garrafas/bebidas.**

| Elemento | Deve ser... |
|---|---|
| Balas | Tampinhas de garrafa verdes com "B" |
| Inimigos | Garrafas de refrigerante (Coca-Cola e futuros rivais) |
| Sons de tiro | "Pop" de tampinha saindo da garrafa |
| Sons de acerto | Líquido borbulhando, gás escapando |
| Sons de morte | Vidro quebrando + "blub" líquido |
| Música | Jazz/ragtime anos 30, estilo propaganda vintage |
| Cenário | Fábrica de bebidas art déco, anos 30, cartoon |
| Poderes futuros | Relacionados a bebidas (jato de líquido, espuma, gás CO2) |
| Pontuação | "Garrafas destruídas", não "inimigos mortos" |

## Personagem Principal — Jorbe Guarna
- Corpo: garrafão verde com silhueta de garrafa contour
- Tampa verde escura no topo como chapéu
- Rosto humano visível: óculos redondos, bigode/barba, pele morena
- Luvas brancas cartoon (rubber hose)
- Tênis vermelhos grandes
- Escrito "BRASIL" no peito em dourado
- Atira tampinhas verdes giratórias

## Inimigos
- **Mini Cola** (scale 0.60): rápida, pouca vida, vem em grupo
- **Cola Normal** (scale 1.00): balanceada
- **MEGA COLA** (scale 1.60): lenta, enorme HP, aparece a partir da onda 5
- Futuro: garrafas de outras marcas como chefes de fase

## Mecânica de Combate
- 3 andares na fábrica (↑/W ↓/S para trocar)
- ESPAÇO: atirar tampinhas (segurar para automático)
- Cada andar mira uma zona diferente da garrafa:
  - Andar 3 → Cabeça (tampinha)
  - Andar 2 → Barriga (rótulo)
  - Andar 1 → Pernas/base
- 🔴 Zona VERMELHA pulsando = ponto fraco → dano crítico
- 🔵 Zona AZUL = escudo → quase sem dano
- Ponto fraco de cada garrafa muda a cada poucos segundos

## Ondas
- Ondas infinitas e progressivas
- Cada onda: mais garrafas, mais HP, velocidade levemente maior
- 5 vidas (♥) — perde 1 quando garrafa chega na fábrica
- Objetivo: sobreviver o máximo de ondas possível

## Estética Visual
- **Estilo**: Cuphead, Fleischer Studios, rubber hose anos 30
- **Contornos**: grossos, pretos (INK = #1A0A00)
- **Paleta**: verde (Jorbe), vermelho/marrom (Coca-Cola), âmbar/creme (fábrica), preto
- **Cenário**: silhueta de cidade art déco, chaminés, estrelas cartoon
- **Efeitos**: grain de película, vinheta, film noir
- Personagens com membros elásticos (bezier curves), olhos grandes

## Sons e Música (Web Audio API)
- **Música de fundo**: ragtime/jazz loop anos 30 (osciladores)
- **Tiro**: pop curto (square wave descendente)
- **Acerto normal**: thud percussivo
- **Crítico**: borbulha de líquido (sweep + noise)
- **Garrafa destruída**: crash de vidro (noise burst highpass)
- **Fábrica atingida**: sino de alarme (sawtooth duplo)
- **Nova onda**: fanfarra curta (3 notas ascendentes)
- **Game over**: melodia descendente triste

## Arquivos
- `index.html` — jogo completo (HTML + CSS + JS inline)
- `CLAUDE.md` — este arquivo
- `.claude/launch.json` — config do servidor de preview
