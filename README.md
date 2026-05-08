# ConnectaTel - Análisis de Comportamiento de Clientes

## Descripción del Proyecto

Este proyecto analiza el comportamiento de los clientes de **ConnectaTel**, una empresa de telecomunicaciones en Latinoamérica.

El objetivo principal es explorar, limpiar y analizar los datos de clientes y consumo para identificar:
- patrones de uso,
- segmentos de clientes,
- valores atípicos (outliers),
- y oportunidades de negocio.

El análisis se realiza con información registrada hasta el año **2024**.

---

# Datasets Utilizados

## `plans.csv`
Contiene información de los planes telefónicos:
- minutos incluidos,
- GB incluidos,
- costos adicionales,
- precio mensual.

---

## `users.csv`
Información de clientes:
- ID de usuario,
- edad,
- ciudad,
- fecha de registro,
- tipo de plan,
- churn.

---

## `usage.csv`
Registros detallados de uso:
- llamadas,
- mensajes,
- duración,
- fechas de actividad.

---

# Tecnologías Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# Etapas del Análisis

## 1. Carga y Exploración de Datos
- Importación de datasets.
- Revisión de estructura y tipos de datos.
- Identificación de valores nulos e inconsistencias.

---

## 2. Análisis de Calidad de Datos

Se detectaron:
- valores faltantes,
- sentinels,
- categorías inconsistentes,
- fechas inválidas.

### Principales problemas detectados

| Columna | Problema |
|---|---|
| `city` | Valores nulos e inconsistencias |
| `age` | Sentinel `-999` |
| `reg_date` | Fechas futuras (2026) |
| `duration` / `length` | Alto porcentaje de nulos |

---

## 3. Limpieza de Datos

Se aplicaron procesos de:
- reemplazo de sentinels,
- tratamiento de nulos,
- conversión de fechas,
- estandarización de categorías.

---

## 4. Agregación de Métricas por Usuario

Se construyeron métricas agregadas:
- `cant_mensajes`
- `cant_llamadas`
- `cant_minutos_llamada`

Posteriormente se integraron con la tabla de usuarios.

---

## 5. Análisis Exploratorio de Datos (EDA)

### Estadística descriptiva
Se analizaron:
- medias,
- medianas,
- distribuciones,
- outliers.

### Visualizaciones
Se desarrollaron:
- histogramas,
- curvas KDE,
- boxplots.

Variables analizadas:
- edad,
- cantidad de mensajes,
- cantidad de llamadas,
- minutos consumidos.

---

## 6. Segmentación de Clientes

### Segmentación por Uso
Los usuarios fueron clasificados en:
- Bajo uso
- Uso medio
- Alto uso

---

# Hallazgos Principales

## Plan Básico
- Mayor volumen de usuarios.
- Principal canal de adquisición.
- Alto nivel de actividad general.

---

## Plan Premium
- Menor cantidad de usuarios.
- Mayor intensidad de consumo.
- Mayor potencial de rentabilidad.
- Usuarios más estables.

---

## Patrones de Uso
- La mayoría de usuarios presenta consumo moderado.
- Las distribuciones muestran sesgo hacia la derecha.
- Existe un pequeño grupo de usuarios intensivos.

---

## Outliers
Se identificaron usuarios con consumos extremos en:
- llamadas,
- mensajes,
- minutos consumidos.

Estos usuarios podrían representar:
- clientes VIP,
- oportunidades comerciales,
- segmentos de alto valor.

---

# Insights Relevantes

- Los usuarios Premium presentan mayor consumo de minutos.
- El plan Básico domina en cantidad de clientes.
- El comportamiento de uso es relativamente estable entre edades.
- Los usuarios intensivos representan oportunidades de monetización.

---

# Cómo Ejecutar el Proyecto

Haz clic en el siguiente botón:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](URL_DEL_NOTEBOOK_EN_GITHUB)

O:

1. Abre el archivo `.ipynb` en GitHub
2. Haz clic en **Open in Colab**

## Cómo reproducir el análisis

1. Abre `data_clean_connectatel.ipynb`
2. Ejecuta las celdas en orden

---

# Estructura del Proyecto

```bash
├── data/
│   ├── plans.csv
│   ├── users.csv
│   └── usage.csv
│
├── notebooks/
│   └── data_clean_connectatel.ipynb
│
└── README.md

---
