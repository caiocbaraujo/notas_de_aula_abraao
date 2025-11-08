### 13/10/2025 — Revisão de Convergência Estocástica

- **Revisão**: James
- **Seção 3.7(a)**: Revisão de convergência estocástica

### 3.7(1a) Alguns resultados limites
- **(R1)**: \(\lim_{n\to\infty} n^{1/n} = 1\)
- **(R2)**: \(\lim_{n\to\infty} (1+1/n)^{n} = e\)
- **(R3)**: \(\lim_{n\to\infty} (1+x/n)^{n} = e^{x}\)

### Exemplo — Aproximação Binomial → Poisson
Seja \(X \sim \operatorname{Binomial}(n,p_n)\) com \(p_n = \lambda/n \in (0,1)\). Para \(k\in\{0,1,2,\\dots\}\):

\[\mathbb{P}(X=k) = \binom{n}{k} p_n^k (1-p_n)^{n-k}\]

Desenvolvendo:

\[\mathbb{P}(X=k) = \frac{n!}{(n-k)!\,k!} \left(\frac{\lambda}{n}\right)^k \left(1-\frac{\lambda}{n}\right)^{n-k}\]

Reescrevendo os fatores:

\[\mathbb{P}(X=k) = \frac{\lambda^k}{k!}\, \frac{n(n-1)\cdots(n-k+1)}{n^k}\, \left(1-\frac{\lambda}{n}\right)^{n}\,\left(1-\frac{\lambda}{n}\right)^{-k}\]

ou, em produto:

\[\mathbb{P}(X=k) = \frac{\lambda^k}{k!}\, \prod_{j=0}^{k-1}\left(1-\frac{j}{n}\right)\, \left(1-\frac{\lambda}{n}\right)^{n}\,\left(1-\frac{\lambda}{n}\right)^{-k}\]

Usando os limites acima quando \(n\to\infty\):

- \(\prod_{j=0}^{k-1}\left(1-\frac{j}{n}\right) \to 1\)
- \(\left(1-\frac{\lambda}{n}\right)^n \to e^{-\lambda}\)
- \(\left(1-\frac{\lambda}{n}\right)^{-k} \to 1\)

Logo,

\[\mathbb{P}(X=k) \to e^{-\lambda}\, \frac{\lambda^k}{k!}\quad \Rightarrow\quad X \xrightarrow{d} \operatorname{Poisson}(\lambda).\]
