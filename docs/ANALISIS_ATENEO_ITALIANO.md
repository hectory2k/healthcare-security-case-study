**3 puntos aplicables a VigiSalud:**

1. **Calidad del dato antes que todo.** Garbage in, garbage out. Cualquier sesgo en los registros de guardia (subtriage, datos faltantes, inconsistencias) se transfiere directo al modelo. Validar y limpiar antes de entrenar, siempre.

2. **R² del 61% es aceptable en guardia, no en UCI.** El paper SARIMA reportó 61% de determinación con MAPE ~7.4%. VigiSalud tiene MAE ~7.0 con Random Forest — rendimiento comparable o mejor. El benchmark de referencia para decisiones operativas no necesita superar el 80% de meteorología; alcanza con orientar la planificación de turnos.

3. **El entregable es la acción, no el número.** El tablero del Hospital Italiano detectó subtriage masivo → creó unidad de dolor torácico → midió tiempo síntoma-ECG. El modelo predice, pero el valor real está en qué hace la guardia con esa predicción (refuerzo de personal, alertas Telegram, etc.).


1. Calidad del dato: Ya lo tenés con el glosario formoseño y la validación OCR.
2. MAE 7.0 es competitivo: Comparable al SARIMA del paper (R² 61%).
3. El valor está en la acción: No es solo predecir, es qué hace la guardia con esa predicción. Tus alertas de Telegram ya hacen eso.
