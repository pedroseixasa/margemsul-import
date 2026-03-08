# 🚗 MargemSul Import

Simulador web profissional para análise de rentabilidade na importação de carros elétricos usados da Alemanha para Portugal.

## 🎯 Sobre o Projeto

Aplicação single-page desenvolvida para facilitar a tomada de decisão em importações de veículos elétricos, calculando automaticamente todos os custos, impostos e margem de lucro esperada.

## ✨ Funcionalidades

- **Cálculo automático de IVA alemão** — Deduz automaticamente o IVA de 19% em compras empresariais
- **Análise de rentabilidade completa** — IRC, overhead, lucro bruto e líquido
- **Comparação de mercado PT** — Suporta até 3 referências do Standvirtual
- **Avisos inteligentes** — Alertas sobre elegibilidade para isenção de IVA PT
- **Status visual** — Sistema de cores indicando viabilidade do negócio
- **Responsive design** — Totalmente adaptável a mobile, tablet e desktop
- **Light/Dark mode** — Adaptação automática ao tema do sistema
- **Exportação PDF** — Gera relatório impresso para apresentação
- **Zero dependências** — Single HTML file, funciona offline

## 📋 Regras de Negócio

### Constantes Fixas

- IVA Alemão: 19%
- Overhead: 600€ (viagem + importação + legalização)
- ISV: 0€ (elétricos)
- IVA Portugal: 0€ (EV usados com +6.000 km e +6 meses)
- IRC: 21% sobre lucro bruto
- Km viagem default: 2.300 km

### Cálculos Automáticos

```
Preço líquido = Preço com IVA ÷ 1.19
IVA poupado = Preço com IVA − Preço líquido
Total investido = Preço líquido + 600€
Venda conservadora = mínimo(referências PT)
Venda realista = média(referências PT)
Lucro bruto = Venda realista − Total investido
IRC = 21% × Lucro bruto (se > 0)
Lucro líquido = Lucro bruto − IRC
Margem = (Lucro bruto ÷ Total investido) × 100
```

### Sistema de Avaliação

| Status | Critério |
|--------|----------|
| 🟢 **Excelente** | Lucro ≥ 4.000€ **e** margem ≥ 25% |
| 🟠 **Viável** | Lucro positivo mas abaixo do threshold |
| 🔴 **Não rentável** | Lucro negativo |

## 💻 Tecnologias

- HTML5
- CSS3 (Custom Properties, Grid, Flexbox)
- JavaScript Vanilla (ES6+)  
- Material Design inspired
- Responsive & Mobile-First

## 📊 Como Usar

1. Preencher dados do carro na Alemanha (preço, km, matrícula)
2. Adicionar 1-3 referências comparáveis do Standvirtual PT
3. Clicar em **Simular** para análise instantânea
4. Analisar rentabilidade, avisos e status
5. Exportar PDF para apresentação ao cliente

## 🎨 Design

Estilo minimalista inspirado em Google Material com foco em clareza e usabilidade:

- Tipografia: **Inter** / System UI
- Paleta: Tons neutros com acentos de cor estratégicos
- Componentes: Cards flutuantes, badges informativos, gradientes suaves
- Temas: Light/Dark mode automático via `prefers-color-scheme`
- Layout: Responsivo 2-col desktop → 1-col mobile
- Print: Otimizado para exportação PDF

---

**MargemSul Import** © 2026 — Ferramenta profissional para análise de importação de veículos elétricos
