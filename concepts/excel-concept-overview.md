# <a name="excel-workbooks-and-charts-api-overview"></a><span data-ttu-id="04066-101">Información general de la API de libros y gráficos de Excel</span><span class="sxs-lookup"><span data-stu-id="04066-101">Excel workbooks and charts API overview</span></span>

<span data-ttu-id="04066-102">Excel es una herramienta de productividad indispensable.</span><span class="sxs-lookup"><span data-stu-id="04066-102">Excel is an indispensable productivity tool.</span></span> <span data-ttu-id="04066-103">Los usuarios en todos los sectores y funciones la adoptan como una herramienta de almacenamiento, seguimiento y manipulación de todo tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="04066-103">Users across all industries and job functions embrace it as a tool for storing, tracking, and manipulating all kinds of data.</span></span> <span data-ttu-id="04066-104">Se usa para todo, desde sencillos seguimientos de tareas y administración de datos, hasta cálculos complejos e informes profesionales.</span><span class="sxs-lookup"><span data-stu-id="04066-104">It's used for everything from simple task tracking and data management, to complex calculations and professional reporting.</span></span> <span data-ttu-id="04066-105">Puede usar la API de REST de Excel en Microsoft Graph para ampliar el valor de los datos, los cálculos, los informes y los paneles.</span><span class="sxs-lookup"><span data-stu-id="04066-105">You can use the Excel REST API in Microsoft Graph to extend the value of your data, calculations, reporting, and dashboards.</span></span>

## <a name="why-integrate-with-excel"></a><span data-ttu-id="04066-106">¿Por qué debería realizar la integración con Excel?</span><span class="sxs-lookup"><span data-stu-id="04066-106">Why integrate with Excel?</span></span>

<span data-ttu-id="04066-107">Puede utilizar Microsoft Graph para permitir que las aplicaciones web y móviles lean y modifiquen los libros de Excel almacenados en OneDrive, SharePoint u otras plataformas de almacenamiento de información admitidas.</span><span class="sxs-lookup"><span data-stu-id="04066-107">You can use Microsoft Graph to allow web and mobile applications to read and modify Excel workbooks stored in OneDrive, SharePoint, or other supported storage platforms. The  (or Excel file) resource contains all the other Excel resources through relationships. You can access a workbook through the Drive API by identifying the location of the file in the URL. For example:</span></span>

### <a name="perform-calculations"></a><span data-ttu-id="04066-108">Realizar cálculos</span><span class="sxs-lookup"><span data-stu-id="04066-108">Perform date calculations.</span></span>

<span data-ttu-id="04066-109">A los usuarios les gusta la facilidad con la que pueden realizar cálculos complejos y profundos desde Excel.</span><span class="sxs-lookup"><span data-stu-id="04066-109">Users love the ease with which they can perform deep and complex calculations within Excel.</span></span> <span data-ttu-id="04066-110">Ahora puede acceder al potente motor de cálculo de Excel con resultados instantáneos.</span><span class="sxs-lookup"><span data-stu-id="04066-110">You can now access Excel’s powerful calculation engine with instant results.</span></span> <span data-ttu-id="04066-111">Por ejemplo, una calculadora de hipoteca puede aprovechar las ventajas de la función PAGO de Excel mediante una simple llamada de API que incluye el capital, la tasa y el número de pagos.</span><span class="sxs-lookup"><span data-stu-id="04066-111">For example, a mortgage calculator can take advantage of the PMT function from Excel by making a simple API call that includes principal, rate and number of payments.</span></span> <span data-ttu-id="04066-112">Excel hace todo el trabajo difícil y devuelve el pago mensual al instante.</span><span class="sxs-lookup"><span data-stu-id="04066-112">Excel does all the difficult work and returns the monthly payment instantly.</span></span> <span data-ttu-id="04066-113">Con más de 300 funciones de hoja de cálculo de Excel disponibles actualmente, tiene acceso total a la gran variedad de fórmulas compatibles con Excel a día de hoy.</span><span class="sxs-lookup"><span data-stu-id="04066-113">With more than 300 Excel worksheet functions currently available, you have full access to the breadth of formulas supported by Excel today.</span></span> <span data-ttu-id="04066-114">No es necesario reconstruir repetidamente modelos empresariales complejos.</span><span class="sxs-lookup"><span data-stu-id="04066-114">Complex business models don’t need to be rebuilt repeatedly.</span></span> <span data-ttu-id="04066-115">Los desarrolladores pueden programar Excel para realizar cálculos al instante y recuperar los resultados con llamadas de API simples.</span><span class="sxs-lookup"><span data-stu-id="04066-115">Developers can program Excel to perform those calculations instantly and retrieve the results with simple API calls.</span></span>

### <a name="generate-reports-and-analyze-results"></a><span data-ttu-id="04066-116">Generar informes y analizar los resultados</span><span class="sxs-lookup"><span data-stu-id="04066-116">Generate reports and analyze results</span></span>

<span data-ttu-id="04066-117">Excel es una herramienta de análisis e informes flexible, que va desde tablas de datos simples a paneles profesionales complejos.</span><span class="sxs-lookup"><span data-stu-id="04066-117">Excel is a flexible reporting and analysis tool, from simple data tables to complex professional dashboards.</span></span> <span data-ttu-id="04066-118">Hoy le damos acceso completo a todas las características de informes de Excel, que convierten a Excel en un servicio de informes en línea en Office 365.</span><span class="sxs-lookup"><span data-stu-id="04066-118">Today, we give you full access to all of Excel’s reporting features, making Excel an online reporting service within Office 365.</span></span> <span data-ttu-id="04066-119">Imagine cualquiera de los escenarios de creación de informes que crean los usuarios y de los que dependen a día de hoy colocados en una aplicación personalizada para crear diagramas profesionales o analizar grandes conjuntos de datos de forma inteligente, fusionándose sin problemas con Excel en estas experiencias personalizadas.</span><span class="sxs-lookup"><span data-stu-id="04066-119">Imagine any of the reporting scenarios users create and rely on today pulled into a custom app to create professional charts or analyze large sets of data intelligently, seamlessly blending Excel into those customized experiences.</span></span>

### <a name="store-and-track-data"></a><span data-ttu-id="04066-120">Almacenar y realizar un seguimiento de los datos</span><span class="sxs-lookup"><span data-stu-id="04066-120">Store and track data</span></span>

<span data-ttu-id="04066-121">Excel también es una excelente herramienta para almacenar y realizar un seguimiento de los datos.</span><span class="sxs-lookup"><span data-stu-id="04066-121">Excel is also a great tool to store and track data.</span></span> <span data-ttu-id="04066-122">Si la información se almacena en un libro, los datos están disponibles para cualquier aplicación que se integra con Office 365.</span><span class="sxs-lookup"><span data-stu-id="04066-122">If your information is stored in a workbook, that data is available to any app that integrates with Office 365.</span></span> <span data-ttu-id="04066-123">Su contenido está disponible para la lectura desde soluciones personalizadas y estas pueden usar Excel para almacenar datos.</span><span class="sxs-lookup"><span data-stu-id="04066-123">Its contents are available to read from custom solutions, and those solutions can use Excel for data storage.</span></span>

><span data-ttu-id="04066-124">**Nota:** La API de REST de Excel solo es compatible con libros de formato de archivo Office Open XML (archivos con la extensión `.xlsx`).</span><span class="sxs-lookup"><span data-stu-id="04066-124">**Note:** The Excel REST API supports only Office Open XML file formatted workbooks. The `.xlsx` extension workbooks are not supported.</span></span> <span data-ttu-id="04066-125">Los libros con la extensión `.xls` no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="04066-125">The `.xls` extension workbooks are not supported.</span></span> 

### <a name="using-the-excel-rest-api"></a><span data-ttu-id="04066-126">Usar la API de REST de Excel</span><span class="sxs-lookup"><span data-stu-id="04066-126">Using the Excel Services 2010 REST API</span></span>
<span data-ttu-id="04066-127">Puede utilizar Microsoft Graph para permitir que las aplicaciones web y móviles lean y modifiquen los libros de Excel almacenados en OneDrive, SharePoint u otras plataformas de almacenamiento de información admitidas.</span><span class="sxs-lookup"><span data-stu-id="04066-127">You can use Microsoft Graph to allow web and mobile applications to read and modify Excel workbooks stored in OneDrive, SharePoint, or other supported storage platforms. The  (or Excel file) resource contains all the other Excel resources through relationships. You can access a workbook through the Drive API by identifying the location of the file in the URL. For example:</span></span> <span data-ttu-id="04066-128">El recurso `Workbook` (o el archivo de Excel) contiene todos los demás recursos de Excel mediante relaciones.</span><span class="sxs-lookup"><span data-stu-id="04066-128">The `Workbook` (or Excel file) resource contains all the other Excel resources through relationships.</span></span> <span data-ttu-id="04066-129">Puede acceder a un libro a través de la API de Drive si identifica la ubicación del archivo en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="04066-129">You can access a workbook through the Drive API by identifying the location of the file in the URL.</span></span> <span data-ttu-id="04066-130">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="04066-130">For example:</span></span>

`https://graph.microsoft.com/{version}/me/drive/items/{id}/workbook/`

`https://graph.microsoft.com/{version}/me/drive/root:/{item-path}:/workbook/ `

<span data-ttu-id="04066-131">Puede obtener acceso a un conjunto de objetos de Excel (como una tabla, intervalo o gráfico) mediante las API de REST estándares para realizar operaciones de creación, lectura, actualización y eliminación (CRUD) en el libro.</span><span class="sxs-lookup"><span data-stu-id="04066-131">You can access a set of Excel objects (such as Table, Range, or Chart) by using standard REST APIs to perform create, read, update, and delete (CRUD) operations on the workbook.</span></span>

## <a name="next-steps"></a><span data-ttu-id="04066-132">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="04066-132">Next steps</span></span>

* [<span data-ttu-id="04066-133">Administrar sesiones de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="04066-133">Manage sessions in Excel with Microsoft Graph</span></span>](excel-manage-sessions.md)
* [<span data-ttu-id="04066-134">Escribir en un libro de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="04066-134">Write to an Excel workbook using Microsoft Graph</span></span>](excel-write-to-workbook.md)
* [<span data-ttu-id="04066-135">Usar funciones de libro de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="04066-135">Use workbook functions in Excel with Microsoft Graph</span></span>](excel-use-functions.md)
* [<span data-ttu-id="04066-136">Actualizar el formato de un rango en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="04066-136">Update a range’s format in Excel with Microsoft Graph</span></span>](excel-update-range-format.md)
* [<span data-ttu-id="04066-137">Mostrar una imagen del gráfico en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="04066-137">Display a chart image in Excel with Microsoft Graph</span></span>](excel-display-chart-image.md)
* [<span data-ttu-id="04066-138">Usar la API de REST de Excel</span><span class="sxs-lookup"><span data-stu-id="04066-138">Use the Excel REST API</span></span>](../api-reference/v1.0/resources/excel.md)