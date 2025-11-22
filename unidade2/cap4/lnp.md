O Lema de Neyman-Pearson (LNP) é o resultado fundamental na teoria de testes de hipóteses, pois estabelece a metodologia para a construção do **Teste Mais Poderoso (MP)**. Ele se aplica ao caso de **hipóteses simples versus simples** ($H_0: \theta = \theta_0$ vs $H_1: \theta = \theta_1$).

O LNP afirma que o teste mais poderoso de nível $\alpha$ é baseado na **razão de verossimilhanças** $\Lambda(x) = L(\theta_1; x) / L(\theta_0; x)$, rejeitando $H_0$ quando essa razão excede uma constante $k$.

---

# O Lema de Neyman-Pearson (LNP)

## 1. Estabelecendo a Desigualdade Fundamental

A demonstração da otimalidade do teste de Neyman-Pearson começa com a prova de uma desigualdade que deve ser satisfeita por **todos os pontos amostrais** $x$.

Seja $\Upsilon$ o teste proposto pelo LNP (o teste MP) e $\Upsilon^*$ qualquer outro teste de nível $\alpha$. Sejam $\psi_{\Upsilon}(x)$ e $\psi_{\Upsilon^*}(x)$ suas respectivas funções críticas (ou funções de teste).

### A Desigualdade Fundamental (Equação 4.3.3)

O primeiro e mais crucial passo da prova é verificar que, para todo $x$ no espaço amostral $\mathcal{X}^n$, a seguinte desigualdade é válida:

$$
\mathbf{[\psi_{\Upsilon}(x) - \psi_{\Upsilon^*}(x)] \cdot [L(\theta_1; x) - k \cdot L(\theta_0; x)] \geq 0} \quad \text{}
$$

### Por que essa Desigualdade é Importante?

Essa desigualdade é a **base lógica da prova** porque ela estabelece, ponto a ponto, uma **relação de otimalidade** entre a regra do teste proposto ($\psi_{\Upsilon}$) e a evidência fornecida pelos dados ($L(\theta_1; x) / L(\theta_0; x)$).

Para que o produto de dois fatores seja não-negativo ($\geq 0$), eles devem ter **sinais compatíveis** (ambos $\geq 0$ ou ambos $\leq 0$). O teste $\Upsilon$ é construído de forma que essa compatibilidade de sinais seja garantida:

| Condição para o Teste $\Upsilon$ | Fator 1: $\psi_{\Upsilon}(x) - \psi_{\Upsilon^*}(x)$ (Diferença dos testes) | Fator 2: $L(\theta_1; x) - k \cdot L(\theta_0; x)$ (Razão de Verossimilhanças) | Conclusão |
| :---: | :---: | :---: | :---: |
| **Rejeição Forte** $\psi_{\Upsilon}(x) = 1$ | $\mathbf{1 - \psi_{\Upsilon^*}(x) \geq 0}$ | $\mathbf{> 0}$ (Pois $L_1 > k L_0$) | Produto $\geq 0$ |
| **Não Rejeição Forte** $\psi_{\Upsilon}(x) = 0$ | $\mathbf{0 - \psi_{\Upsilon^*}(x) \leq 0}$ | $\mathbf{< 0}$ (Pois $L_1 < k L_0$) | Produto $\geq 0$ |
| **Caso Aleatorizado** $0 < \psi_{\Upsilon}(x) < 1$ | Indefinido | $\mathbf{= 0}$ (Pois $L_1 = k L_0$) | Produto $= 0$ |

Em todos os casos, a desigualdade fundamental (4.3.3) é satisfeita.

## 2. Da Desigualdade ao Poder

A importância da desigualdade fundamental se manifesta quando a integramos sobre todo o espaço amostral $\mathcal{X}^n$.

$$
\mathbf{0 \leq \int_{\mathcal{X}^n} [\psi_{\Upsilon}(x) - \psi_{\Upsilon^*}(x)] [L(\theta_1; x) - k \cdot L(\theta_0; x)] dx} \quad \text{}
$$

Ao expandir o produto e aplicar o Princípio da Esperança, onde a integral da função crítica $\psi(x)$ multiplicada pela verossimilhança $L(\theta; x)$ é a **Função Poder** $Q(\theta) = E_{\theta}[\psi(X)]$:

$$
0 \leq Q_{\Upsilon}(\theta_1) - Q_{\Upsilon^*}(\theta_1) - k [Q_{\Upsilon}(\theta_0) - Q_{\Upsilon^*}(\theta_0)] \quad \text{}
$$

Rearranjando os termos, obtemos:
$$
Q_{\Upsilon}(\theta_1) - Q_{\Upsilon^*}(\theta_1) \geq k [Q_{\Upsilon}(\theta_0) - Q_{\Upsilon^*}(\theta_0)] \quad \text{}
$$

O teste $\Upsilon$ é construído para ter tamanho **exato** $\alpha$, então $Q_{\Upsilon}(\theta_0) = \alpha$. O teste rival $\Upsilon^*$ tem nível $\alpha$, ou seja, $Q_{\Upsilon^*}(\theta_0) \leq \alpha$.

Isso implica que o termo entre colchetes é $\geq 0$:
$$
Q_{\Upsilon}(\theta_0) - Q_{\Upsilon^*}(\theta_0) = \alpha - Q_{\Upsilon^*}(\theta_0) \geq 0 \quad \text{}
$$

Como $k \geq 0$, o lado direito da desigualdade final é não-negativo, forçando a conclusão:

$$
Q_{\Upsilon}(\theta_1) - Q_{\Upsilon^*}(\theta_1) \geq 0 \implies \mathbf{Q_{\Upsilon}(\theta_1) \geq Q_{\Upsilon^*}(\theta_1)} \quad \text{}
$$

Isso prova que o poder do teste $\Upsilon$ (o teste MP) é maior ou igual ao poder de qualquer outro teste $\Upsilon^*$ de nível $\alpha$.

---

## 3. Exemplo Prático: Aplicação do LNP (Exercício 2.1)

O **Exercício 2.1** do *Caderno de Exercícios - Capítulo 4* demonstra a aplicação do LNP, mostrando como a razão de verossimilhanças se transforma diretamente na estatística de teste.

**Problema:**
Sejam $X_1, \dots, X_{10}$ uma amostra de $X \sim N(\theta, 4)$. Use o LNP para derivar o teste MP de nível $\alpha = 0.05$ para:
$$H_0 : \theta = 2 \quad \text{vs} \quad H_1 : \theta = 5$$

### Passo 1: Derivação da Razão de Verossimilhanças

O primeiro passo para aplicar o LNP é calcular a razão $\Lambda(x) = L(\theta_1; x) / L(\theta_0; x)$.

Para a Distribuição Normal, a verossimilhança é:
$$L(\theta; x) = (2\pi \sigma^2)^{-n/2} \exp \left\{ - \frac{1}{2\sigma^2} \sum_{i=1}^n (x_i - \theta)^2 \right\}$$

Substituindo $\sigma^2 = 4$ e $n=10$:
$$\frac{L_1}{L_0} = \exp \left\{ - \frac{1}{2(4)} \left[ \sum (x_i - 5)^2 - \sum (x_i - 2)^2 \right] \right\}$$

Após a simplificação (Passo 1 na solução do Exercício 2.1):
$$\frac{L_1}{L_0} = \exp \left\{ \frac{3}{4} \sum x_i - 26.25 \right\}$$

### Passo 2: Tradução da Desigualdade Fundamental

O LNP exige que a região crítica rejeite $H_0$ quando $L_1 / L_0 > k$. Essa condição é a tradução prática da **Desigualdade Fundamental** para a construção do teste MP.

Rejeitamos $H_0$ se:
$$\exp \left\{ \frac{3}{4} \sum x_i - 26.25 \right\} > k$$

Tomando o logaritmo em ambos os lados e isolando a estatística suficiente $T(x) = \sum x_i$:
$$\frac{3}{4} \sum x_i - 26.25 > \log k$$
$$\sum x_i > \frac{4}{3} (\log k + 26.25)$$

Como $4(\log k + 26.25)/3$ é apenas uma constante, chamamos essa condição de $\sum x_i > k_1$. Dividindo por $n=10$, o teste é equivalente a:
$$\bar{x} > c$$

**Interpretação:** A razão de verossimilhanças, que sustenta a Desigualdade Fundamental, demonstrou que o teste MP depende apenas da média amostral $\bar{x}$ e rejeita $H_0$ para valores **grandes** de $\bar{x}$.

### Passo 3: Determinação da Constante $k$ (ou $c$)

A constante $k$ (ou $c$) é determinada pela condição de que o teste tenha nível $\alpha = 0.05$:
$$P_{H_0} [\bar{X} > c] = \alpha = 0.05$$

Sob $H_0: \theta = 2$, a média amostral tem distribuição:
$$\bar{X} \sim N(\theta_0, \sigma^2/n) = N(2, 4/10) = N(2, 0.4)$$

Padronizando para o quantil $z_{0.05} = 1.645$:
$$c = \theta_0 + z_{0.05} \cdot \sigma_{\bar{X}} = 2 + 1.645 \cdot \sqrt{0.4}$$
$$c \approx 2 + 1.645 \cdot 0.632 \approx 3.04$$

**Teste Final (Teste MP):**
Rejeitamos $H_0$ se $\bar{x} > 3.04$. Pelo LNP, este é o teste Mais Poderoso entre todos os testes possíveis de nível 0.05 para distinguir $\theta=2$ de $\theta=5$.

A Desigualdade Fundamental é, portanto, a ferramenta teórica que permite transformar o princípio abstrato da maximização do poder em uma regra de decisão concreta e calculável ($\bar{x} > c$).