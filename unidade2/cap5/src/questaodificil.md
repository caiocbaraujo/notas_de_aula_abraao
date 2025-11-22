Esta é uma excelente requisição, pois ela nos leva ao cerne do estudo de testes ótimos e à complexidade dos testes bilaterais em distribuições não-Normais. O desafio reside em aplicar o conceito de **Teste Uniformemente Mais Poderoso (UMP) bilateral**, que geralmente não existe, exceto em casos especiais, como a distribuição Uniforme $U(0, \theta)$, que é um tópico avançado do material.

Abaixo, apresento uma questão mais difícil do que o Exercício 5.2, focada na determinação do tamanho amostral mínimo utilizando a função poder do **Teste UMP Bilateral para a Uniforme**.

---

### Questão Avançada sobre Função Poder e Amostra Mínima

Uma instituição de controle de qualidade investiga o tempo máximo ($\theta$) que um componente eletrônico pode durar em um ambiente extremo. O tempo de falha dos componentes é modelado por uma **distribuição Uniforme $U(0, \theta)$**, onde $\theta$ é o parâmetro de escala desconhecido.

O valor especificado para o tempo máximo é $\theta_0 = 800$ horas. O objetivo é testar se o tempo real difere desse valor, utilizando o **Teste UMP Bilateral** (Teorema 4.5.1).

Formule as hipóteses como:
$$H_0: \theta = 800 \quad \text{vs} \quad H_1: \theta \neq 800$$

Assuma que o nível de significância é fixado em **$\alpha = 0.01$**.

**Qual é o tamanho amostral mínimo ($n$)** necessário para garantir que o poder do teste ($Q(\theta)$) seja de, no mínimo, **$99\%$** quando o verdadeiro parâmetro for $\theta_1 = 1000$ horas?

*Dica:* A função poder do Teste UMP Bilateral para a Uniforme, quando $\theta > \theta_0$, é dada pela soma das probabilidades de rejeição nas duas caudas da estatística $T(X) = X_{(n)}$, o máximo da amostra.

#### Estrutura Teórica Relevante (Para Resolução)

Para responder a esta questão, é necessário utilizar o **Teorema 4.5.1**, que estabelece a região crítica ($Rc$) do teste UMP bilateral para $U(0, \theta)$ em função da estatística suficiente $T(X) = X_{(n)}$.

1.  **Região Crítica ($Rc$):** O teste rejeita $H_0$ se:
    $$Rc = \{x: T(x) > \theta_0\} \cup \{x: T(x) \le \theta_0 \alpha^{1/n}\}$$

2.  **Função Poder ($Q(\theta)$) para $\theta > \theta_0$:** O poder é a probabilidade de rejeitar $H_0$ quando $H_1$ é verdadeira (ou seja, quando o verdadeiro parâmetro é $\theta = \theta_1$).
    $$Q(\theta) = P_\theta [T(x) > \theta_0] + P_\theta [T(x) \le \theta_0 \alpha^{1/n}]$$

3.  **Cálculo das Probabilidades (utilizando a FDA de $X_{(n)}$):** A Função de Distribuição Acumulada (FDA) de $T(X)=X_{(n)}$ sob o verdadeiro parâmetro $\theta$ é $F_{X_{(n)}}(t; \theta) = (t/\theta)^n$ para $0 < t < \theta$.
    *   Primeiro termo:
        $$P_\theta [T(x) > \theta_0] = 1 - P_\theta [T(x) \le \theta_0] = 1 - \left(\frac{\theta_0}{\theta}\right)^n$$
    *   Segundo termo:
        $$P_\theta [T(x) \le \theta_0 \alpha^{1/n}] = F_{X_{(n)}}(\theta_0 \alpha^{1/n}; \theta) = \left(\frac{\theta_0 \alpha^{1/n}}{\theta}\right)^n = \left(\frac{\theta_0}{\theta}\right)^n \alpha$$

4.  **Função Poder Final:** Substituindo os termos:
    $$Q(\theta) = 1 - \left(\frac{\theta_0}{\theta}\right)^n + \alpha \left(\frac{\theta_0}{\theta}\right)^n$$

A questão se resume a resolver esta equação para o valor mínimo de $n$ que satisfaça a condição $Q(1000) \ge 0.99$.