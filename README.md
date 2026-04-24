# PriceOps — Simulador de Pricing Estratégico

> Simule preços, analise margens, calcule break-even e explore cenários de desconto — tudo em tempo real, direto no navegador, sem planilhas.

---

## Sobre o projeto

O **PriceOps** é uma ferramenta de precificação estratégica construída inteiramente em HTML, CSS e JavaScript puro. Nasceu da necessidade de ter uma calculadora de preços rápida, visual e sem dependências — sem instalar nada, sem cadastro, sem backend.

O projeto evoluiu de um simulador simples para uma aplicação com landing page própria e simulador em modo tela cheia, com três módulos analíticos integrados.

---

## Funcionalidades

###  Módulo Pricing
- Cálculo do preço ideal a partir do CMV e custo fixo rateado
- Configuração de impostos sobre venda, comissão de vendas e margem de lucro desejada
- Visualização da composição do preço em barras proporcionais (CMV, fixo, impostos, comissão, lucro)
- Simulação de desconto máximo com cálculo da margem real resultante
- Indicador visual de status: meta atingida, abaixo da meta ou prejuízo

###  Módulo Cenários
- Comparação simultânea de 6 níveis de desconto (0% a 25%)
- Tabela com preço, margem, receita e lucro total por cenário
- Gráfico de barras com receita e lucro por volume de vendas
- Destaque automático dos cenários dentro e fora da meta de margem

###  Módulo Break-even
- Cálculo do ponto de equilíbrio em unidades e em faturamento
- Margem de contribuição por unidade
- Gráfico de linha com cruzamento entre receita total e custos totais
- Base configurável de custo fixo mensal

---

## Tecnologias

- **HTML5** — estrutura e semântica
- **CSS3** — layout, variáveis, animações e responsividade
- **JavaScript (vanilla)** — lógica de cálculo e interatividade
- **Chart.js 4.4** — gráficos de barra e linha
- **Google Fonts** — tipografia (DM Serif Display, DM Mono, Outfit)

---

## Como usar

**Opção 1 — Direto no navegador**

Faça o download ou clone o repositório e abra o arquivo `pricing_simulator.html` no navegador:

```bash
git clone https://github.com/GZimbra/Simulador_Pricing_HTML.git
cd Simulador_Pricing_HTML
# Abra o arquivo pricing_simulator.html no seu navegador
```

**Opção 2 — GitHub Pages**

Acesse diretamente pelo link publicado:

```
https://gzimbra.github.io/Simulador_Pricing_HTML/pricing_simulator.html
```

---

## Estrutura do projeto

```
Simulador_Pricing_HTML/
│
├── pricing_simulator.html   # Landing page + simulador completo
└── README.md
```

---

## Fórmulas utilizadas

| Conceito | Fórmula |
|---|---|
| Preço de venda | `(CMV + Fixo) ÷ (1 − Margem − Impostos − Comissão)` |
| Preço com desconto | `Preço × (1 − Desconto%)` |
| Margem real | `Lucro líquido ÷ Preço com desconto × 100` |
| Margem de contribuição | `Preço − CMV − Impostos − Comissão` |
| Break-even (un.) | `Custo fixo mensal ÷ Margem de contribuição` |

---

## Capturas de tela

### Landing Page
Interface de apresentação com resumo dos módulos e acesso ao simulador.

### Simulador — Módulo Pricing
Entrada de custos, sliders de margem e visualização da composição do preço.

### Simulador — Módulo Cenários
Tabela comparativa de descontos com gráfico de receita × lucro.

### Simulador — Módulo Break-even
Gráfico de cruzamento com ponto de equilíbrio e métricas de contribuição.

---

## Melhorias planejadas

- [ ] Exportação dos resultados em PDF ou CSV
- [ ] Histórico de simulações salvo localmente (localStorage)
- [ ] Modo comparação de múltiplos produtos
- [ ] Suporte a múltiplas alíquotas (Simples Nacional, Lucro Presumido)
- [ ] Internacionalização (EN / ES)

---

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

## Autor

Desenvolvido por **GZimbra**  
[github.com/GZimbra](https://github.com/GZimbra)

GZimbra

---
