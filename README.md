# MargemSul Import - Simulador de Importação EV

Aplicação web responsiva para simular importação de carros elétricos da Alemanha para Portugal.

## 📱 Características

- ✅ 100% responsivo (mobile-first)
- ✅ Light/Dark mode automático
- ✅ Cálculo automático de IVA alemão poupado
- ✅ Análise de rentabilidade com IRC
- ✅ Avisos coloridos sobre elegibilidade
- ✅ Exportação para PDF
- ✅ Single HTML file (sem dependências)

## 🚀 Como Hospedar

### Opção 1: GitHub Pages (Grátis)

1. Criar repositório no GitHub
2. Fazer upload do ficheiro `index.html`
3. Ir a Settings → Pages
4. Escolher branch main
5. Site disponível em: `https://seu-usuario.github.io/repo-name`

### Opção 2: Netlify (Grátis)

1. Aceder a [netlify.com](https://www.netlify.com/)
2. Arrastar a pasta MargemSulImport para o Netlify Drop
3. Site publicado instantaneamente com URL personalizada

### Opção 3: Vercel (Grátis)

1. Aceder a [vercel.com](https://vercel.com/)
2. Importar projeto ou arrastar pasta
3. Deploy automático com domínio vercel.app

### Opção 4: Cloudflare Pages (Grátis)

1. Aceder a [pages.cloudflare.com](https://pages.cloudflare.com/)
2. Fazer upload do ficheiro
3. Deploy instantâneo

## 📋 Regras de Negócio Implementadas

### Constantes Fixas

- IVA Alemão: 19%
- Overhead: 600€ (viagem + importação + legalização)
- ISV: 0€ (elétricos)
- IVA Portugal: 0€ (EV usados com +6.000 km e +6 meses)
- IRC: 21% sobre lucro bruto
- Km viagem default: 2.300 km

### Cálculos Automáticos

- Preço líquido = Preço com IVA ÷ 1.19
- IVA poupado = Preço com IVA - Preço líquido
- Total investido = Preço líquido + 600€
- Venda conservadora = Mínimo das referências PT
- Venda realista = Média das referências PT
- Lucro bruto = Venda realista - Total investido
- IRC = 21% × Lucro bruto (se positivo)
- Lucro líquido = Lucro bruto - IRC
- Margem = Lucro bruto ÷ Total investido × 100

### Status Global

- 🟢 Verde: Lucro ≥ 4.000€ E margem ≥ 25%
- 🟠 Laranja: Lucro positivo mas abaixo do threshold
- 🔴 Vermelho: Lucro negativo

## 💡 Como Usar

1. Preencher dados do carro na Alemanha
2. Adicionar 1-3 referências do Standvirtual
3. Clicar em "Simular"
4. Analisar resultados e avisos
5. Gerar PDF se necessário

## 🎨 Design

- Fonte: Inter / System UI
- Cores neutras e profissionais
- Estilo inspirado em Google Material com cartões minimalistas e badges informativos
- Gradientes suaves e sombras flutuantes para sensação premium
- Adaptação automática ao tema do sistema
- Layout 2 colunas (desktop) / 1 coluna (mobile)
- Otimizado para impressão

## 📄 Licença

Desenvolvido para MargemSul Import © 2026
