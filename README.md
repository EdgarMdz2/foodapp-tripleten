# 🍫 Food App - A/B Test  

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)

## 📌 Descripción  
Este proyecto corresponde al análisis de datos de una aplicación del sector **foodtech**, enfocada en la compra y entrega de productos alimenticios.  
El objetivo principal fue entender cómo los usuarios interactúan con la aplicación y evaluar, mediante pruebas de hipótesis, si un cambio en el diseño tipográfico afecta la conversión hacia la compra.  

El trabajo se presenta en un **Jupyter Notebook** para su lectura y consulta.  
⚠️ Nota: Los datos utilizados son privados, por lo que no se incluyen en este repositorio.  

---

## 🎯 Contexto del análisis  
El análisis se dividió en dos áreas clave:  

1. **Embudo de conversión**  
   - Identificar qué proporción de usuarios completa el proceso de compra.  
   - Detectar en qué etapas ocurre la mayor fricción.  
   - Señalar puntos de optimización para mejorar la conversión.  

2. **Prueba A/A/B de rediseño**  
   - Se evaluó un cambio en la tipografía de la aplicación.  
   - Se diseñó un test con **dos grupos de control (A/A)** y un **grupo experimental (B)**.  
   - El objetivo fue medir si la nueva tipografía impactaba de manera positiva o negativa en el comportamiento de los usuarios.  

---

## 🗂️ Datos  
Cada registro del dataset corresponde a un evento generado por un usuario en la app.  

- **EventName**: tipo de evento (inicio de sesión, vista de producto, compra, etc.).  
- **DeviceIDHash**: identificador único del usuario.  
- **EventTimestamp**: marca temporal del evento.  
- **ExpId**: identificador del experimento.  
  - `246` y `247`: grupos de control.  
  - `248`: grupo experimental.  

---

## 🔍 Metodología  
1. **Preparación de los datos**: renombrado de columnas, verificación de duplicados y valores nulos.  
2. **EDA (Exploratory Data Analysis)**: análisis temporal de registros para asegurar un periodo representativo.  
3. **Embudo de conversión**: análisis del flujo de eventos principales:  
   - MainScreenAppear → OffersScreenAppear → CartScreenAppear → PaymentScreenSuccessful.  
4. **A/B Testing**:  
   - Aplicación de pruebas de hipótesis.  
   - Ajuste del nivel de significancia por comparaciones múltiples.  

---

## 📊 Resultados principales  
- El embudo de conversión permitió identificar etapas con mayor fricción en el proceso de compra.  
- El test A/A confirmó la consistencia de los datos.  
- El test A/B no mostró diferencias **estadísticamente significativas** en la tasa de conversión entre el grupo experimental y los controles.  
- Los valores p significativos en comparaciones iniciales (A1/A2 y A2/B) no se mantuvieron tras aplicar la corrección por comparaciones múltiples.  

👉 **Conclusión**: El rediseño tipográfico no generó un efecto medible en la conversión de los usuarios.  

---

## 🛠️ Tecnologías utilizadas  
- **Python**  
- **Pandas, NumPy** (manejo y análisis de datos)  
- **Matplotlib, Seaborn** (visualización)  
- **SciPy, Statsmodels** (pruebas estadísticas)  
