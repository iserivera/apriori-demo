# Integración del Dataset Basket Optimisation mediante KaggleHub

Este repositorio contiene un ejemplo básico de cómo importar el conjunto de datos **Basket Optimisation** utilizando la biblioteca `kagglehub`, permitiendo su uso en entornos externos a Kaggle.

---

## 1. Descripción del Dataset

- **Nombre**: [dragonheir/basket-optimisation](https://www.kaggle.com/datasets/dragonheir/basket-optimisation)  
- **Proveedor**: Kaggle a través de la interfaz `kagglehub`  
- **Contenido**: Datos transaccionales para análisis de comportamiento de compra, comúnmente utilizados en sistemas de recomendación, minería de patrones de asociación y optimización de canastas de productos.

---

## 2. Requisitos

Antes de ejecutar el código, asegúrate de instalar la siguiente dependencia:

```bash
pip install kagglehub

```

Nota: Este entorno de ejecución puede diferir del entorno oficial de Kaggle. Es posible que necesites instalar otras dependencias adicionales según tu flujo de trabajo.

--

## 3. Ejecución del Código
A continuación se muestra el fragmento necesario para descargar el dataset:

``bash
import kagglehub
``


# Descarga del dataset y almacenamiento en ruta local

``bash
dragonheir_basket_optimisation_path = kagglehub.dataset_download('dragonheir/basket-optimisation')

print('Data source import complete.')
``

Una vez ejecutado, los archivos estarán disponibles localmente en la ruta asignada por kagglehub.

--

--
## 4. Estructura del Proyecto

.
├── README.md
├── main.ipynb
└── data/
    └── basket-optimisation/  # Carpeta descargada automáticamente por kagglehub


--

## 5. Posprocesamiento sugerido
Puedes usar pandas para cargar y explorar los archivos descargados:

``bash
import pandas as pd
import os

data_path = os.path.join(dragonheir_basket_optimisation_path, 'market_basket.csv')
df = pd.read_csv(data_path)

print(df.head())
``