# SheyQuant Research Lab

## Project 01 — Goal-Based Portfolio Construction

**Versión:** Research Brief V1  
**Área:** Quantitative Finance · Portfolio Management · Risk Management  
**Mercado:** Estados Unidos  
**Horizonte:** 30 años

---

## 1. Contexto

Un inversionista de largo plazo no necesariamente busca maximizar su rentabilidad. Su verdadero objetivo puede ser acumular suficiente patrimonio para financiar una obligación futura, como la jubilación.

Este proyecto estudiará cómo construir y evaluar cuantitativamente un portafolio orientado a una meta financiera concreta.

Se utilizará un enfoque **Goal-Based Investing**, diferenciando entre:

- **Performance-Seeking Portfolio (PSP):** activos cuyo objetivo principal es generar crecimiento.
- **Liability-Hedging Portfolio (LHP):** activos cuyo objetivo es reducir el riesgo asociado al cumplimiento de la obligación futura.

El objetivo no será encontrar simplemente el portafolio con mayor retorno, sino estudiar la relación entre **crecimiento, riesgo y probabilidad de alcanzar una meta financiera real**.

---

# 2. Investor Persona

Se define el siguiente inversionista ficticio:

| Variable | Supuesto inicial |
|---|---:|
| Edad inicial | 32 años |
| Edad objetivo | 62 años |
| Horizonte | 30 años |
| Capital inicial | USD 75,000 |
| Aportes adicionales | USD 0 |
| Perfil de riesgo | Moderado-agresivo |
| Mercado principal | Estados Unidos |
| Moneda | USD |
| Objetivo | Financiar USD 5,000 mensuales durante la jubilación |

El inversionista dispone actualmente de USD 75,000 y no realizará nuevas contribuciones durante los próximos 30 años.

Esto permitirá estudiar exclusivamente el efecto de:

**rentabilidad + riesgo + asignación de activos + interés compuesto + inflación + tiempo.**

---

# 3. Financial Goal

El inversionista desea disponer, a los 62 años, de un patrimonio capaz de financiar aproximadamente:

**USD 5,000 mensuales expresados en poder adquisitivo actual.**

Esto equivale actualmente a:

**USD 60,000 anuales.**

Sin embargo, USD 5,000 dentro de 30 años no tendrán el mismo poder adquisitivo que USD 5,000 hoy.

Por lo tanto, la obligación futura deberá ajustarse por inflación.

Si:

- \(C_0\) = consumo anual deseado actualmente;
- \(\pi\) = inflación anual;
- \(T\) = horizonte de inversión,

entonces:

\[
C_T=C_0(1+\pi)^T
\]

donde:

\[
C_0=60,000
\]

y:

\[
T=30
\]

La inflación será inicialmente estudiada utilizando datos históricos estadounidenses antes de seleccionar el supuesto de largo plazo utilizado en las simulaciones.

---

# 4. Retirement Liability

Existe una distinción fundamental entre:

**Ingreso anual necesario al comenzar la jubilación**

y

**capital total necesario para financiar la jubilación.**

No asumiremos automáticamente que alcanzar una cantidad arbitraria —por ejemplo, USD 1 millón— significa que la meta está financiada.

El capital requerido dependerá, entre otros factores, de:

- inflación;
- duración de la jubilación;
- rentabilidad durante la fase de retiro;
- riesgo de mercado;
- secuencia de retornos;
- política de retiros.

Como supuesto inicial, se estudiará una jubilación desde los **62 hasta los 92 años**, equivalente a aproximadamente **30 años de retiros**.

Posteriormente calcularemos el valor presente, a la fecha de jubilación, de los flujos de consumo esperados.

Este valor representará nuestra **retirement liability**.

---

# 5. Research Question

### Pregunta principal

> **¿Puede un portafolio cuantitativamente construido a partir de USD 75,000, sin contribuciones adicionales durante 30 años, alcanzar con una probabilidad razonable el capital necesario para financiar USD 5,000 mensuales en poder adquisitivo actual durante la jubilación?**

### Pregunta secundaria

> **¿Puede una estrategia que combine un Performance-Seeking Portfolio (PSP) y un Liability-Hedging Portfolio (LHP) mejorar la probabilidad de alcanzar el objetivo frente a una estrategia tradicional de inversión?**

---

# 6. Research Hypotheses

## H1 — Growth Hypothesis

Una mayor exposición a activos de crecimiento incrementará el patrimonio esperado al final del horizonte.

Sin embargo, también aumentará:

- volatilidad;
- drawdowns;
- tail risk;
- incertidumbre respecto al patrimonio final.

---

## H2 — Liability Hedging Hypothesis

La incorporación de un LHP reducirá determinados riesgos asociados al cumplimiento de la obligación futura, especialmente aquellos relacionados con:

- inflación;
- tasas de interés;
- preservación de capital;
- proximidad temporal de la obligación.

---

## H3 — Goal Probability Hypothesis

El portafolio con mayor retorno esperado **no necesariamente será el portafolio con mayor probabilidad de cumplir la meta financiera**.

Esta será una de las hipótesis centrales del proyecto.

---

## H4 — Dynamic Allocation Hypothesis

Una asignación PSP/LHP que evolucione conforme se aproxima la fecha de jubilación podría producir una mejor relación entre crecimiento y seguridad de la meta que mantener una asignación estática durante los 30 años.

---

# 7. Portfolio Architecture

El portafolio se dividirá conceptualmente en dos componentes.

## Performance-Seeking Portfolio — PSP

Su función será generar crecimiento real de largo plazo.

El universo inicial podrá incluir exposiciones representativas de:

- renta variable estadounidense;
- renta variable internacional;
- small caps;
- factores de riesgo;
- otros activos diversificadores cuando exista justificación cuantitativa.

La selección definitiva de instrumentos se realizará posteriormente.

---

## Liability-Hedging Portfolio — LHP

Su función será reducir la sensibilidad del objetivo financiero frente a determinados riesgos.

Podrá incluir exposiciones representativas de:

- bonos del Tesoro estadounidense;
- Treasury Inflation-Protected Securities (TIPS);
- bonos de distintas duraciones;
- instrumentos de corta duración.

La composición definitiva dependerá del análisis de la liability.

---

# 8. Benchmark

No evaluaremos una estrategia de manera aislada.

La estrategia Goal-Based deberá compararse contra benchmarks.

Como candidatos iniciales se estudiarán:

- portafolio 60/40;
- exposición pasiva a renta variable estadounidense;
- asignación estática PSP/LHP.

El benchmark definitivo será documentado antes del backtest.

---

# 9. Data

El proyecto utilizará principalmente datos financieros estadounidenses.

Las posibles fuentes incluirán datos de:

- precios históricos;
- índices bursátiles;
- Treasury yields;
- inflación estadounidense;
- tasas libres de riesgo;
- activos representativos de las distintas clases utilizadas.

Se priorizarán fuentes reproducibles y suficientemente largas para analizar diferentes regímenes económicos.

---

# 10. Return Metrics

Evaluaremos como mínimo:

### Total Return

Rentabilidad acumulada del portafolio.

### CAGR

\[
CAGR =
\left(\frac{V_T}{V_0}\right)^{1/T}-1
\]

Permitirá comparar crecimiento anualizado.

### Real Return

\[
1+r_{real}=
\frac{1+r_{nominal}}{1+\pi}
\]

Esta métrica será especialmente importante porque nuestro objetivo está definido en términos de **poder adquisitivo**.

---

# 11. Risk Metrics

El análisis incluirá:

### Volatilidad anualizada

Medirá la dispersión de los retornos.

### Sharpe Ratio

Permitirá analizar retorno excedente por unidad de riesgo.

### Semideviation

Medirá específicamente las desviaciones negativas.

### Historical VaR

Estimará pérdidas asociadas a determinados niveles de confianza.

### CVaR / Expected Shortfall

Analizará la magnitud media de las pérdidas cuando se supera el VaR.

### Maximum Drawdown

Medirá la mayor caída histórica desde un máximo hasta un mínimo posterior.

---

# 12. Goal-Based Metrics

Estas métricas serán incluso más importantes que algunas métricas tradicionales.

## Funding Ratio

\[
Funding\ Ratio_t=
\frac{Assets_t}{Liability_t}
\]

Interpretación:

**> 1:** objetivo financiado según los supuestos del modelo.

**= 1:** activos aproximadamente iguales a la obligación estimada.

**< 1:** déficit de financiación.

---

## Probability of Goal Success

Mediante simulaciones estimaremos:

\[
P(W_T \geq L_T)
\]

donde:

- \(W_T\) = patrimonio al alcanzar la jubilación;
- \(L_T\) = capital requerido para financiar la obligación.

Esta será una de las principales métricas del proyecto.

---

## Expected Shortfall Relative to Goal

Cuando el inversionista no alcance la meta, no queremos saber solamente **cuántas veces falla**.

También queremos saber:

> ¿Por cuánto falla?

Por ello estudiaremos la distribución del déficit respecto a la meta.

---

# 13. Portfolio Optimization

El proyecto explorará progresivamente diferentes enfoques.

### Portfolio A — Growth Benchmark

Alta exposición a activos de crecimiento.

### Portfolio B — Traditional Benchmark

Portafolio diversificado tradicional.

### Portfolio C — Static PSP/LHP

Asignación fija entre crecimiento y cobertura de obligaciones.

### Portfolio D — Dynamic PSP/LHP

Asignación que cambia conforme evoluciona:

- horizonte restante;
- funding ratio;
- riesgo;
- proximidad al objetivo.

El objetivo no será simplemente maximizar Sharpe Ratio.

Buscaremos mejorar la **probabilidad de financiar la meta**.

---

# 14. Simulation

Los resultados históricos por sí solos no son suficientes.

Utilizaremos simulaciones para estudiar diferentes trayectorias futuras.

Una simulación conceptual tendrá la forma:

\[
W_{t+1}=W_t(1+r_{t+1})
\]

repetida a través del horizonte de inversión.

Generaremos múltiples trayectorias posibles y observaremos la distribución del patrimonio final.

Esto permitirá estimar:

- probabilidad de éxito;
- probabilidad de déficit;
- patrimonio mediano;
- percentiles;
- downside outcomes;
- funding ratio.

---

# 15. Stress Testing

La estrategia será evaluada bajo escenarios adversos.

Entre otros:

### Equity Crash

Caída significativa del mercado bursátil.

### Inflation Shock

Inflación persistentemente superior al supuesto base.

### Interest Rate Shock

Cambios importantes en tasas que afecten los activos de renta fija.

### Lost Decade

Período prolongado de retornos reales bajos.

### Pre-Retirement Crash

Caída significativa del portafolio pocos años antes de comenzar la jubilación.

Este último escenario será especialmente importante debido al reducido tiempo disponible para recuperar pérdidas.

---

# 16. Success Criteria

Una estrategia no será considerada superior únicamente porque produzca mayor CAGR.

Evaluaremos conjuntamente:

1. Probability of Goal Success.
2. Funding Ratio.
3. Expected Goal Shortfall.
4. Real Return.
5. Maximum Drawdown.
6. CVaR.
7. Volatilidad.
8. Sharpe Ratio.
9. Robustez frente a diferentes escenarios.

La prioridad será:

> **cumplir la meta con un nivel de riesgo razonable.**

---

# 17. What We Are NOT Trying to Prove

Este estudio no pretende:

- predecir exactamente los retornos futuros;
- encontrar un portafolio perfecto;
- demostrar que una estrategia siempre supera al mercado;
- recomendar inversiones concretas a una persona;
- garantizar que el objetivo financiero será alcanzado.

El proyecto busca estudiar cuantitativamente cómo diferentes decisiones de construcción de portafolio afectan la probabilidad de financiar una obligación futura.

---

# 18. Research Workflow

El proyecto seguirá la siguiente secuencia:

**Research Question**

↓

**Financial Goal**

↓

**Liability Modeling**

↓

**Data Collection**

↓

**Exploratory Analysis**

↓

**Risk Analysis**

↓

**Portfolio Construction**

↓

**PSP/LHP Allocation**

↓

**Backtesting**

↓

**Monte Carlo / Scenario Simulation**

↓

**Stress Testing**

↓

**Goal Probability Analysis**

↓

**Interpretation**

↓

**Research Conclusions**

---

# 19. Planned Notebook Structure

```text
01_goal_based_portfolio/

├── research_brief.md
│
├── notebooks/
│   ├── 01_liability_model.ipynb
│   ├── 02_data_collection.ipynb
│   ├── 03_return_analysis.ipynb
│   ├── 04_risk_analysis.ipynb
│   ├── 05_portfolio_construction.ipynb
│   ├── 06_psp_lhp.ipynb
│   ├── 07_backtesting.ipynb
│   ├── 08_simulation.ipynb
│   ├── 09_stress_testing.ipynb
│   └── 10_results.ipynb
│
├── data/
├── figures/
└── README.md
```

---

# 20. Expected Final Deliverable

El resultado final deberá permitir responder de manera clara:

> **¿Son USD 75,000 suficientes hoy para financiar este objetivo dentro de 30 años sin realizar nuevas contribuciones?**

Si la respuesta es no, cuantificaremos el déficit.

Posteriormente responderemos:

> **¿Qué combinación entre crecimiento y liability hedging produce la mejor probabilidad de alcanzar la meta bajo nuestros supuestos?**

Finalmente estudiaremos:

> **¿Qué ocurre con esa conclusión cuando cambian inflación, retornos, volatilidad, horizonte o condiciones de mercado?**

El resultado será un estudio cuantitativo reproducible y documentado que pueda incorporarse al portafolio profesional de **SheyQuant Research Lab**.
