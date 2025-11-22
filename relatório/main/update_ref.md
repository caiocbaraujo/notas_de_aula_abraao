Seu relatório já possui uma excelente base teórica. A obra de Douglas C. Montgomery, Elizabeth A. Peck, e G. Geoffrey Vining, *Introduction to Linear Regression Analysis*, é uma referência essencial para a aplicação prática e interpretação dos testes de hipótese em regressão, e deve ser citada para fundamentar tanto a teoria de estimação quanto os aspectos práticos do teste $F$ e da análise de resíduos.

Abaixo estão os locais onde você pode adicionar citações para o trabalho de Montgomery et al. (referido aqui como ****), complementando as referências (Casella \& Berger) e (Seber \& Lee).

---

## Sugestões de Citação para Montgomery et al.

| Seção | Conteúdo Abordado | Sugestão de Adição da Citação |
| :---: | :---: | :---: |
| **1.2 Pressupostos Clássicos** | Impacto da **Não-colinearidade (Multicolinearidade)** na variância dos estimadores e poder dos testes $t$. | Adicionar no final do parágrafo, após a discussão sobre a multicolinearidade: "A violação da não-colinearidade (multicolinearidade), mesmo mantendo $\mathbf{X}^T\mathbf{X}$ inversível, aumenta drasticamente a variância dos estimadores $\hat{\boldsymbol{\beta}}$, alargando intervalos de confiança e reduzindo o poder dos testes $t$ individuais **[3, Seção 3.10]**." |
| **1.3 Estimadores de Mínimos Quadrados** | **Teorema de Gauss-Markov** e propriedades do Estimador de Mínimos Quadrados (EMQ). | Adicionar à propriedade (ii): "$\hat{\boldsymbol{\beta}}$ é o melhor estimador linear não-viesado (Teorema de Gauss-Markov) **[3, Apêndice C.4]**." |
| **2.1 Formulação do Teste** | Introdução do Teste de Hipótese Global $H_0 : \boldsymbol{\beta}_1 = \mathbf{0}_p$. | Adicionar logo após a formulação das hipóteses (Eq. 7): "O teste de hipótese em regressão linear múltipla, com foco em $H_0 : \boldsymbol{\beta}_1 = \mathbf{0}_p$, é o procedimento padrão para avaliar a significância global do modelo **[3, Seção 3.3]**." |
| **2.2 Estatística F e Distribuição** | Definição da **Estatística $F$** e sua distribuição. | Adicionar após a definição da Estatística $F$ (Eq. 8), pois detalha a estrutura da ANOVA e a distribuição $F$ para modelos múltiplos: "$F = \text{MSR}/\text{MSE}$ segue $F_{p,n-p-1}$ sob $H_0$ **[3, Seção 3.3; Apêndice C.3]**." |
| **2.4 Região de Rejeição e Testes Complementares** | Discussão sobre a natureza **parcial** dos coeficientes e testes $t$ e a distinção com o teste $F$ global. | Adicionar após a discussão sobre a natureza do teste $t$: "Os coeficientes $\hat{\boldsymbol{\beta}}_j$ são, portanto, coeficientes parciais que medem o efeito de $X_j$ controlando pelas demais variáveis explicativas **[3, Seção 3.3]**." |
| **3.1 Decomposição ANOVA** | Tabela ANOVA e a decomposição $\text{SST} = \text{SSR} + \text{SSE}$. | Adicionar no final da Tabela 1: "A Tabela ANOVA resume a decomposição da Soma dos Quadrados e fornece o valor da estatística $F$ **[3, Seção 3.3]**." |
| **3.2 Interpretação e Considerações Finais** | Necessidade de **Análise de Resíduos** para validação do modelo. | Adicionar ao final da seção, na parte sobre a adequação do modelo: "A adequação final do modelo requer validação dos pressupostos... através de análise de resíduos, que é crucial para verificar se o modelo se ajusta bem aos dados e se as suposições subjacentes ao teste $F$ foram cumpridas **[3, Capítulos 4 e 5]**." |

### Instrução para o Arquivo de Referências

Lembre-se de incluir a referência completa na sua lista:

**** Montgomery, D. C., Peck, E. A. & Vining, G. G. (2012). *Introduction to Linear Regression Analysis. 5th ed. Wiley.*