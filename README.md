# Diagnóstico de Salud Laboral y Clima Organizacional 📊💼

## 📋 Descripción del Proyecto
Este proyecto desarrolla un diagnóstico analítico integral sobre la salud laboral y el clima interno de una organización mediante un enfoque basado en datos (*Data-Driven*). El objetivo principal es evaluar la interacción interdepartamental entre la remuneración económica, la sobrecarga laboral (horas extras), la satisfacción del colaborador y el impacto logístico del tiempo de traslado (distancia a la oficina).

A través de este análisis, se identifican cuellos de botella operativos y perfiles en "Alerta Roja" con alto riesgo de fuga (rotación voluntaria), proponiendo recomendaciones accionables de "Inversión Cero" para optimizar la retención de talento.

## 📊 Reporte de Negocio e Insights (PDF)
El desarrollo técnico está respaldado por un informe ejecutivo detallado que traduce las métricas del script en estrategias comerciales de retención.

* 📄 **[Ver Reporte Completo: Diagnostico Salud Laboral y Clima Organizacional](./Diagn%C3%B3stico%20de%20Salud%20Laboral%20y%20Clima%20Organizacional)**

---

## 🛠️ Tecnologías y Herramientas Utilizadas
* **Lenguaje:** Python
* **Librerías de Manipulación de Datos:** Pandas, NumPy
* **Librerías de Visualización:** Matplotlib / Seaborn
* **Entorno de Desarrollo:** Jupyter Notebook / Google Colab

---

## 📊 Metodología y Procesamiento de Datos

### 1. Feature Engineering (Procesamiento Avanzado)
Para transformar las métricas continuas en insights de negocio asimilables y de rápida lectura, se aplicó una lógica de segmentación avanzada utilizando `np.select` de NumPy para crear las siguientes dimensiones:

* **Clasificación de Salario:** Alto ($\ge \$100.000$), Medio ($\ge \$80.000$), Bajo ($< \$80.000$).
* **Clasificación de Distancia:** Larga ($\ge 25\text{ km}$), Media ($\ge 15\text{ km}$), Corta ($< 15\text{ km}$).
* **Nivel de Antigüedad:** Alta ($\ge 12\text{ años}$), Media ($\ge 8\text{ años}$), Baja ($< 8\text{ años}$).
* **Clasificación de Satisfacción:** Alta ($\ge 4$), Media ($= 3$), Baja ($< 3$).
* **Carga de Horas Extras:** Alta ($\ge 25\text{ hrs}$), Media ($\ge 11\text{ hrs}$), Baja ($< 11\text{ hrs}$).

### 2. Análisis Interdepartamental (Tablas Pivot)
Cruzando las nuevas variables categóricas, se consolidó la siguiente matriz métrica por sector:

| Departamento | Horas Extras / Mes | Salario Promedio | % Part. Salarial | Promedio Satisfacción |
| :--- | :---: | :---: | :---: | :---: |
| **IT** | 67 | \$120,666.67 | 24.69% | 2.67 |
| **Ventas** | 45 | \$100,000.00 | 20.46% | 3.00 |
| **Marketing** | 40 | \$71,500.00 | 14.63% | 1.50 |
| **RRHH** | 5 | \$88,000.00 | 18.01% | 4.00 |
| **Finanzas** | 0 | \$108,500.00 | 22.20% | 5.00 |

---

## 🔍 Hallazgos Clave y Primeras Impresiones

1. **Finanzas (Departamento Modelo):** Presenta el nivel de satisfacción máximo (5.0), salarios competitivos y un esquema de cero horas extras.
2. **IT y Ventas (Zonas de Desgaste):** A pesar de contar con las mejores remuneraciones, registran una satisfacción Media-Baja provocada por la alta carga de horas extras acumuladas.
3. **Marketing (Estado Crítico):** Registra los salarios más bajos de la organización, alta carga horaria extra y la satisfacción promedio más baja (1.50).
4. **Factor Clave de Retención:** El análisis demostró que el **100% de los colaboradores con Satisfacción Alta comparten una Carga de Horas Extras Baja**, validando la correlación directa entre el agotamiento horario y la insatisfacción.

### 🚨 Detección de Perfiles en Alerta Roja (Riesgo de Fuga)
* **ID 1004 (Marketing):** Satisfacción mínima (1.0), salario bajo, 28 horas extras y factor estresor por traslado largo (28 km).
* **ID 1007 (Ventas):** Satisfacción crítica (2.5), alta exposición a horas extras (35 mensuales) y distancia extrema de traslado (38 km).

---

## 📈 Visualizaciones Estadísticas
El repositorio incluye gráficos de dispersión (*Scatter Plots*) generados en Python que convalidan visualmente las hipótesis de negocio:
* **Relación Sueldo vs. Satisfacción:** Identifica la dispersión del clima según la recompensa económica por depto.
* **Relación Horas Extras vs. Satisfacción:** Evidencia de forma contundente cómo decae la satisfacción a medida que aumentan las horas extra por mes.

*(Podés guardar tus gráficos como imágenes e insertarlos acá usando: `![Sueldo vs Satisfaccion](ruta/tu_grafico1.png)`)*

---

## 💡 Conclusiones y Recomendaciones de "Inversión Cero"
Para estabilizar el ecosistema corporativo sin incurrir en incrementos masivos de presupuesto, se proponen tres acciones estratégicas inmediatas:

1. **Redistribución Operativa:** Regular de forma estricta las horas adicionales en IT y Ventas mediante eficiencias de procesos y balanceo de cargas de trabajo.
2. **Flexibilidad Geográfica (Home Office):** Implementar un modelo híbrido o de teletrabajo focalizado para el personal expuesto a distancias mayores a 25 km, eliminando el desgaste del trayecto diario.
3. **Saneamiento en Marketing:** Ajustar la base de la pirámide salarial en el sector más postergado para alinearlo equitativamente con su esfuerzo operativo.

---


## 💻 Código Fuente
El desarrollo completo de la vista analítica con el script optimizado se encuentra documentado y listo para su ejecución en la sección de archivos del repositorio:

* 💾 **[Ver Script Completo](./People_Analythics.ipynb)** 
