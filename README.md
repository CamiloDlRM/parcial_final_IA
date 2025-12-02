# parcial_final_IA



Clasificación de Calidad de Vino
Proyecto de machine learning para clasificar calidad de vino usando técnicas supervisadas y no supervisadas. Incluye implementación del algoritmo KNN en C.

Dataset
Dataset de Calidad de Vino del repositorio UCI con 1,599 muestras de vino tinto portugués. Contiene 11 propiedades químicas que predicen calidad en tres categorías: Malo, Bueno, Excelente.

Métodos
Preprocesamiento de datos con StandardScaler y división 70/30 entrenamiento-prueba. PCA redujo dimensiones a 9 componentes capturando 95% de varianza.

Aprendizaje no supervisado utilizó clustering K-means y DBSCAN. Baja coincidencia con clases reales indica estructura compleja.

Aprendizaje supervisado probó seis algoritmos: Random Forest, SVM, Regresión Logística, Árbol de Decisión, KNN y Naive Bayes.

Optimización aplicó Grid Search, SMOTE para balanceo de clases, ingeniería de características y métodos ensemble.

KNN implementado desde cero en C demostrando comprensión algorítmica.

Resultados
Stacking Ensemble final logró 72.7% de accuracy con F1-score de 0.724. Variables más importantes: alcohol, sulfatos y acidez volátil.
Random Forest base: 70.0% accuracy
Random Forest optimizado: 71.3% accuracy
Ensemble final: 72.7% accuracy

Validación cruzada confirmó generalización estable en todos los modelos.

Hallazgos Clave
Las propiedades químicas predicen efectivamente la calidad del vino pero el solapamiento de clases limita la precisión máxima. Los métodos ensemble superan a modelos individuales. La subjetividad humana en evaluación de calidad introduce ruido inherente.

Aplicaciones
Automatización de control de calidad en bodegas, optimización de producción, clasificación rápida para decisiones de embotellado.

Requisitos
Python: pandas, numpy, scikit-learn, matplotlib, seaborn, imbalanced-learn, umap-learn
C: compilador gcc con librería matemática

Uso
Ejecutar scripts de Python secuencialmente en Colab o Jupyter. Compilar implementación en C con gcc y ejecutar.

Limitaciones
Evaluaciones de calidad subjetivas, desbalanceo de clases, requiere mediciones de laboratorio.

Trabajo Futuro
Agregar más características, explorar deep learning, implementar SHAP para explicabilidad, desplegar como API de producción.
