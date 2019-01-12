---
title: Escribir datos en un libro de Excel con Microsoft Graph
description: p = excelstarter).
localization_priority: Priority
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 234130a8fa56dfdc078c694069a9fe879140d27f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954886"
---
# <a name="write-data-to-an-excel-workbook-with-microsoft-graph"></a>Escribir datos en un libro de Excel con Microsoft Graph

La API de REST de Excel proporciona una forma sencilla, independiente de la plataforma para cargar información en un libro de Excel. Este tema muestra cómo escribir conjuntos de datos simples en un libro de Excel en tres marcos de desarrollo web: ASP.NET, Angular y React. Puede mirar los ejemplos de código destacados en este tema visitando las [muestras de inicio de Excel de Microsoft Graph en GitHub](https://github.com/microsoftgraph?utf8=%E2%9C%93&q=excelstarter).

> **Nota:** los tres ejemplos escriben datos en un libro de Excel denominado **demo.xlxs**. Le proporcionan este libro para que pueda cargarlo en su propio OneDrive, pero también puede usar Microsoft Graph para cargar archivos en OneDrive. Si le interesa obtener información sobre las llamadas de REST que necesita cargar un archivo de cualquier tipo a la carpeta raíz de OneDrive, consulte el [ejemplo de lista de tareas pendientes de ASP.NET de la API de REST de Excel de Microsoft Graph](https://github.com/microsoftgraph/aspnet-todo-rest-sample).

Las tres muestras de ejemplo de Excel hacen lo mismo: recuperar el nombre y la dirección del usuario que ha iniciado sesión y agregar los dos elementos de información a una nueva fila en el libro **demo.xlsx**. Puede modificar las muestras para agregar más filas agregando información a la matriz bidimensional que representa la fila o filas que desea agregar.

## <a name="add-a-row-or-rows-to-an-excel-workbook-with-a-single-rest-request"></a>Agregar una fila o filas a un libro de Excel con una sola solicitud REST

La API de REST de Excel requiere que realice una llamada POST a un cuerpo de solicitud simple al extremo de REST que representa la colección de filas de un libro de Excel. Si trabaja con un bloc de notas en la carpeta raíz de la cuenta de OneDrive del usuario que ha iniciado sesión, el extremo de REST tendrá un aspecto similar al siguiente:

`https://graph.microsoft.com/v1.0/me/drive/root:/demo.xlsx:/workbook/tables/Table1/rows/add`

Para obtener más información sobre cómo llegar a los archivos en carpetas de OneDrive, consulte el [tipo de recurso DriveItem](/graph/api/resources/driveitem?view=graph-rest-1.0) en la documentación de referencia.

> **Nota:** puede buscar en la colección de fila existente del libro haciendo una solicitud GET en la parte de la ruta que termina en `/rows`.

El cuerpo de POST tiene este aspecto:

`{
  "index": null,
  "values": [
    ['alex darrow', 'adarrow@tenant.onmicrosoft.com']
  ]
}`

El valor del primer parámetro `index` especifica la posición relativa de la fila que se va a agregar a la matriz de filas con índice cero. Las filas situadas debajo de la fila insertada se desplazarán hacia abajo. El parámetro `null` indica que la nueva fila se agrega al final.

El valor del segundo parámetro `values` es una matriz de cadena bidimensional que contiene los valores sin formato de cada fila que desea agregar. La matriz en la muestra contiene solo una fila, pero puede agregar más filas agregando más matrices de cadenas.

Puede probar esta consulta con su cuenta de OneDrive cargando el archivo demo.xlsx a su carpeta raíz de OneDrive y ejecutando la consulta en el [Probador de Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer).

Eso es todo lo que necesita saber para poder escribir datos en un libro de Excel. Necesitará saber cómo crear y realizar la solicitud en su propio marco y las muestras de inicio de Excel muestran tres maneras diferentes de hacerlo.

## <a name="add-a-row-or-rows-to-an-excel-workbook-in-aspnet"></a>Agregar una fila o filas en un libro de Excel en ASP.NET

Encontrará el código de ASP.NET que crea y envía la solicitud en los archivos [GraphResources.cs](https://github.com/microsoftgraph/aspnet-excelstarter-sample/blob/master/Microsoft%20Graph%20Excel%20REST%20ASPNET/Models/GraphResources.cs) y [GraphService.cs](https://github.com/microsoftgraph/aspnet-excelstarter-sample/blob/master/Microsoft%20Graph%20Excel%20REST%20ASPNET/Models/GraphService.cs) de la [Muestra de inicio de Excel de Microsoft Graph para ASP.NET 4.6](https://github.com/microsoftgraph/aspnet-excelstarter-sample).

El archivo `GraphResources.cs` proporciona una clase auxiliar para encapsular los datos de usuario que está recuperando de Microsoft Graph y el cuerpo de la solicitud que usará cuando escriba en el libro.

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

La clase `GraphService.cs` contiene un método `AddInfoToExcel` que rellena estas clases, serializa la información de la solicitud en un objeto JSON y después pasa ese objeto como el cuerpo de la solicitud POST.

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

## <a name="add-a-row-or-rows-to-an-excel-workbook-in-angular"></a>Agregar una fila o filas en un libro de Excel en Angular

Encontrará el código de Angular que crea y envía la solicitud el [archivo home.service.ts](https://github.com/microsoftgraph/angular-excelstarter-sample/blob/master/src/app/home/home.service.ts) de la [muestra de inicio de Excel de Microsoft Graph para Angular](https://github.com/microsoftgraph/angular-excelstarter-sample).

Puesto que este ejemplo usa TypeScript, aprovecha la [biblioteca de cliente de JavaScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-sdk-javascript) y los [tipos de TypeScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-typescript-typings).

La función `addInfoToExcel` en el archivo `home.service.ts` crea la matriz de cadena bidimensional y el cuerpo de la solicitud que contiene la matriz. Después usa la biblioteca de cliente de JavaScript de Microsoft Graph para crear y enviar la solicitud. La respuesta regresa en forma de una promesa.

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

## <a name="add-a-row-or-rows-to-an-excel-workbook-in-react"></a>Agregar una fila o filas en un libro de Excel en React

Encontrará el código de que crea y envía la solicitud el [archivo home.js](https://github.com/microsoftgraph/react-excelstarter-sample/blob/master/src/home/home.js) de la [Muestra de inicio de Excel de Microsoft Graph para React](https://github.com/microsoftgraph/react-excelstarter-sample).

La función `onWriteToExcel` crea la matriz de cadena bidimensional y la pasa como el cuerpo de la solicitud. Usa [axios](https://www.npmjs.com/package/axios) para realizar la solicitud HTTP.

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

##<a name="see-also"></a>Vea también

* [Administrar sesiones de Excel con Microsoft Graph](excel-manage-sessions.md)
* [Usar funciones de libro de Excel con Microsoft Graph](excel-use-functions.md)
* [Actualizar el formato de un rango en Excel con Microsoft Graph](excel-update-range-format.md)
* [Mostrar una imagen de gráfico de Excel con Microsoft Graph](excel-display-chart-image.md)
* [Usar la API de REST de Excel](/graph/api/resources/excel?view=graph-rest-1.0)    
