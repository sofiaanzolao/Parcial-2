# Parcial-2
# 🧑‍💻 Parcial 2 – Inteligencia Artificial Aplicada

Este repositorio contiene la entrega del **Parcial 2** de la materia *HE2 – Inteligencia Artificial Aplicada*.  
El objetivo del proyecto es predecir si una persona gana más de **$50.000 USD** anuales usando el dataset **Adult Census Income** del repositorio UCI.

## 📂 Contenido
- 📓 `Parcial_2.ipynb`: Notebook en Google Colab con todo el desarrollo (EDA, baseline, MLP en PyTorch).
- 📄 `Reporte_Parcial_2.pdf`: Reporte escrito con respuestas a las preguntas solicitadas.
- 📊 `adult_train_profile.html`: Reporte exploratorio (EDA) del conjunto de **entrenamiento**.
- 📊 `adult_val_profile.html`: Reporte exploratorio (EDA) del conjunto de **validación**.
- 📊 `adult_test_profile.html`: Reporte exploratorio (EDA) del conjunto de **prueba**.

## 🚀 Flujo de trabajo
1. **Recolección y procesamiento de datos**  
   - Limpieza y normalización  
   - OneHotEncoding + StandardScaler  
   - Split 50/50 del test → validación y prueba  

2. **Modelos**  
   - 🔹 Baseline: Regresión Logística  
   - 🔹 MLP en PyTorch (con y sin regularización)  

3. **Experimentos**  
   - ≥5 configuraciones de hiperparámetros sin regularización  
   - ≥5 configuraciones con Dropout + EarlyStopping  

4. **Evaluación**  
   - Métricas: Accuracy, Precisión, Recall, F1 y AUC  
   - Comparación entre regresión logística y MLP  

## 📊 Resultados esperados
- El baseline (logística) ofrece un punto de referencia.  
- El MLP sin regularización muestra riesgo de **overfitting**.  
- El MLP con Dropout y EarlyStopping mejora la capacidad de generalización.  

## 🛠️ Requisitos
- Python 3.9+  
- PyTorch  
- Scikit-learn  
- Pandas / Numpy / Matplotlib  

## 🙌 Autor
Entrega desarrollada por **Gabriela Zamora, Gilberto Galeana y Sofía Anzola**.
