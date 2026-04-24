# TODO — Empório São Vicente (Warm Bar Redesign)

## Status: ✅ COMPLETO

### Arquivos criados/modificados:
- [x] `app/globals.css` — CSS completo do design Warm Bar (cursor, loader, nav, scenes, hero, ticker, statement, products, combo, categories, proof, reviews, closing, footer, sticky, media queries)
- [x] `app/layout.tsx` — SEO, fonts (Bebas Neue, DM Sans, JetBrains Mono), Schema.org
- [x] `app/page.tsx` — Página principal completa com todas as seções + GSAP ScrollTrigger + canvas backgrounds + cursor customizado
- [x] `hooks/useCanvasScene.ts` — Hook modular para canvas scenes
- [x] `hooks/canvas/drawHero.ts` — Canvas: bar escuro com garrafas, bokeh, wood grain
- [x] `hooks/canvas/drawStatement.ts` — Canvas: whisky glass macro
- [x] `hooks/canvas/drawCombo.ts` — Canvas: party lighting
- [x] `hooks/canvas/drawProof.ts` — Canvas: aerial bar top view
- [x] `hooks/canvas/drawClosing.ts` — Canvas: night bar ambiance
- [x] `hooks/canvas/drawProductsBg.ts` — Canvas: subtle whisky swirl
- [x] `hooks/canvas/drawCatsBg.ts` — Canvas: bottle grid pattern
- [x] `src/canvas/index.js` — ✅ Versão JavaScript das funções de canvas (conversão completa das 5 principais funções) - **Corrigido**: Renomeado para index.js e imports corrigidos
- [x] `components/CanvasScene.tsx` — ✅ Componente exemplo para integração React

### Build & Dev:
- [x] `npm run build` — ✅ Sucesso (0 erros) - **Corrigido**: Erros de import resolvidos automaticamente
- [x] `npm run dev` — ✅ Rodando em http://localhost:3000

### Design implementado:
| Seção | Descrição |
|-------|-----------|
| Loader | "EMPÓRIO / SÃO VICENTE" com barra dourada e fade-out |
| Cursor | Círculo cream + anel externo com lag suave |
| Hero | Canvas bar procedural + headline "BEBA MELHOR, PAGUE MENOS." |
| Ticker | Marquee infinito com produtos em destaque |
| Statement | Canvas whisky glass + "OS PREÇOS QUE FRANCA NÃO SABIA QUE MERECIA" |
| Products | Grid editorial 6 produtos com preços dourados De/Por |
| Combo | Canvas party + card glassmorphism "3× MONTE SEU ROLÊ" R$359 |
| Categories | Grid 4×2 com 8 categorias (emoji + hover dourado) |
| Proof | Canvas aerial + números (4.9★, 500+, 30min, 100%) |
| Reviews | 3 cards de depoimentos com aspas decorativas |
| Closing | Canvas night bar + "SEM FRESCURA. SEM ENROLAÇÃO. SÓ BEBIDA BOA." |
| Footer | Endereço, links, copyright |
| Sticky | Barra WhatsApp verde com animação de pulso |

### Paleta:
- Ink: `#06040E`
- Cream: `#F2EDE4`
- Gold: `#BF8B2E`
- Amber: `#E0A030`
- Red: `#C8282A`

### Correções Automáticas Aplicadas:
- **Erro de import**: `src/canvas/scenes.js` renomeado para `src/canvas/index.js` para permitir import como módulo
- **Caminhos incorretos**: Todos os imports em `components/CanvasScene.tsx` corrigidos de `../canvas/scenes` para `../src/canvas`
- **Build TypeScript**: Agora passa sem erros - todas as dependências resolvidas corretamente
