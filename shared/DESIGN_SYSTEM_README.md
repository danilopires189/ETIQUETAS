# Design System - Pague Menos Sistema de Etiquetas

## 📋 Visão Geral

Este design system fornece uma base consistente e moderna para todas as aplicações do sistema de etiquetas Pague Menos. Ele inclui tokens de design, componentes reutilizáveis, layouts responsivos e otimizações de acessibilidade e performance.

## 🎨 Arquitetura

```
shared/
├── design-tokens.css      # Variáveis CSS (cores, tipografia, espaçamento, etc.)
├── components.css         # Componentes reutilizáveis (botões, cards, forms, etc.)
├── layouts.css           # Sistema de grid e layouts responsivos
├── panel-layout.css      # Layout padrão dos painéis (baseado no módulo caixa)
├── accessibility.css     # Otimizações de acessibilidade e performance
├── design-system.css     # Estilos legados (manter compatibilidade)
├── performance.css       # Otimizações de performance legadas
├── visual-tests.html     # Página de testes de validação visual
└── test-components.html  # Página de teste de componentes
```

## 🚀 Como Usar

### 1. Importar os Arquivos CSS

Adicione os seguintes links no `<head>` de suas páginas HTML, **nesta ordem**:

```html
<link rel="stylesheet" href="../shared/design-tokens.css">
<link rel="stylesheet" href="../shared/components.css">
<link rel="stylesheet" href="../shared/layouts.css">
<link rel="stylesheet" href="../shared/panel-layout.css">
<link rel="stylesheet" href="../shared/accessibility.css">
<link rel="stylesheet" href="../shared/design-system.css">
<link rel="stylesheet" href="styles.css"> <!-- Seus estilos específicos -->
```

### 2. Usar Variáveis CSS

Todas as variáveis estão disponíveis através de `var(--nome-da-variavel)`:

```css
.meu-elemento {
  color: var(--brand-primary);
  padding: var(--space-4);
  border-radius: var(--radius-lg);
  font-size: var(--text-base);
}
```

## 🎨 Design Tokens

### Cores

#### Cores da Marca
- `--brand-primary`: #062e6f (Azul Pague Menos)
- `--brand-secondary`: #e0002b (Vermelho)
- `--brand-accent`: #0ea5e9 (Azul claro)

#### Escala Neutra
- `--neutral-50` até `--neutral-950` (11 variações)

#### Cores Funcionais
- Success: `--success-50` até `--success-900`
- Warning: `--warning-50` até `--warning-900`
- Error: `--error-50` até `--error-900`
- Info: `--info-50` até `--info-900`

#### Gradientes
- `--gradient-primary`: Gradiente azul principal
- `--gradient-secondary`: Gradiente vermelho
- `--gradient-glass`: Efeito glassmorphism
- `--gradient-hero`: Gradiente para hero sections
- `--gradient-subtle`: Gradiente sutil
- `--gradient-shine`: Efeito de brilho

### Tipografia

#### Tamanhos de Fonte
- `--text-2xs` (10px) até `--text-7xl` (72px)
- Tamanhos fluidos: `--text-fluid-xs` até `--text-fluid-5xl`

#### Pesos de Fonte
- `--font-thin` (100) até `--font-black` (900)

#### Alturas de Linha
- `--leading-none` (1) até `--leading-loose` (2)

#### Espaçamento de Letras
- `--tracking-tighter` até `--tracking-widest`

### Espaçamento

Sistema de espaçamento de 0 a 32 (0px a 128px):
- `--space-0`, `--space-px`, `--space-0-5`, `--space-1`, etc.

### Border Radius

- `--radius-none` até `--radius-3xl`
- `--radius-full` (9999px para círculos)

### Sombras

#### Sombras Neutras
- `--shadow-xs` até `--shadow-2xl`
- `--shadow-inner`

#### Sombras Coloridas
- `--shadow-primary`, `--shadow-accent`, `--shadow-success`, `--shadow-error`

### Transições

- `--transition-fast` (150ms)
- `--transition-base` (200ms)
- `--transition-slow` (300ms)
- `--transition-slower` (500ms)

#### Easing Functions
- `--ease-linear`, `--ease-in`, `--ease-out`, `--ease-in-out`
- `--ease-bounce`, `--ease-elastic`

## 🧩 Componentes

### Botões

```html
<!-- Variantes -->
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-accent">Accent</button>
<button class="btn btn-outline">Outline</button>
<button class="btn btn-ghost">Ghost</button>

<!-- Tamanhos -->
<button class="btn btn-sm">Small</button>
<button class="btn">Normal</button>
<button class="btn btn-lg">Large</button>

<!-- Estados -->
<button class="btn" disabled>Disabled</button>
```

### Formulários

```html
<div class="form-field">
  <label class="form-label">Nome</label>
  <input type="text" class="form-input" placeholder="Digite seu nome">
  <span class="form-helper">Texto de ajuda</span>
</div>

<!-- Select -->
<select class="form-select">
  <option>Opção 1</option>
  <option>Opção 2</option>
</select>

<!-- Textarea -->
<textarea class="form-textarea"></textarea>

<!-- Estados de validação -->
<input class="form-input is-valid">
<input class="form-input is-invalid">
```

### Cards

```html
<div class="card">
  <div class="card-header">
    <h3 class="card-title">Título do Card</h3>
  </div>
  <div class="card-body">
    Conteúdo do card
  </div>
  <div class="card-footer">
    <button class="btn btn-primary">Ação</button>
  </div>
</div>
```

### Header Moderno

```html
<header class="app-header">
  <div class="header-container">
    <div class="header-brand">
      <img src="logo.png" alt="Logo" class="brand-logo">
      <h1 class="header-title">Título</h1>
    </div>
    <div class="header-actions">
      <button class="btn btn-ghost">Ação</button>
    </div>
  </div>
</header>
```

### Logos Padronizados

```html
<!-- Tamanhos -->
<img src="logo.png" class="brand-logo brand-logo--sm">
<img src="logo.png" class="brand-logo brand-logo--md">
<img src="logo.png" class="brand-logo brand-logo--lg">
<img src="logo.png" class="brand-logo brand-logo--xl">

<!-- Grupo de logos -->
<div class="logo-group">
  <img src="pm.png" class="brand-logo">
  <img src="danilo.png" class="brand-logo">
</div>
```

## 📐 Layouts

### Grid Responsivo

```html
<!-- Grid automático -->
<div class="responsive-grid">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>

<!-- Grids fixos -->
<div class="grid-2">...</div>  <!-- 2 colunas -->
<div class="grid-3">...</div>  <!-- 3 colunas -->
<div class="grid-4">...</div>  <!-- 4 colunas -->

<!-- Grid com auto-fit -->
<div class="grid-auto">...</div>
```

### Containers

```html
<div class="container">Conteúdo centralizado</div>
<div class="container container-sm">Container pequeno</div>
<div class="container container-lg">Container grande</div>
```

### Flexbox Utilities

```html
<div class="flex">...</div>
<div class="flex-col">...</div>
<div class="flex-center">...</div>
<div class="flex-between">...</div>
<div class="gap-4">...</div>
```

### Panel Controls (Layout Padrão - Baseado no Módulo Caixa)

```html
<section class="panel controls">
  <!-- Campo simples -->
  <div class="field">
    <label for="campo1">
      Campo 1
      <span class="tooltip" data-tooltip="Texto de ajuda">ℹ️</span>
    </label>
    <input id="campo1" type="text" placeholder="Digite...">
    <div class="field-validation" id="campo1-validation"></div>
    <div class="field-info" id="campo1-info"></div>
  </div>
  
  <!-- Campo com inputs lado a lado -->
  <div class="field">
    <label>Largura × Altura (mm)</label>
    <div class="row">
      <input type="number" placeholder="Largura">
      <input type="number" placeholder="Altura">
    </div>
  </div>
  
  <!-- Campo com checkbox/switch -->
  <div class="field">
    <label>Opções</label>
    <div class="row wrap">
      <label class="switch">
        <input type="checkbox" checked>
        <span>Exibir logo</span>
      </label>
      <span class="hint">Opacidade (%)</span>
      <input type="number" min="0" max="100" value="100">
    </div>
  </div>
  
  <!-- Campo que ocupa toda a largura -->
  <div class="field full">
    <div class="generation-controls">
      <button class="btn btn-primary">Gerar</button>
      <div class="generation-info">
        <span>0 etiquetas</span>
      </div>
    </div>
    <div class="progress-container" style="display: none;">
      <div class="progress-bar">
        <div class="progress-fill"></div>
      </div>
      <span class="progress-text">Gerando...</span>
    </div>
  </div>
</section>
```

#### Estrutura do Header Padrão

```html
<header class="app-header">
  <div class="brand">
    <div class="brand-logos">
      <img src="../assets/pm.png" alt="Pague Menos" class="brand-logo primary">
      <img src="../assets/logo.png" alt="Danilo" class="brand-logo secondary">
    </div>
    <div class="brand-text">
      <h1>Pague Menos</h1>
      <span class="app-subtitle">Etiquetas • Módulo</span>
    </div>
  </div>
  <div class="actions">
    <button class="btn btn-ghost" onclick="window.location.href='../index.html'">
      <svg>...</svg>
      Hub
    </button>
    <button class="btn btn-ghost" onclick="window.print()">
      <svg>...</svg>
      Imprimir
    </button>
  </div>
</header>
```

#### Estrutura do Footer Padrão

```html
<footer class="app-footer">
  <div class="container">
    <div class="footer-content">
      <div class="footer-info">
        <p class="footer-title">Sistema de Etiquetas Pague Menos</p>
        <p class="footer-subtitle">Desenvolvido por Danilo Pires</p>
      </div>
      <div class="footer-links">
        <a href="https://wa.me/5562981020272" target="_blank" class="footer-link">
          <svg>...</svg>
          Suporte
        </a>
      </div>
    </div>
  </div>
</footer>
```

#### Modal Padrão

```html
<div class="modal" style="display: none;">
  <div class="modal-content">
    <div class="modal-header">
      <h3>Título do Modal</h3>
      <button class="modal-close">×</button>
    </div>
    <div class="modal-body">
      Conteúdo do modal
    </div>
    <div class="modal-footer">
      <button class="btn btn-ghost">Cancelar</button>
      <button class="btn btn-primary">Confirmar</button>
    </div>
  </div>
</div>
```

## ♿ Acessibilidade

### Contraste de Cores

Todas as combinações de cores atendem ao padrão WCAG 2.1 AA:
- Texto normal: mínimo 4.5:1
- Texto grande: mínimo 3:1

### Navegação por Teclado

Todos os elementos interativos são acessíveis via teclado:
- Tab: navegar entre elementos
- Enter/Space: ativar botões
- Escape: fechar modais

### Indicadores de Foco

Todos os elementos focáveis têm indicadores visuais claros:
```css
*:focus-visible {
  outline: 3px solid var(--brand-accent);
  outline-offset: 2px;
}
```

### Redução de Movimento

O sistema respeita a preferência `prefers-reduced-motion`:
```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

### Touch Targets

Todos os elementos interativos têm tamanho mínimo de 44x44px em dispositivos móveis.

### Screen Readers

Use classes utilitárias para conteúdo apenas para screen readers:
```html
<span class="sr-only">Texto apenas para leitores de tela</span>
```

## 📱 Responsividade

### Breakpoints

- Mobile: < 768px
- Tablet: 768px - 1023px
- Desktop: ≥ 1024px
- Large Desktop: ≥ 1440px

### Classes de Visibilidade

```html
<!-- Esconder em diferentes tamanhos -->
<div class="hide-mobile">Escondido em mobile</div>
<div class="hide-tablet">Escondido em tablet</div>
<div class="hide-desktop">Escondido em desktop</div>

<!-- Mostrar apenas em tamanhos específicos -->
<div class="show-mobile">Apenas mobile</div>
<div class="show-tablet">Apenas tablet</div>
<div class="show-desktop">Apenas desktop</div>
```

### Media Queries

```css
/* Mobile first */
.elemento {
  /* Estilos mobile */
}

@media (min-width: 768px) {
  .elemento {
    /* Estilos tablet */
  }
}

@media (min-width: 1024px) {
  .elemento {
    /* Estilos desktop */
  }
}
```

## 🚀 Performance

### GPU Acceleration

Animações usam propriedades GPU-accelerated:
- `transform`
- `opacity`
- `filter`

### Lazy Loading

```html
<img src="image.jpg" loading="lazy" alt="Descrição">
```

### Contenção de Layout

Componentes principais usam `contain` para melhor performance:
```css
.card {
  contain: layout style paint;
}
```

## 🧪 Testes

### Validação Visual

Abra `shared/visual-tests.html` no navegador para validar:
- Paleta de cores
- Contraste WCAG
- Breakpoints responsivos
- Touch targets
- Navegação por teclado
- Tipografia
- Componentes
- Animações

### Teste de Componentes

Abra `shared/test-components.html` para ver todos os componentes em ação.

## 📝 Boas Práticas

### 1. Use Variáveis CSS

❌ Evite:
```css
.elemento {
  color: #062e6f;
  padding: 16px;
}
```

✅ Prefira:
```css
.elemento {
  color: var(--brand-primary);
  padding: var(--space-4);
}
```

### 2. Mobile First

❌ Evite:
```css
.elemento {
  width: 1200px;
}

@media (max-width: 768px) {
  .elemento {
    width: 100%;
  }
}
```

✅ Prefira:
```css
.elemento {
  width: 100%;
}

@media (min-width: 768px) {
  .elemento {
    width: 1200px;
  }
}
```

### 3. Use Classes Utilitárias

❌ Evite criar classes customizadas para layouts simples:
```css
.meu-flex-container {
  display: flex;
  align-items: center;
  gap: 16px;
}
```

✅ Use classes utilitárias:
```html
<div class="flex items-center gap-4">...</div>
```

### 4. Acessibilidade Primeiro

Sempre inclua:
- Labels em inputs
- Alt text em imagens
- ARIA labels quando necessário
- Indicadores de foco visíveis

### 5. Performance

- Use `will-change` com moderação
- Prefira `transform` e `opacity` para animações
- Implemente lazy loading em imagens
- Minimize reflows e repaints

## 🔄 Atualizações

Para atualizar o design system:

1. Modifique os arquivos em `shared/`
2. Teste em `visual-tests.html`
3. Verifique compatibilidade em todas as aplicações
4. Documente mudanças neste README

## 📞 Suporte

Para dúvidas ou sugestões sobre o design system:
- Desenvolvedor: Danilo Pires
- WhatsApp: (62) 98102-0272

## 📄 Licença

© 2024 Pague Menos - Sistema de Etiquetas
