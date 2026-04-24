# Canvas Scenes - JavaScript Implementation

Este arquivo contém a implementação JavaScript das funções de canvas backgrounds para o projeto Empório São Vicente.

## Funções Disponíveis

### drawHeroScene(canvas)
- **Descrição**: Bar escuro com garrafas na prateleira, balcão de madeira, bokeh quente
- **Background**: Gradiente escuro #0A0614 → #110820 → #05030A
- **Elementos**: 10 garrafas com reflexos, prateleira de madeira, espelho, bokeh lights, motas de poeira

### drawStatementScene(canvas)
- **Descrição**: Copo de whisky tumbler com líquido âmbar, macro fotográfico
- **Background**: Gradiente radial concentrado com tons âmbar
- **Elementos**: Copo principal + 2 copos secundários desfocados, cubos de gelo, brilho na superfície

### drawComboScene(canvas)
- **Descrição**: Celebração/festa, múltiplas garrafas, luzes coloridas
- **Background**: #07040F com 5 fontes de luz coloridas
- **Elementos**: 6 garrafas silhueta, 80 faíscas/confetes aleatórios

### drawProofScene(canvas)
- **Descrição**: Vista aérea de balcão de mármore com copos de bebidas
- **Background**: #08060F com superfície de mármore
- **Elementos**: 4 copos top-down (whisky, gin, vinho, mixer), veios de mármore, luz overhead

### drawClosingScene(canvas)
- **Descrição**: Bar noturno, atmosfera misteriosa, silhueta de garrafas
- **Background**: #040208 (mais escuro), atmosfera vermelha
- **Elementos**: 14 garrafas silhueta, traços de néon, 50 bokeh quentes

## Utilização Básica

```javascript
import { drawHeroScene, drawStatementScene } from './src/canvas';

// Em um componente React
const canvasRef = useRef(null);

useEffect(() => {
  const canvas = canvasRef.current;
  if (canvas) {
    // Define dimensões
    canvas.width = window.innerWidth * 1.2;
    canvas.height = window.innerHeight * 1.2;

    // Desenha a cena
    drawHeroScene(canvas);
  }
}, []);
```

## Funções Utilitárias

### setCanvasDimensions(canvas)
Define as dimensões do canvas (largura × altura × 1.2)

### handleCanvasResize(callback)
Gerencia redimensionamento com debounce de 300ms

### initAllScenes()
Inicializa todas as cenas (função principal)

## Integração com Next.js

Para usar em componentes React, importe dinamicamente:

```javascript
import { useEffect, useRef } from 'react';

export default function HeroCanvas() {
  const canvasRef = useRef(null);

  useEffect(() => {
    import('../src/canvas').then(({ drawHeroScene, setCanvasDimensions }) => {
      const canvas = canvasRef.current;
      if (canvas) {
        setCanvasDimensions(canvas);
        drawHeroScene(canvas);
      }
    });
  }, []);

  return <canvas ref={canvasRef} className="absolute inset-0" />;
}
```

## Performance

- Todas as funções são otimizadas para renderização procedural
- Gradientes e efeitos são calculados em tempo real
- Suporte a redimensionamento responsivo
- Compatível com dispositivos de alta densidade (DPR)