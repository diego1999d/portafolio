# Proyecto 5 — Recuperación de oro (Gold Recovery)

## Descripción
Se construirá un modelo para predecir la eficiencia de recuperación en una planta metalúrgica y ayudar a decidir la optimización del proceso. El trabajo sigue las etapas de exploración, preprocesamiento, análisis y modelado.

## Archivos
- `data/gold_recovery_train.csv`
- `data/gold_recovery_test.csv`
- `data/gold_recovery_full.csv`
- `notebook/Notebook proyecto 5.ipynb`

## Objetivos
1. Preparar los datos.
2. Verificar el cálculo de `rougher.output.recovery` y comparar con el valor provisto.
3. Analizar variables ausentes en test y su tipo.
4. Preprocesar datos (imputación/escala/filtrado).
5. Analizar:
   - Cambios de concentración (Au, Ag, Pb) por etapa.
   - Distribución de tamaños de partícula en train vs. test.
   - Suma total de concentraciones por etapa y eliminación de anomalías si procede.
6. Construir modelos y evaluar con **sMAPE** (validación cruzada) y prueba final.

## Métrica (sMAPE)
\[
\text{sMAPE} = \frac{100}{n} \sum_{i=1}^{n} \frac{| \hat{y}_i - y_i |}{\left(|y_i| + |\hat{y}_i|\right)/2}
\]

## Librerías esperadas
`pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

## Estructura recomendada del notebook
1. Carga y vistazo inicial.
2. Verificación de recuperación y EAM.
3. Variables ausentes en test.
4. Preprocesamiento.
5. Análisis exploratorio (concentraciones, tamaños, outliers).
6. Modelado + validación cruzada (sMAPE).
7. Evaluación final y conclusiones.
