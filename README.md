# Caption Lab

Ferramenta de referência para criar tipografia animada de legendas de Reels
(título de abertura + legendas simples com palavras em destaque), no mesmo
estilo visual das referências: paleta preto/vermelho, legenda em destaque
tipo *bold condensed* e animação de palavras aparecendo uma a uma.

Site estático, um arquivo só (`index.html`), sem build step — abre direto no
navegador ou publica em qualquer host estático (Vercel, GitHub Pages, etc).

## Como usar

1. Abra `index.html` no navegador (Chrome/Edge recomendado por causa da
   gravação de vídeo via `MediaRecorder`).
2. **Roteiro**: cada linha vira um bloco. A primeira linha é o **título**
   (abertura mais trabalhada); as demais viram **legendas simples**.
   - Use `|` dentro de uma linha para forçar quebra manual (bom pro título).
   - Marque uma palavra com `*palavra*` para ela sair sempre em vermelho.
3. **Criatividade**: controla o quanto as palavras variam (rotação, escala,
   destaque automático, mistura de fontes). Use "Nova variação" para gerar
   outra combinação aleatória mantendo o mesmo nível.
4. **Fontes**: escolha 1 fonte, uma mistura de 2, ou modo colagem (estilo
   "recorte de jornal", com rotação por palavra). 10 fontes disponíveis,
   incluindo uma serifada (Playfair Display) e duas script (Yellowtail,
   Caveat).
5. **Cores & fundo**: cor de destaque 1 e 2 (8 tons — vermelhos, amarelo,
   ciano, rosa, laranja, verde, branco), glow, tema de fundo (vermelho,
   azul-marinho, preto, claro) e textura (grão ou pontilhado).
6. **Estilos prontos**: 4 presets estilo CapCut que configuram cores, fontes,
   destaque e animação de uma vez — *Sticker Pop* (chip + círculo + bounce),
   *Halftone Punch* (texto pontilhado + sublinhado + shake), *Editorial
   Serif* (fundo claro, serifa itálica, chip + seta) e *Gradient 3D*
   (texto em gradiente com extrusão + flip 3D). Não mexem no seu roteiro.
7. **Destaque (hook style)**: aplica um tratamento a só as palavras marcadas
   ou a todas — fundo (nenhum / chip / contorno / fita), preenchimento do
   texto (sólido / gradiente / halftone / contorno), rabisco desenhado à mão
   (sublinhado / círculo / seta) e extrusão 3D (profundidade 0–10).
8. **Animação**: 8 estilos de entrada (pop, slide, typewriter, bounce
   elástico, shake, glitch, blur focus, flip 3D) + modo aleatório por bloco,
   e velocidade.
9. **Som de entrada**: toca um clique sintetizado (tick / pop / snap) a cada
   palavra que aparece, com volume ajustável. É gerado por Web Audio, sem
   nenhum arquivo de áudio externo.
10. **Espaçamento**: letter-spacing, altura de linha, espaço entre palavras,
    margem lateral.
11. **Biblioteca de elementos**: clique para adicionar micrographics (faísca,
    anel, seta, mira, linha, pontilhado, scanlines, eco do título) ao palco.
    Arraste para posicionar; ajuste rotação ou remova na lista à direita.
12. **Exportar**:
   - `Gravar clipe (WebM)` grava a animação inteira do palco (1080×1920).
     Vídeo sai com fundo sólido — os navegadores não gravam canvas com
     alpha de forma confiável. Para usar como overlay no seu editor,
     coloque a camada em modo de mesclagem **Tela (Screen)** ou
     **Clarear (Lighten)**: o preto some e sobra só a tipografia.
   - `Baixar frame (PNG)` tira uma foto do frame atual — com a opção de
     fundo transparente marcada, sai uma PNG limpa pra usar como capa/título.
   - `Baixar preset (JSON)` / `Carregar preset` salvam e recarregam toda a
     configuração (fontes, cores, criatividade, destaque, som, elementos,
     espaçamento), pra você guardar "looks" prontos e reusar em vídeos
     futuros. O som escolhido também entra no clipe WebM gravado.

## Limitações conhecidas

- Vídeo exportado não tem canal alfa (limitação de navegador) — use blend
  mode no editor, como descrito acima.
- `letter-spacing` no canvas depende de suporte do navegador (funciona bem
  em Chrome/Edge recentes).
- O painel "Destaque" aplica um único conjunto de fundo/preenchimento/rabisco
  a todas as palavras marcadas do roteiro inteiro (não dá pra ter um estilo
  diferente por bloco ainda).
