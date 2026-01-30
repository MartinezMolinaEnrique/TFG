
> El notebook principal contiene **todo el flujo experimental**, desde la carga del dataset hasta el entrenamiento del modelo base.
> 
---

## 👤 Autor

**Enrique Martínez Molina**  
Grado en Ingeniería Informática – Universidad de Almería  

**Director del TFG:**  
Francisco José Orts Gómez  
Gracia Ester Martín Garzón  

---

## 📄 Licencia

Este proyecto se publica con fines **académicos y educativos**.  
El uso del código es libre para fines docentes o de investigación, citando adecuadamente la fuente.

---

# Evaluación de técnicas de Machine Learning en Sistemas de Detección de Intrusiones (IDS)

Este repositorio contiene el desarrollo experimental del **Trabajo Fin de Grado (TFG)** titulado:

> **“Evaluación de técnicas de Machine Learning en sistemas de detección de intrusiones (IDS)”**

realizado en el **Grado en Ingeniería Informática** de la **Universidad de Almería (UAL)**.

El objetivo principal del trabajo es analizar y comparar el rendimiento de distintos **algoritmos de Machine Learning** aplicados a la detección de intrusiones en redes, utilizando datasets de referencia en el ámbito de la ciberseguridad.

---

## 📌 Objetivos del proyecto

- Analizar el problema de la **detección de intrusiones en redes (IDS)** desde un enfoque de aprendizaje automático.
- Estudiar y preparar datasets clásicos utilizados en la literatura.
- Diseñar un **pipeline de preprocesamiento robusto**, evitando fugas de información (*data leakage*).
- Implementar un **modelo base de clasificación binaria** mediante **Regresión Logística**.
- Establecer una base sólida para la comparación posterior con otros algoritmos de ML/DL.

---

## 📊 Dataset utilizado

### NSL-KDD
Se utiliza el dataset **NSL-KDD**, una versión depurada del clásico KDD’99, ampliamente empleada en la evaluación de sistemas IDS.

- Archivos utilizados:
  - `KDDTrain+.txt` (conjunto de entrenamiento)
  - `KDDTest+.txt` (conjunto de prueba)
- Tipo de problema: **clasificación binaria**
  - `0` → tráfico normal
  - `1` → tráfico malicioso (ataque)

---

## ⚙️ Flujo de trabajo

El desarrollo sigue un flujo metodológico claro y reproducible:

1. **Carga del dataset**
2. **Análisis exploratorio inicial**
   - Tipos de datos
   - Valores nulos
   - Valores infinitos
   - Duplicados
3. **Limpieza del dataset**
   - Eliminación de duplicados
   - Eliminación de variables constantes
4. **Definición de variables**
   - Variables de entrada (`X`)
   - Variable objetivo (`y`)
5. **Split interno del conjunto de entrenamiento**
   - Entrenamiento / Validación (estratificado)
   - El conjunto de test oficial no se modifica
6. **Preprocesamiento**
   - Codificación One-Hot para variables categóricas
   - Escalado estándar de variables numéricas
   - Implementación mediante `ColumnTransformer`
7. **Verificaciones**
   - Dimensionalidad tras One-Hot Encoding
   - Número de categorías generadas
   - Correcta aplicación del escalado
8. **Modelo base**
   - Regresión Logística como baseline

---

## 🧠 Modelo base: Regresión Logística

La **regresión logística** se utiliza como modelo base debido a que:

- Es un algoritmo clásico y ampliamente documentado.
- Permite interpretar el problema en términos probabilísticos.
- Es sensible al escalado, lo que justifica el preprocesamiento aplicado.
- Sirve como referencia para comparar modelos más complejos.

---

## 🛠️ Tecnologías utilizadas

- **Python**
- **NumPy**
- **Pandas**
- **Scikit-learn**
- **Matplotlib**
- **Jupyter Notebook / Google Colab**
- **LaTeX (IEEE style)** para la memoria del TFG





