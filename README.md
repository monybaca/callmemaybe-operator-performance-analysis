# CallMeMaybe Operator Performance Analysis

Este proyecto analiza el desempeño operativo de los operadores de la plataforma de telefonía virtual **CallMeMaybe**, con el objetivo de medir su eficiencia y detectar posibles casos de ineficiencia. El análisis se basa en tres métricas principales: **tiempo promedio de espera**, **tasa de llamadas perdidas** y **volumen de llamadas salientes**. Estas métricas permiten identificar patrones de comportamiento y determinar qué operadores requieren intervención.

---

## 📌 Objetivo

- Evaluar el rendimiento de los operadores del sistema CallMeMaybe.
- Identificar tiempos de espera excesivos y patrones anómalos.
- Calcular y analizar la tasa de llamadas perdidas por operador.
- Medir la actividad de llamadas salientes como indicador de productividad.
- Crear criterios robustos para detectar operadores ineficientes.
- Realizar pruebas estadísticas que respalden las conclusiones.

---

## 🧾 Descripción de los datos

Los datasets incluyen:

### **Tabla de llamadas**
- `operator_id`: identificador del operador  
- `waiting_time`: tiempo de espera antes de atender  
- `is_missed_call`: indicador de llamada perdida  
- `outgoing_calls`: número de llamadas salientes  
- `call_duration`: duración de la llamada  

### **Tabla de clientela**
- `user_id`: identificador del cliente  
- `date_start`: fecha de registro  
- Variables adicionales de uso del servicio  

---

## 🧹 Preparación y Limpieza de Datos

- Conversión de fechas y tipos de datos.
- Cálculo del tiempo promedio de espera por operador.
- Cómputo de:
  - total de llamadas entrantes  
  - porcentaje de llamadas perdidas  
  - total de llamadas salientes  
- Identificación de valores extremos en:
  - tiempo de espera (operadores con ≥1.5 horas)  
  - tasa de llamadas perdidas  
- Depuración de filas inconsistentes o incompletas.

---

## 📊 Análisis Exploratorio (EDA)

- Distribución del tiempo de espera por operador.  
- Percentiles y detección de outliers.  
- Análisis de la tasa de llamadas perdidas, incluyendo percentiles 25%, 50%, 75% y top 1%.  
- Comparación del volumen de llamadas salientes entre operadores.  
- Visualización conjunta de métricas clave:
  - tiempo de espera vs. tasa de pérdida  
  - tiempo de espera vs. llamadas salientes  
  - tasa de pérdida vs. actividad  

---

## 🚩 Identificación de Operadores Ineficientes

Los operadores se evalúan en base a tres criterios principales:

1. **Tiempo de espera elevado**  
2. **Alta tasa de llamadas perdidas**  
3. **Baja cantidad de llamadas salientes**

Un operador se considera ineficiente si cumple uno o más de estos criterios.  
Se genera una clasificación final de operadores según el número de criterios que incumplen.

---

## 📈 Pruebas Estadísticas

Para validar diferencias significativa entre grupos se aplican pruebas como:

- Comparación de promedios (t-test o z-test).  
- Pruebas de diferencia de proporciones para la tasa de pérdidas.  
- Análisis comparativo entre operadores eficientes vs. ineficientes.  

Estas pruebas respaldan con evidencia si los operadores de bajo rendimiento presentan diferencias que no se deben al azar.

---

## 🔍 Hallazgos Principales

- Los operadores con tiempo de espera extremadamente alto también suelen tener tasas de pérdida elevadas.
- El análisis revela grupos pequeños con desempeño claramente deficiente.
- Muchos operadores cumplen con estándares de calidad, pero otros requieren intervención inmediata.
- Los criterios combinados (espera + pérdida + actividad) proporcionan una clasificación sólida para decisiones operativas.

---

## 🛠 Tecnologías Utilizadas

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib / Seaborn**
- **Statsmodels / SciPy**
- **Jupyter Notebook**

---

## 📁 Archivos del Proyecto

- `callmemaybe-operator-performance-analysis.ipynb` — Notebook principal.
- Datasets de llamadas y clientela proporcionados en la práctica.

---

## 📬 Contacto

Proyecto realizado como parte del portafolio analítico de **Monica Baca**.
