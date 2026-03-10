# EDA-Python

## Pasos realizados en el proyecto

1. **Carga de datos:**
   - Importación del archivo `bank-additional.xlsx`.
   - Consolidación de las distintas hojas presentes en `customer-details.xlsx`.

2. **Limpieza y preparación de datos:**
   - Relleno de valores faltantes en variables categóricas y numéricas.
   - Conversión de tipos de datos (`ID` convertido a string).
   - Eliminación de registros duplicados.
   - Generación de rangos de edad e ingresos (`tramos_edad`, `tramos_income`).

3. **Integración de datasets:**
   - Unión de los datasets mediante `merge` usando `id_` y `ID`, creando el DataFrame final `df_cruzado`.

4. **Análisis exploratorio de datos:**
   - Evaluación de la distribución de variables categóricas (`job`, `marital`, `education`, `contact`).
   - Exploración de variables numéricas (`age`, `campaign`, `income`).
   - Creación de visualizaciones utilizando `Seaborn` y `Matplotlib`.

5. **Exportación del dataset procesado:**
   - Guardado del DataFrame final en formato `df_cruzado.csv`.

---

## Resultados del análisis

### Variables categóricas

- `job`: las categorías *student* y *retired* muestran las mayores tasas de conversión, aunque su representación en el dataset es reducida.
- `marital`: el grupo *single* presenta una conversión ligeramente superior.
- `education`: el grupo *illiterate* destaca en conversión, aunque con muy pocos registros. También resalta *university.degree* con resultados positivos.
- `contact`: el contacto realizado mediante *cellular* resulta significativamente más eficaz que mediante *telephone*.

### Variables numéricas

- `campaign`: se observa que a medida que aumenta el número de intentos de contacto, la tasa de conversión disminuye.
- `age`: los individuos mayores de 60 años presentan mayores tasas de conversión, aunque constituyen una parte pequeña del total.
- `income`: las tasas de conversión son bastante similares entre los distintos niveles de ingresos, por lo que no parece ser una variable determinante.

### Relación `age` vs `income`

- No se identifica una correlación fuerte entre edad e ingresos.
- Tampoco se aprecia un patrón claro que conecte directamente ambas variables con el éxito de la campaña.

---

## Cómo ejecutar

1. Clona este repositorio:
git clone