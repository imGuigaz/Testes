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
   "recorte de jornal", com rotação e fundo tipo etiqueta por palavra).
5. **Paleta & estilo**: tom de vermelho de destaque, glow, fundo colagem.
6. **Animação**: estilo (pop / slide / typewriter) e velocidade.
7. **Espaçamento**: letter-spacing, altura de linha, espaço entre palavras,
   margem lateral.
8. **Biblioteca de elementos**: clique para adicionar micrographics (faísca,
   anel, seta, mira, linha, pontilhado, scanlines, eco do título) ao palco.
   Arraste para posicionar; ajuste rotação ou remova na lista à direita.
9. **Exportar**:
   - `Gravar clipe (WebM)` grava a animação inteira do palco (1080×1920).
     Vídeo sai com fundo sólido — os navegadores não gravam canvas com
     alpha de forma confiável. Para usar como overlay no seu editor,
     coloque a camada em modo de mesclagem **Tela (Screen)** ou
     **Clarear (Lighten)**: o preto some e sobra só a tipografia.
   - `Baixar frame (PNG)` tira uma foto do frame atual — com a opção de
     fundo transparente marcada, sai uma PNG limpa pra usar como capa/título.
   - `Baixar preset (JSON)` / `Carregar preset` salvam e recarregam toda a
     configuração (fontes, cores, criatividade, elementos, espaçamento),
     pra você guardar "looks" prontos e reusar em vídeos futuros.

## Limitações conhecidas

- Vídeo exportado não tem canal alfa (limitação de navegador) — use blend
  mode no editor, como descrito acima.
- `letter-spacing` no canvas depende de suporte do navegador (funciona bem
  em Chrome/Edge recentes).
