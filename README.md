📊**Análisis de Ventas de Producto por Ciudad**
Dashboard interactivo desarrollado en Power BI para analizar el comportamiento comercial de productos tecnológicos en las principales ciudades de Colombia.

🎯 **Objetivo**
Identificar patrones de ventas por producto y ciudad, detectar el mes de mayor rendimiento y visualizar la distribución del ingreso total, con el fin de apoyar la toma de decisiones comerciales basadas en datos.

📸 **Vista del dashboard**
adjunto en los archivos del repositorio

📌** Principales hallazgos**

Ventas totales: $714 millones COP en el período analizado
Producto líder: Monitor con el 21.85% del total de ventas ($156M)
Ciudad líder: Medellín concentra el mayor volumen de ventas
Mes pico: Enero registró las ventas más altas del año (~$100M)
Los 5 productos analizados tienen una distribución bastante equilibrada (entre 16% y 22% cada uno), lo que indica una demanda diversificada


🗂️ **Contenido del repositorio**
ArchivoDescripciónAnalisis de Ventas de producto x ciudad.pbixArchivo Power BI con el dashboard completoAnalisis de Ventas de producto x ciudad.pdfExportación en PDF del dashboardCaptura de pantalla 2026-04-28 131002.pngVista previa del dashboard

📊 **Visualizaciones incluidas**

KPIs — Ventas totales, producto líder, ciudad líder y mes pico
Gráfico de barras apiladas — Ventas por ciudad desglosadas por producto
Gráfico de torta — Participación porcentual por producto
Barras horizontales — Comparativo de ventas por ciudad
Barras verticales — Tendencia de ventas mes a mes
Tabla resumen — Ranking de productos con ventas totales


🛠️ **Herramientas utilizadas**

Power BI Desktop — Construcción del dashboard y visualizaciones
DAX — Medidas calculadas para KPIs dinámicos (producto líder, ciudad líder, mes pico)
Power Query — Transformación y limpieza de datos


💡 **Medidas DAX destacadas**
dax-- Producto con mayor volumen de ventas
Producto Líder = 
CALCULATE(
    SELECTEDVALUE(Ventas[Producto]),
    TOPN(1, ALL(Ventas[Producto]), CALCULATE(SUM(Ventas[Monto])), DESC)
)

-- Ciudad con mayor volumen de ventas
Ciudad Líder = 
CALCULATE(
    SELECTEDVALUE(Ventas[Ciudad]),
    TOPN(1, ALL(Ventas[Ciudad]), CALCULATE(SUM(Ventas[Monto])), DESC)
)

-- Mes con mayor volumen de ventas
Mes Líder = 
CALCULATE(
    SELECTEDVALUE(Ventas[Mes]),
    TOPN(1, ALL(Ventas[Mes]), CALCULATE(SUM(Ventas[Monto])), DESC)
)

👩‍💻 Autora
Laura Katherine Cuevas Alba
Data Analyst en formación | SQL · Python · Power BI
LinkedIn · GitHub
