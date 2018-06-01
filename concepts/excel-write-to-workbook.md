# <a name="write-data-to-an-excel-workbook-with-microsoft-graph"></a><span data-ttu-id="57311-101">Escribir datos en un libro de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="57311-101">Write data to an Excel workbook with Microsoft Graph</span></span>

<span data-ttu-id="57311-102">La API de REST de Excel proporciona una forma sencilla, independiente de la plataforma para cargar información en un libro de Excel.</span><span class="sxs-lookup"><span data-stu-id="57311-102">The Excel REST API provides an easy, platform-agnostic way to upload information to an Excel workbook.</span></span> <span data-ttu-id="57311-103">Este tema muestra cómo escribir conjuntos de datos simples en un libro de Excel en tres marcos de desarrollo web: ASP.NET, Angular y React.</span><span class="sxs-lookup"><span data-stu-id="57311-103">This topic shows you how to write simple data sets to an Excel workbook on three web development frameworks: ASP.NET, Angular, and React.</span></span> <span data-ttu-id="57311-104">Puede mirar los ejemplos de código destacados en este tema visitando las [muestras de inicio de Excel de Microsoft Graph en GitHub](https://github.com/microsoftgraph?utf8=%E2%9C%93&q=excelstarter).</span><span class="sxs-lookup"><span data-stu-id="57311-104">You can look at the code samples featured in this topic by visiting the [Microsoft Graph Excel starter samples on GitHub](https://github.com/microsoftgraph?utf8=%E2%9C%93&q=excelstarter).</span></span>

> <span data-ttu-id="57311-105">**Nota:** los tres ejemplos escriben datos en un libro de Excel denominado **demo.xlxs**.</span><span class="sxs-lookup"><span data-stu-id="57311-105">**Note:** All three of the samples write data to an Excel workbook named **demo.xlxs**.</span></span> <span data-ttu-id="57311-106">Le proporcionan este libro para que pueda cargarlo en su propio OneDrive, pero también puede usar Microsoft Graph para cargar archivos en OneDrive.</span><span class="sxs-lookup"><span data-stu-id="57311-106">They provide this workbook for you so that you can upload it to your own OneDrive, but you can also use Microsoft Graph to upload files to OneDrive.</span></span> <span data-ttu-id="57311-107">Si le interesa obtener información sobre las llamadas de REST que necesita cargar un archivo de cualquier tipo a la carpeta raíz de OneDrive, consulte el [ejemplo de lista de tareas pendientes de ASP.NET de la API de REST de Excel de Microsoft Graph](https://github.com/microsoftgraph/aspnet-todo-rest-sample).</span><span class="sxs-lookup"><span data-stu-id="57311-107">If you're interested in learning the REST calls you need to upload a file of any type to your root OneDrive folder, see the [Microsoft Graph Excel REST API ASP.NET to-do list sample](https://github.com/microsoftgraph/aspnet-todo-rest-sample).</span></span>

<span data-ttu-id="57311-108">Las tres muestras de ejemplo de Excel hacen lo mismo: recuperar el nombre y la dirección del usuario que ha iniciado sesión y agregar los dos elementos de información a una nueva fila en el libro **demo.xlsx**.</span><span class="sxs-lookup"><span data-stu-id="57311-108">All three of the Excel starter samples do the same thing: retrieve the name and address of the signed-in user and add those two pieces of information to a new row in the **demo.xlsx** workbook.</span></span> <span data-ttu-id="57311-109">Puede modificar las muestras para agregar más filas agregando información a la matriz bidimensional que representa la fila o filas que desea agregar.</span><span class="sxs-lookup"><span data-stu-id="57311-109">You can modify the samples to add additional rows simply by adding information to the two-dimensional array that represents the row or rows that you want to add.</span></span>

## <a name="add-a-row-or-rows-to-an-excel-workbook-with-a-single-rest-request"></a><span data-ttu-id="57311-110">Agregar una fila o filas a un libro de Excel con una sola solicitud REST</span><span class="sxs-lookup"><span data-stu-id="57311-110">Add a row or rows to an Excel workbook with a single REST request</span></span>

<span data-ttu-id="57311-111">La API de REST de Excel requiere que realice una llamada POST a un cuerpo de solicitud simple al extremo de REST que representa la colección de filas de un libro de Excel.</span><span class="sxs-lookup"><span data-stu-id="57311-111">The Excel REST API requires you to POST a simple request body to the REST endpoint that represents the row collection of an Excel workbook.</span></span> <span data-ttu-id="57311-112">Si trabaja con un bloc de notas en la carpeta raíz de la cuenta de OneDrive del usuario que ha iniciado sesión, el extremo de REST tendrá un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="57311-112">If you're working with a notebook in the root folder of the signed-in user's OneDrive account, the REST endpoint will look like this:</span></span>

`https://graph.microsoft.com/v1.0/me/drive/root:/demo.xlsx:/workbook/tables/Table1/rows/add`

<span data-ttu-id="57311-113">Para obtener más información sobre cómo llegar a los archivos en carpetas de OneDrive, consulte el [tipo de recurso DriveItem](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/driveitem) en la documentación de referencia.</span><span class="sxs-lookup"><span data-stu-id="57311-113">For more information about how to reach files in OneDrive folders, see the [DriveItem resource type](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/driveitem) in our reference documentation.</span></span>

> <span data-ttu-id="57311-114">**Nota:** puede buscar en la colección de fila existente del libro haciendo una solicitud GET en la parte de la ruta que termina en `/rows`.</span><span class="sxs-lookup"><span data-stu-id="57311-114">**Note:** You can look at the existing row collection of the workbook by making a GET request to the part of the path that ends at `/rows`.</span></span>

<span data-ttu-id="57311-115">El cuerpo de POST tiene este aspecto:</span><span class="sxs-lookup"><span data-stu-id="57311-115">The POST body looks like this:</span></span>

`{
  "index": null,
  "values": [
    ['alex darrow', 'adarrow@tenant.onmicrosoft.com']
  ]
}`

<span data-ttu-id="57311-116">El valor del primer parámetro `index` especifica la posición relativa de la fila que se va a agregar a la matriz de filas con índice cero.</span><span class="sxs-lookup"><span data-stu-id="57311-116">The value of the first `index` parameter specifies the relative position of the row that you're adding to the zero-indexed array of rows.</span></span> <span data-ttu-id="57311-117">Las filas situadas debajo de la fila insertada se desplazarán hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="57311-117">Rows below the inserted row will be shifted downwards.</span></span> <span data-ttu-id="57311-118">El parámetro `null` indica que la nueva fila se agrega al final.</span><span class="sxs-lookup"><span data-stu-id="57311-118">The `null` parameter indicates that the new row will be added to the end.</span></span>

<span data-ttu-id="57311-119">El valor del segundo parámetro `values` es una matriz de cadena bidimensional que contiene los valores sin formato de cada fila que desea agregar.</span><span class="sxs-lookup"><span data-stu-id="57311-119">The value of the second `values` parameter is a two-dimensional string array that contains the unformatted values of each row that you want to add.</span></span> <span data-ttu-id="57311-120">La matriz en la muestra contiene solo una fila, pero puede agregar más filas agregando más matrices de cadenas.</span><span class="sxs-lookup"><span data-stu-id="57311-120">The array in the sample contains only one row, but you can add more rows by adding more string arrays.</span></span>

<span data-ttu-id="57311-121">Puede probar esta consulta con su cuenta de OneDrive cargando el archivo demo.xlsx a su carpeta raíz de OneDrive y ejecutando la consulta en el [Probador de Microsoft Graph](https://developer.microsoft.com/es-ES/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="57311-121">You can test this query with your own OneDrive account by uploading the demo.xlsx file to your OneDrive root folder and executing this query on the [Microsoft Graph Explorer](https://developer.microsoft.com/es-ES/graph/graph-explorer).</span></span>

<span data-ttu-id="57311-122">Eso es todo lo que necesita saber para poder escribir datos en un libro de Excel.</span><span class="sxs-lookup"><span data-stu-id="57311-122">That is all you need to know in order to write data to an Excel workbook.</span></span> <span data-ttu-id="57311-123">Necesitará saber cómo crear y realizar la solicitud en su propio marco y las muestras de inicio de Excel muestran tres maneras diferentes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="57311-123">You do need to know how to construct and make the request in your own framework, and the Excel starter samples demonstrate three separate ways of doing this.</span></span>

## <a name="add-a-row-or-rows-to-an-excel-workbook-in-aspnet"></a><span data-ttu-id="57311-124">Agregar una fila o filas en un libro de Excel en ASP.NET</span><span class="sxs-lookup"><span data-stu-id="57311-124">Add a row or rows to an Excel workbook in ASP.NET</span></span>

<span data-ttu-id="57311-125">Encontrará el código de ASP.NET que crea y envía la solicitud en los archivos [GraphResources.cs](https://github.com/microsoftgraph/aspnet-excelstarter-sample/blob/master/Microsoft%20Graph%20Excel%20REST%20ASPNET/Models/GraphResources.cs) y [GraphService.cs](https://github.com/microsoftgraph/aspnet-excelstarter-sample/blob/master/Microsoft%20Graph%20Excel%20REST%20ASPNET/Models/GraphService.cs) de la [Muestra de inicio de Excel de Microsoft Graph para ASP.NET 4.6](https://github.com/microsoftgraph/aspnet-excelstarter-sample).</span><span class="sxs-lookup"><span data-stu-id="57311-125">You'll find the ASP.NET code that constructs and sends the request in the [GraphResources.cs](https://github.com/microsoftgraph/aspnet-excelstarter-sample/blob/master/Microsoft%20Graph%20Excel%20REST%20ASPNET/Models/GraphResources.cs) and [GraphService.cs](https://github.com/microsoftgraph/aspnet-excelstarter-sample/blob/master/Microsoft%20Graph%20Excel%20REST%20ASPNET/Models/GraphService.cs) files of the [Microsoft Graph Excel Starter Sample for ASP.NET 4.6](https://github.com/microsoftgraph/aspnet-excelstarter-sample).</span></span>

<span data-ttu-id="57311-126">El archivo `GraphResources.cs` proporciona una clase auxiliar para encapsular los datos de usuario que está recuperando de Microsoft Graph y el cuerpo de la solicitud que usará cuando escriba en el libro.</span><span class="sxs-lookup"><span data-stu-id="57311-126">The `GraphResources.cs` file provides a helper class for encapsulating both the user data you're retrieving from Microsoft Graph and the request body that you'll use when you write to your workbook.</span></span>

    public class UserInfo
    {
        public string Name { get; set; }
        public string Address { get; set; }

    }

    public class UserInfoRequest
    {
        public string index { get; set; }
        public string[][] values { get; set; }
    }

<span data-ttu-id="57311-127">La clase `GraphService.cs` contiene un método `AddInfoToExcel` que rellena estas clases, serializa la información de la solicitud en un objeto JSON y después pasa ese objeto como el cuerpo de la solicitud POST.</span><span class="sxs-lookup"><span data-stu-id="57311-127">The `GraphService.cs` class contains an `AddInfoToExcel` method that populates these classes, serializes the request information into a JSON object, and then passes that object as the POST request body.</span></span>

        public async Task<string> AddInfoToExcel(string accessToken, string name, string address)
        {
            string endpoint = "https://graph.microsoft.com/v1.0/me/drive/root:/demo.xlsx:/workbook/tables/Table1/rows/add";
            using (var client = new HttpClient())
            {
                using (var request = new HttpRequestMessage(HttpMethod.Post, endpoint))
                {
                    // Populate UserInfoRequest object
                    string[] userInfo = { name, address  };
                    string[][] userInfoArray = { userInfo };
                    UserInfoRequest userInfoRequest = new UserInfoRequest();
                    userInfoRequest.index = null;
                    userInfoRequest.values = userInfoArray;

                    // Serialize the information in the UserInfoRequest object
                    string jsonBody = JsonConvert.SerializeObject(userInfoRequest);
                    request.Headers.Accept.Add(new MediaTypeWithQualityHeaderValue("application/json"));
                    request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", accessToken);
                    request.Content = new StringContent(jsonBody, Encoding.UTF8, "application/json");

                    using (var response = await client.SendAsync(request))
                    {
                        if (response.IsSuccessStatusCode)
                        {
                            return Resource.Graph_UploadToExcel_Success_Result;
                        }
                        return response.ReasonPhrase;
                    }
                }
            }
        }

## <a name="add-a-row-or-rows-to-an-excel-workbook-in-angular"></a><span data-ttu-id="57311-128">Agregar una fila o filas en un libro de Excel en Angular</span><span class="sxs-lookup"><span data-stu-id="57311-128">Add a row or rows to an Excel workbook in Angular</span></span>

<span data-ttu-id="57311-129">Encontrará el código de Angular que crea y envía la solicitud el [archivo home.service.ts](https://github.com/microsoftgraph/angular-excelstarter-sample/blob/master/src/app/home/home.service.ts) de la [muestra de inicio de Excel de Microsoft Graph para Angular](https://github.com/microsoftgraph/angular-excelstarter-sample).</span><span class="sxs-lookup"><span data-stu-id="57311-129">You'll find the Angular code that constructs and sends the request in the [home.service.ts file](https://github.com/microsoftgraph/angular-excelstarter-sample/blob/master/src/app/home/home.service.ts) of the [Microsoft Graph Excel Starter Sample for Angular](https://github.com/microsoftgraph/angular-excelstarter-sample).</span></span>

<span data-ttu-id="57311-130">Puesto que este ejemplo usa TypeScript, aprovecha la [biblioteca de cliente de JavaScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-sdk-javascript) y los [tipos de TypeScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-typescript-typings).</span><span class="sxs-lookup"><span data-stu-id="57311-130">Since this sample uses TypeScript, it takes advantage of the [Microsoft Graph JavaScript Client Library](https://github.com/microsoftgraph/msgraph-sdk-javascript) and the [ Microsoft Graph TypeScript Types](https://github.com/microsoftgraph/msgraph-typescript-typings).</span></span>

<span data-ttu-id="57311-131">La función `addInfoToExcel` en el archivo `home.service.ts` crea la matriz de cadena bidimensional y el cuerpo de la solicitud que contiene la matriz.</span><span class="sxs-lookup"><span data-stu-id="57311-131">The `addInfoToExcel` function in the `home.service.ts` file constructs the two-dimensional string array and the request body that contains the array.</span></span> <span data-ttu-id="57311-132">Después usa la biblioteca de cliente de JavaScript de Microsoft Graph para crear y enviar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="57311-132">It then uses the Microsoft Graph JavaScript Client Library to construct and send the request.</span></span> <span data-ttu-id="57311-133">La respuesta regresa en forma de una promesa.</span><span class="sxs-lookup"><span data-stu-id="57311-133">The response comes back in the form of a Promise.</span></span>

      addInfoToExcel(user: MicrosoftGraph.User) {
        const userInfo = [];
        const userEmail = user.mail || user.userPrincipalName;    
        userInfo.push([user.displayName, userEmail]);

        const userInfoRequestBody = {
          index: null,
          values: userInfo
        };   

        const body = JSON.stringify(userInfoRequestBody);

        var client = this.getClient();
        var url = `${this.url}/me/drive/root:/${this.file}:/workbook/tables/${this.table}/rows/add`
        return Observable.fromPromise(client
        .api(url)
        .post(body)
        );
      }

## <a name="add-a-row-or-rows-to-an-excel-workbook-in-react"></a><span data-ttu-id="57311-134">Agregar una fila o filas en un libro de Excel en React</span><span class="sxs-lookup"><span data-stu-id="57311-134">Add a row or rows to an Excel workbook in React</span></span>

<span data-ttu-id="57311-135">Encontrará el código de que crea y envía la solicitud el [archivo home.js](https://github.com/microsoftgraph/react-excelstarter-sample/blob/master/src/home/home.js) de la [Muestra de inicio de Excel de Microsoft Graph para React](https://github.com/microsoftgraph/react-excelstarter-sample).</span><span class="sxs-lookup"><span data-stu-id="57311-135">You'll find the code that constructs and sends the request in the [home.js file](https://github.com/microsoftgraph/react-excelstarter-sample/blob/master/src/home/home.js) of the [Microsoft Graph Excel Starter Sample for React](https://github.com/microsoftgraph/react-excelstarter-sample).</span></span>

<span data-ttu-id="57311-136">La función `onWriteToExcel` crea la matriz de cadena bidimensional y la pasa como el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="57311-136">The `onWriteToExcel` function constructs the two-dimensional string array and passes it as the request body.</span></span> <span data-ttu-id="57311-137">Usa [axios](https://www.npmjs.com/package/axios) para realizar la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="57311-137">It uses [axios](https://www.npmjs.com/package/axios) to make the HTTP request.</span></span>

      onWriteToExcel() {
        const { token, me } = this.state;

        const myEmailAddress = me.mail || me.userPrincipalName;
        const values = [];

        values.push([me.displayName, myEmailAddress]);

        axios
          .post('https://graph.microsoft.com/v1.0/me/drive/root:/demo.xlsx:/workbook/tables/Table1/rows/add',
            { index: null, values },
            { headers: { Authorization: `Bearer ${token}` }}
          )
          .then(res => {
                          console.log(res);
                          const successMessage = "Successfully wrote your data to demo.xlsx!";
                          this.setState ({ successMessage });
                         })
          .catch(err => console.error(err));
      }

##<a name="see-also"></a><span data-ttu-id="57311-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="57311-138">See also</span></span>

* [<span data-ttu-id="57311-139">Administrar sesiones de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="57311-139">Manage sessions in Excel with Microsoft Graph</span></span>](excel-manage-sessions.md)
* [<span data-ttu-id="57311-140">Usar funciones de libro de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="57311-140">Use workbook functions in Excel with Microsoft Graph</span></span>](excel-use-functions.md)
* [<span data-ttu-id="57311-141">Actualizar el formato de un rango en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="57311-141">Update a range’s format in Excel with Microsoft Graph</span></span>](excel-update-range-format.md)
* [<span data-ttu-id="57311-142">Mostrar una imagen del gráfico en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="57311-142">Display a chart image in Excel with Microsoft Graph</span></span>](excel-display-chart-image.md)
* [<span data-ttu-id="57311-143">Usar la API de REST de Excel</span><span class="sxs-lookup"><span data-stu-id="57311-143">Use the Excel REST API</span></span>](../api-reference/v1.0/resources/excel.md)    
