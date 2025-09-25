# 🧑‍💻 Parcial 2 – Inteligencia Artificial Aplicada

Este repositorio contiene la entrega del **Parcial 2** de la materia *HE2 – Inteligencia Artificial Aplicada*.  
El objetivo es predecir si una persona gana más de **50.000 USD** anuales usando el dataset **Adult Census Income** del repositorio UCI.

## 📂 Contenido
- 📓 `Parcial_2.ipynb`: Notebook en Google Colab con todo el desarrollo (EDA, baseline, MLP en PyTorch).  
- 📄 `Reporte_Parcial 2.pdf`: Reporte escrito con las respuestas al parcial.  
- 📊 `adult_train_profile.html`: Reporte exploratorio (EDA) del conjunto de **entrenamiento**.  
- 📊 `adult_val_profile.html`: Reporte exploratorio (EDA) del conjunto de **validación**.  
- 📊 `adult_test_profile.html`: Reporte exploratorio (EDA) del conjunto de **prueba**.  
- 📑 `resumen_experimentos.csv`: Resumen tabular de los resultados de todos los experimentos (sin y con regularización).  

## 🚀 Flujo de trabajo
1. **Procesamiento de datos**  
   - Limpieza de etiquetas y valores nulos.  
   - Eliminación de variables redundantes (`education`) y poco informativas (`fnlwgt`).  
   - Imputación de categorías faltantes con `"Unknown"`.  
   - Escalado con `StandardScaler` en numéricas y `OneHotEncoding` en categóricas.  
   - Split 50/50 del set de prueba → validación y test.  

2. **Modelos implementados**  
   - 🔹 **Baseline**: Regresión Logística.  
   - 🔹 **Redes Neuronales (MLP)** en PyTorch, con experimentos **sin regularización** y con **Dropout + Weight Decay + EarlyStopping**.  

3. **Experimentos**  
   - ≥5 configuraciones de hiperparámetros **sin regularización**.  
   - ≥5 configuraciones **con regularización**.  
   - Registro de métricas y pérdidas por época.  

4. **Evaluación**  
   - Métricas: **Precisión, Recall, F1 y AUC** (se priorizan sobre Accuracy por el desbalance de clases).  
   - Comparación: Baseline vs MLP (sin regularización vs con regularización).  

## 📊 Resultados principales
- **Mejor sin regularización**: `EXP5_capacidad_mínima_batch_grande_sin_reg`  
  - F1 (val) = 0.6537 | F1 (test) = 0.6828 | AUC (test) = 0.9126.  
  - Ajuste razonable sin señales fuertes de sobreajuste.  

- **Mejor con regularización**: `EXP5_con_reg_R5(p=0.5, wd=1e-2)`  
  - F1 (val) = 0.6612 | F1 (test) = 0.6915 | AUC (test) = 0.9162.  
  - Regularización mejoró la capacidad de generalización.  

- **Comparación con baseline (Regresión Logística)**:  
  - Logística logra mayor **recall (~0.84)** pero baja precisión (~0.57).  
  - El MLP regulado logra **mayor precisión (~0.74)** y mejor F1/AUC, mostrando un **balance más sólido** en un dataset desbalanceado.  

✅ **Conclusión:** El mejor modelo global fue el **MLP con regularización (EXP5 R5)**, ya que superó a los demás en F1 y AUC, confirmando que la regularización ayudó a mejorar el equilibrio entre precisión y recall.  

## 🛠️ Requisitos
- Python 3.9+  
- PyTorch  
- Scikit-learn  
- Pandas / Numpy / Matplotlib  

## 🙌 Autores
Entrega desarrollada por **Gabriela Zamora, Gilberto Galeana y Sofía Anzola Ortegón**.  

