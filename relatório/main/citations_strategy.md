Analisando os arquivos de sugestões e comparando com o `report.tex` para identificar onde adicionar mais citações.


[3 tools called]


Comparando as sugestões com o `report.tex`, identifiquei onde adicionar mais citações:

## Análise de citações faltantes

### Citações já presentes
1. Linha 62: Montgomery sobre multicolinearidade
2. Linha 97: Casella & Berger sobre Teorema de Gauss-Markov
3. Linha 114: Seber & Lee sobre independência de $\hat{\beta}$ e $\hat{\sigma}^2$
4. Linha 156: Casella & Berger sobre LRT

### Citações recomendadas a adicionar

#### 1. Seção 1.3 - Teorema de Gauss-Markov (Linha 91)
- Local: propriedade (ii) do Teorema 1.1
- Sugestão: adicionar citação de Montgomery após mencionar o Teorema de Gauss-Markov
- Código sugerido:
```latex
\item[(ii)] $\hat{\beta}$ é o melhor estimador linear não-viesado (Teorema de Gauss-Markov) \citep[Apêndice C.4]{montgomery2012};
```

#### 2. Seção 1.4 - Teorema de Cochran (Linha 125)
- Local: após a declaração do Teorema de Cochran
- Sugestão: adicionar citação de Seber & Lee
- Código sugerido:
```latex
O Teorema de Cochran estabelece que sob condições adequadas, somas de quadrados podem ser decompostas em componentes qui-quadrado independentes, sendo fundamental para a análise de variância e inferência em modelos lineares \citep{seber2012}.
```

#### 3. Seção 2.1 - Formulação do Teste (Linha 138)
- Local: após a equação 135 (formulação das hipóteses)
- Sugestão: adicionar citação de Montgomery
- Código sugerido:
```latex
onde $\mathbf{0}_p$ é o vetor nulo de dimensão $p$. Sob $H_0$, o modelo reduz-se a $Y_i = \beta_0 + \varepsilon_i$. O teste de hipótese em regressão linear múltipla, com foco em $H_0: \beta_1 = \mathbf{0}_p$, é o procedimento padrão para avaliar a significância global do modelo \citep[Seção 3.3]{montgomery2012}.
```

#### 4. Seção 2.2 - Estatística F (Linha 154)
- Local: após o Teorema 2.1 (distribuição da estatística F)
- Sugestão: adicionar citação de Montgomery
- Código sugerido:
```latex
\end{teorema}

Sob $H_0: \beta_1 = \mathbf{0}_p$ e os pressupostos do modelo, a estatística $F$ segue uma distribuição $F_{p, n-p-1}$ \citep[Seção 3.3]{montgomery2012}.
```

#### 5. Seção 2.3 - Derivação via Decomposição (Linha 160)
- Local: após o parágrafo introdutório da seção
- Sugestão: adicionar citação de Seber & Lee sobre o método rigoroso
- Código sugerido:
```latex
A escolha da estatística $F$ para o teste $H_0: \beta_1 = \mathbf{0}_p$ decorre da estrutura distribucional do modelo normal linear. A derivação da estatística $F$ utilizando a decomposição de somas de quadrados em termos de matrizes de projeção ortogonal é o método mais rigoroso para provar sua distribuição exata sob $H_0$ \citep{seber2012}. Sob $H_0$, o modelo reduz-se a $Y_i = \beta_0 + \varepsilon_i$ com E.M.Q. $\hat{\beta}_0 = \bar{y}$.
```

#### 6. Seção 2.4 - Coeficientes Parciais (Linha 183)
- Local: após a discussão sobre coeficientes parciais
- Sugestão: adicionar citação de Montgomery
- Código sugerido:
```latex
Os coeficientes $\hat{\beta}_j$ são, portanto, \textbf{coeficientes parciais} que medem o efeito de $X_j$ controlando pelas demais variáveis explicativas \citep[Seção 3.3]{montgomery2012}. A multicolinearidade pode resultar em rejeição de $H_0$ pelo teste $F$ global enquanto os testes $t$ individuais falham em identificar variáveis significativas.
```

#### 7. Seção 3.1 - Decomposição ANOVA (Linha 191)
- Local: após a primeira frase sobre decomposição
- Sugestão: adicionar citação de Montgomery
- Código sugerido:
```latex
A decomposição fundamental da variabilidade total é $SST = SSR + SSE$, onde $SST = \sum_{i=1}^n (y_i - \bar{y})^2$ é a Soma Total dos Quadrados \citep[Seção 3.3]{montgomery2012}. A tabela ANOVA resume essa decomposição:
```

#### 8. Seção 3.2 - Análise de Resíduos (Linha 211)
- Local: no parágrafo final sobre adequação do modelo
- Sugestão: adicionar citação de Montgomery sobre análise de resíduos
- Código sugerido:
```latex
É importante ressaltar que rejeitar $H_0$ (significância) não implica que o modelo seja adequado para previsão ou descrição. A adequação final do modelo requer validação dos pressupostos (normalidade e homocedasticidade) através de \textbf{análise de resíduos}, que é crucial para verificar se o modelo se ajusta bem aos dados e se as suposições subjacentes ao teste $F$ foram cumpridas \citep[Capítulos 4 e 5]{montgomery2012}.
```

## Resumo das prioridades

Alta prioridade (conceitos centrais):
1. Teorema de Cochran (Seção 1.4) - Seber & Lee
2. Estatística F e distribuição (Seção 2.2) - Montgomery
3. Derivação via decomposição (Seção 2.3) - Seber & Lee

Média prioridade (fundamentação):
4. Formulação do teste (Seção 2.1) - Montgomery
5. Coeficientes parciais (Seção 2.4) - Montgomery
6. Análise de resíduos (Seção 3.2) - Montgomery

Baixa prioridade (reforço):
7. Teorema de Gauss-Markov (Seção 1.3) - Montgomery (já há Casella & Berger)
8. Decomposição ANOVA (Seção 3.1) - Montgomery

Essas citações reforçam o rigor teórico e mostram que os conceitos estão fundamentados nas referências.