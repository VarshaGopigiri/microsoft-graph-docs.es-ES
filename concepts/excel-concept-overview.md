# <a name="excel-workbooks-and-charts-api-overview"></a>Información general de la API de libros y gráficos de Excel

Excel es una herramienta de productividad indispensable. Los usuarios en todos los sectores y funciones la adoptan como una herramienta de almacenamiento, seguimiento y manipulación de todo tipo de datos. Se usa para todo, desde sencillos seguimientos de tareas y administración de datos, hasta cálculos complejos e informes profesionales. Puede usar la API de REST de Excel en Microsoft Graph para ampliar el valor de los datos, los cálculos, los informes y los paneles.

## <a name="why-integrate-with-excel"></a>¿Por qué debería realizar la integración con Excel?

Puede utilizar Microsoft Graph para permitir que las aplicaciones web y móviles lean y modifiquen los libros de Excel almacenados en OneDrive, SharePoint u otras plataformas de almacenamiento de información admitidas.

### <a name="perform-calculations"></a>Realizar cálculos

A los usuarios les gusta la facilidad con la que pueden realizar cálculos complejos y profundos desde Excel. Ahora puede acceder al potente motor de cálculo de Excel con resultados instantáneos. Por ejemplo, una calculadora de hipoteca puede aprovechar las ventajas de la función PAGO de Excel mediante una simple llamada de API que incluye el capital, la tasa y el número de pagos. Excel hace todo el trabajo difícil y devuelve el pago mensual al instante. Con más de 300 funciones de hoja de cálculo de Excel disponibles actualmente, tiene acceso total a la gran variedad de fórmulas compatibles con Excel a día de hoy. No es necesario reconstruir repetidamente modelos empresariales complejos. Los desarrolladores pueden programar Excel para realizar cálculos al instante y recuperar los resultados con llamadas de API simples.

### <a name="generate-reports-and-analyze-results"></a>Generar informes y analizar los resultados

Excel es una herramienta de análisis e informes flexible, que va desde tablas de datos simples a paneles profesionales complejos. Hoy le damos acceso completo a todas las características de informes de Excel, que convierten a Excel en un servicio de informes en línea en Office 365. Imagine cualquiera de los escenarios de creación de informes que crean los usuarios y de los que dependen a día de hoy colocados en una aplicación personalizada para crear diagramas profesionales o analizar grandes conjuntos de datos de forma inteligente, fusionándose sin problemas con Excel en estas experiencias personalizadas.

### <a name="store-and-track-data"></a>Almacenar y realizar un seguimiento de los datos

Excel también es una excelente herramienta para almacenar y realizar un seguimiento de los datos. Si la información se almacena en un libro, los datos están disponibles para cualquier aplicación que se integra con Office 365. Su contenido está disponible para la lectura desde soluciones personalizadas y estas pueden usar Excel para almacenar datos.

>**Nota:** La API de REST de Excel solo es compatible con libros de formato de archivo Office Open XML (archivos con la extensión `.xlsx`). Los libros con la extensión `.xls` no son compatibles. 

### <a name="using-the-excel-rest-api"></a>Usar la API de REST de Excel
Puede utilizar Microsoft Graph para permitir que las aplicaciones web y móviles lean y modifiquen los libros de Excel almacenados en OneDrive, SharePoint u otras plataformas de almacenamiento de información admitidas. El recurso `Workbook` (o el archivo de Excel) contiene todos los demás recursos de Excel mediante relaciones. Puede acceder a un libro a través de la API de Drive si identifica la ubicación del archivo en la dirección URL. Por ejemplo:

`https://graph.microsoft.com/{version}/me/drive/items/{id}/workbook/`

`https://graph.microsoft.com/{version}/me/drive/root:/{item-path}:/workbook/ `

Puede obtener acceso a un conjunto de objetos de Excel (como una tabla, intervalo o gráfico) mediante las API de REST estándares para realizar operaciones de creación, lectura, actualización y eliminación (CRUD) en el libro.

## <a name="next-steps"></a>Siguientes pasos

* [Administrar sesiones de Excel con Microsoft Graph](excel-manage-sessions.md)
* [Escribir en un libro de Excel con Microsoft Graph](excel-write-to-workbook.md)
* [Usar funciones de libro en Excel con Microsoft Graph](excel-use-functions.md)
* [Actualizar el formato de un rango en Excel con Microsoft Graph](excel-update-range-format.md)
* [Mostrar una imagen de gráfico de Excel con Microsoft Graph](excel-display-chart-image.md)
* [Usar la API de REST de Excel](../api-reference/v1.0/resources/excel.md)
