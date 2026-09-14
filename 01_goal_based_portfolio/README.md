# SheyQuant Research Lab — Proyecto 01

## Goal-Based Portfolio Construction

Estado: Research Brief V1 documentado; implementación cuantitativa pendiente.

Estudio de un inversionista ficticio con USD 75,000 iniciales, sin aportes durante 30 años, que busca financiar USD 5,000 mensuales en poder adquisitivo actual desde los 62 hasta los 92 años. Se compararán estrategias de crecimiento y cobertura de obligaciones (PSP/LHP).

El [Research Brief V1](research_brief.md) contiene las 20 secciones del documento acordado y gobierna la investigación.

## Estructura y orden de trabajo

- `research_brief.md`: contexto, hipótesis, metodología y criterios de evaluación.
- `notebooks/`: diez notebooks numerados, inicialmente con objetivos y espacio para implementación.
- `data/`: documentación de fuentes y datos del proyecto.
- `figures/`: gráficos derivados de los análisis.

1. [01_liability_model.ipynb](notebooks/01_liability_model.ipynb)
2. [02_data_collection.ipynb](notebooks/02_data_collection.ipynb)
3. [03_return_analysis.ipynb](notebooks/03_return_analysis.ipynb)
4. [04_risk_analysis.ipynb](notebooks/04_risk_analysis.ipynb)
5. [05_portfolio_construction.ipynb](notebooks/05_portfolio_construction.ipynb)
6. [06_psp_lhp.ipynb](notebooks/06_psp_lhp.ipynb)
7. [07_backtesting.ipynb](notebooks/07_backtesting.ipynb)
8. [08_simulation.ipynb](notebooks/08_simulation.ipynb)
9. [09_stress_testing.ipynb](notebooks/09_stress_testing.ipynb)
10. [10_results.ipynb](notebooks/10_results.ipynb)

## Cómo comenzar

Abrir los notebooks en JupyterLab o VS Code con soporte para Jupyter y Python 3. Comenzar por el modelo de la obligación y avanzar en el orden indicado. Las plantillas todavía no contienen cálculos ni resultados; las dependencias se fijarán al implementar el primer análisis.

Antes de simular o hacer backtesting, documentar las fuentes, inflación, tasa de descuento, calendario de retiros, benchmark, universo, costos, rebalanceo y criterio numérico de éxito. Registrar semillas aleatorias y versiones cuando se incorpore código.

## Alcance de esta entrega

Estructura base y brief; el estudio y sus conclusiones permanecen pendientes. Proyecto educativo de investigación, sin recomendaciones de inversión personales.
