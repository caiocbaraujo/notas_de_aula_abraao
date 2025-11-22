<!-- 54d02cab-9556-44b8-9d10-fc7fde4bfc91 3be5b662-a69c-4ce9-a54b-ef30dbb6310e -->
# Planejamento: Relatório sobre Teste de Hipótese em Regressão Normal Linear Múltipla

## Estrutura do Documento (4 páginas)

### Página 1: Introdução e Modelo

- **Cabeçalho**: Título, autor, data
- **Seção 1.1 - Introdução**: Contexto da regressão linear múltipla e importância dos testes de hipótese
- **Seção 1.2 - Especificação do Modelo**: 
- Modelo: $Y_i = \beta_0 + \beta_1 X_{1i} + \cdots + \beta_p X_{pi} + \varepsilon_i$
- Notação: $Y_i$ variável aleatória, $X_{1i}, \ldots, X_{pi}$ variáveis fixas
- Forma matricial: $\mathbf{Y} = \mathbf{X}\boldsymbol{\beta} + \boldsymbol{\varepsilon}$
- **Seção 1.3 - Pressupostos**: Normalidade dos erros, homocedasticidade, independência, não-colinearidade

### Página 2: Fundamentação Teórica

- **Seção 2.1 - Estimadores de Mínimos Quadrados**: 
- $\hat{\boldsymbol{\beta}} = (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathbf{Y}$
- Propriedades: não-viesado, eficiente (Gauss-Markov)
- **Seção 2.2 - Distribuição dos Estimadores**:
- $\hat{\boldsymbol{\beta}} \sim N(\boldsymbol{\beta}, \sigma^2(\mathbf{X}^T\mathbf{X})^{-1})$
- Particionamento: $\boldsymbol{\beta} = (\beta_0, \boldsymbol{\beta}_1^T)^T$ onde $\boldsymbol{\beta}_1 = (\beta_1, \ldots, \beta_p)^T$
- **Seção 2.3 - Estimador da Variância**: 
- $\hat{\sigma}^2 = \frac{SSE}{n-p-1}$ onde $SSE = \|\mathbf{Y} - \mathbf{X}\hat{\boldsymbol{\beta}}\|^2$

### Página 3: Teste de Hipótese

- **Seção 3.1 - Hipótese Nula**: $H_0: \boldsymbol{\beta}_1 = \mathbf{0}_p$ (vetor de zeros)
- **Seção 3.2 - Estatística F**:
- $F = \frac{MSR}{MSE} = \frac{SSR/p}{SSE/(n-p-1)}$
- Sob $H_0$: $F \sim F_{p, n-p-1}$
- Interpretação: razão entre variância explicada e não explicada
- **Seção 3.3 - Estatística t para Componentes**:
- Teste individual: $t_j = \frac{\hat{\beta}_j}{SE(\hat{\beta}_j)} \sim t_{n-p-1}$ sob $H_0: \beta_j = 0$
- **Seção 3.4 - Região de Rejeição**: 
- Nível de significância $\alpha$
- Rejeita $H_0$ se $F > F_{p, n-p-1; \alpha}$

### Página 4: Aplicações e Conclusão

- **Seção 4.1 - Exemplo Numérico** (breve):
- Ilustração com modelo simples
- Interpretação dos resultados
- **Seção 4.2 - Relação com Análise de Variância (ANOVA)**:
- Tabela ANOVA
- Decomposição da soma de quadrados: $SST = SSR + SSE$
- **Seção 4.3 - Considerações Finais**:
- Importância do teste para seleção de variáveis
- Limitações e cuidados na interpretação
- Referências bibliográficas básicas

## Detalhes Técnicos

### Pacotes LaTeX Necessários:

- `\documentclass[12pt,a4paper]{article}`
- `\usepackage[utf8]{inputenc}`, `\usepackage[T1]{fontenc}`, `\usepackage[brazil]{babel}`
- `\usepackage{amsmath, amssymb, amsthm}`
- `\usepackage{geometry}` com margens apropriadas
- `\usepackage{hyperref}` para referências

### Notação Matemática:

- Vetores em negrito: $\boldsymbol{\beta}$, $\mathbf{Y}$, $\mathbf{X}$
- Matrizes: $\mathbf{X}^T\mathbf{X}$, $(\mathbf{X}^T\mathbf{X})^{-1}$
- Distribuições: $N(\cdot, \cdot)$, $F_{p, n-p-1}$, $t_{n-p-1}$
- Estatísticas: $\hat{\boldsymbol{\beta}}$, $\hat{\sigma}^2$, $F$, $t_j$

### Conteúdo para Preencher 4 Páginas:

- Equações numeradas e bem formatadas
- Teoremas e proposições quando apropriado
- Explicações detalhadas de cada conceito
- Exemplo numérico ou aplicação prática
- Tabela ANOVA formatada
- Referências bibliográficas

## Arquivo de Saída

- **Arquivo**: `relatório/report.tex`
- **Formato**: LaTeX completo e compilável
- **Idioma**: Português (Brasil)
- **Estilo**: Acadêmico, seguindo padrão dos outros documentos do projeto

### To-dos

- [ ] Configurar estrutura básica do documento LaTeX com preâmbulo, pacotes necessários e formatação
- [ ] Escrever Página 1: Introdução, especificação do modelo e pressupostos
- [ ] Escrever Página 2: Fundamentação teórica, estimadores e distribuições
- [ ] Escrever Página 3: Teste de hipótese H₀: β₁ = 0ₚ, estatísticas F e t
- [ ] Escrever Página 4: Aplicações, ANOVA e conclusão
- [ ] Revisar formatação, garantir 4 páginas completas e verificar consistência matemática