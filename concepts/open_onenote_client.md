# <a name="open-the-onenote-client"></a><span data-ttu-id="e8d0d-101">Abrir el cliente de OneNote</span><span class="sxs-lookup"><span data-stu-id="e8d0d-101">Open the Postman client.</span></span>

<span data-ttu-id="e8d0d-102">Puede usar la propiedad **links** de una página o un bloc de notas para abrir una aplicación de OneNote en una página o bloc de notas determinado.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-102">You can use the **links** property of a page or notebook to open a OneNote application to a particular page or notebook.</span></span> 

<span data-ttu-id="e8d0d-103">La propiedad **links** es un objeto JSON que contiene dos direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-103">The **links** property is a JSON object that contains two URLs.</span></span> <span data-ttu-id="e8d0d-104">Las direcciones URL abren la página o el bloc de notas en la aplicación cliente de OneNote o en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-104">The URLs will open the page or notebook in the OneNote client application or in OneNote Online.</span></span>

```json
{ 
    "links": {
        "oneNoteClientUrl": {
            "href": "onenote:https://..."
        },
        "oneNoteWebUrl": {
            "href": "https://..."
        }
    }
}
```

- <span data-ttu-id="e8d0d-105">**oneNoteClientUrl**: abre el cliente de OneNote si ya está instalado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-105">**oneNoteClientUrl** - Opens the OneNote client if it is already installed on the device.</span></span> <span data-ttu-id="e8d0d-106">Esta dirección URL incluye el prefijo *onenote*.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-106">This URL includes the *onenote* prefix.</span></span>
<span data-ttu-id="e8d0d-107">Abre la versión específica del idioma si hay una instalada en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-107">Opens the language-specific version if one is installed on the device.</span></span> <span data-ttu-id="e8d0d-108">En caso contrario, usa la configuración de idioma de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-108">Otherwise, uses the platform language setting.</span></span>
- <span data-ttu-id="e8d0d-109">**oneNoteWebUrl**: abre OneNote Online si es compatible con el explorador predeterminado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-109">**oneNoteWebUrl** - Opens OneNote Online if the default browser on the device supports it.</span></span> <span data-ttu-id="e8d0d-110">Usa la configuración de idioma del explorador</span><span class="sxs-lookup"><span data-stu-id="e8d0d-110">Uses the browser language setting.</span></span>


<span data-ttu-id="e8d0d-111">La API de OneNote devuelve la propiedad **links** en la respuesta HTTP para las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="e8d0d-111">The OneNote API returns the **links** property in the HTTP response for the following operations:</span></span>

- <span data-ttu-id="e8d0d-112">Crear una página mediante el envío de una solicitud [`POST pages`](../api-reference/v1.0/api/section_post_pages.md)</span><span class="sxs-lookup"><span data-stu-id="e8d0d-112">Create a page by sending a [`POST pages`](../api-reference/v1.0/api/section_post_pages.md) request</span></span>
- <span data-ttu-id="e8d0d-113">Crear un bloc de notas mediante el envío de una solicitud [`POST notebooks`](../api-reference/v1.0/api/onenote_post_notebooks.md)</span><span class="sxs-lookup"><span data-stu-id="e8d0d-113">Create a notebook by sending a [`POST notebooks`](../api-reference/v1.0/api/onenote_post_notebooks.md) request</span></span>
- <span data-ttu-id="e8d0d-114">Obtener los metadatos de la página mediante el envío de una solicitud [`GET pages`](../api-reference/v1.0/api/page_get.md) o [`GET pages/{id}`](../api-reference/v1.0/api/page_get.md)</span><span class="sxs-lookup"><span data-stu-id="e8d0d-114">Get page metadata by sending a [`GET pages`](../api-reference/v1.0/api/page_get.md) or [`GET pages/{id}`](../api-reference/v1.0/api/page_get.md) request</span></span>
- <span data-ttu-id="e8d0d-115">Obtener los metadatos del bloc de notas mediante el envío de una solicitud [`GET notebooks`](../api-reference/v1.0/api/notebook_get.md) o [`GET notebooks/{id}`](../api-reference/v1.0/api/notebook_get.md)</span><span class="sxs-lookup"><span data-stu-id="e8d0d-115">Get notebook metadata by sending a [`GET notebooks`](../api-reference/v1.0/api/notebook_get.md) or [`GET notebooks/{id}`](../api-reference/v1.0/api/notebook_get.md) request</span></span>

<span data-ttu-id="e8d0d-116">Los ejemplos siguientes muestran cómo comprobar el código de estado de la respuesta, analizar el JSON para extraer las direcciones URL y, después, abrir el cliente de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-116">The following examples show how to check the status code of the response, parse the JSON to extract the URLs, and then open the OneNote client.</span></span>

## <a name="ios-example"></a><span data-ttu-id="e8d0d-117">Ejemplo de iOS</span><span class="sxs-lookup"><span data-stu-id="e8d0d-117">iOS example</span></span>

<span data-ttu-id="e8d0d-118">En el ejemplo siguiente obtiene las direcciones URL de cliente de OneNote de la respuesta JSON.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-118">The following example gets the OneNote client URLs from the JSON response.</span></span> <span data-ttu-id="e8d0d-119">Usa la biblioteca de AFNetworking (http://afnetworking.com/) para extraer las dos direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-119">It uses the AFNetworking library (http://afnetworking.com/) to extract the two URLs.</span></span> <span data-ttu-id="e8d0d-120">En el ejemplo, `created` es un puntero al objeto ONSCPSStandardResponse uso para almacenar los valores de respuesta y `responseObject` contiene el JSON analizado.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-120">The following example gets the oncshort client URLs from the JSON response. It uses the AFNetworking library (http://afnetworking.com/http://afnetworking.com/) to extract the two URLs. In the example, created`created` is a pointer to the ONSCPSStandardResponse`responseObject` object used to store the response values, and responseObject holds the parsed JSON.</span></span>

```objectivec
    /* Import the JSON library */
    #import "AFURLRequestSerialization.h"

    - (void)connectionDidFinishLoading:(NSURLConnection *)connection {
            if(delegate) {
                  int status = [returnResponse statusCode];
                  ONSCPSStandardResponse *standardResponse = nil;
                  if (status == 201) {
                        ONSCPSCreateSuccessResponse *created = 
                              [[ONSCPSCreateSuccessResponse alloc] init];
                        created.httpStatusCode = status;
                        NSError *jsonError;
                        NSDictionary *responseObject = 
                              [NSJSONSerialization JSONObjectWithData:returnData options:0 error:&jsonError];
                        if(responseObject && !jsonError) {
                              created.oneNoteClientUrl = ((NSDictionary *)
                                    ((NSDictionary *)responseObject[@"links"])[@"oneNoteClientUrl"])[@"href"];
                              created.oneNoteWebUrl = ((NSDictionary *)
                                    ((NSDictionary *)responseObject[@"links"])[@"oneNoteWebUrl"])[@"href"];
                        }
                  standardResponse = created;
                  }
                  else {
                        ONSCPSStandardErrorResponse *error = [[ONSCPSStandardErrorResponse alloc] init];
                        error.httpStatusCode = status;
                        error.message = [[NSString alloc] initWithData:returnData 
                              encoding:NSUTF8StringEncoding];
                        standardResponse = error;
                  }
                  // Send the response back to the client.
                  if (standardResponse) {
                        [delegate exampleServiceActionDidCompleteWithResponse: standardResponse];
                  }
            }
      }
``` 

<span data-ttu-id="e8d0d-121">Después de analizar las direcciones URL de la respuesta, puede abrir OneNote mediante el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-121">After you parse the URLs from the response, you can open OneNote by using the following code.</span></span> <span data-ttu-id="e8d0d-122">Use `oneNoteClientUrl` para abrir el cliente de OneNote instalado o `oneNoteWebURL` para abrir OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-122">Use `oneNoteClientUrl` to open the installed OneNote client or `oneNoteWebURL` to open OneNote Online.</span></span>

```objectivec
NSURL *url = [NSURL URLWithString:standardResponse.oneNoteWebUrl];
[[UIApplication sharedApplication] openURL:url];
```

## <a name="android-example"></a><span data-ttu-id="e8d0d-123">Ejemplo de Android</span><span class="sxs-lookup"><span data-stu-id="e8d0d-123">Android example</span></span>

<span data-ttu-id="e8d0d-124">En primer lugar, compruebe si el código de estado es el correcto y, después, analice el JSON.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-124">First, check for the success status code and then parse the JSON.</span></span> <span data-ttu-id="e8d0d-125">El ejemplo supone que se ha enviado una solicitud POST, así que busca un código de estado `201 Created`.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-125">The example assumes a POST request was sent, so it checks for a `201 Created` status code.</span></span> <span data-ttu-id="e8d0d-126">Si ha realizado una solicitud `GET`, busque un código de estado `200` en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-126">If you made a `GET` request, check for a `200` status code instead.</span></span>

```java
public ApiResponse getResponse() throws Exception {
    /* Get the HTTP response code and message from the connection object */
    int responseCode = mUrlConnection.getResponseCode();
    String responseMessage = mUrlConnection.getResponseMessage();
    String responseBody = null;

    /* Get the response if the new page was created successfully. */
    if ( responseCode == 201) {
        InputStream is = mUrlConnection.getInputStream();

        /* Verify that this byte array is big enough. */
        byte[] b1 = new byte[1024];
        StringBuffer buffer = new StringBuffer();

        /* Copy the body of the response into the new string. */
        /* Make sure the buffer is big enough. */
        while ( is.read(b1) != -1)
            buffer.append(new String(b1));

      /* When the returned data is complete, close the connection 
         and convert the byte array into a string. */
        mUrlConnection.disconnect();
        responseBody =  buffer.toString();
    }

    /* Create a new JSON object, and an object to hold the response URLs. */
    JSONObject responseObject = null;
    ApiResponse response = new ApiResponse();
    try {

        /* Store and verify the HTTP response code. */
        response.setResponseCode(responseCode);
        response.setResponseMessage(responseMessage);
        if ( responseCode == 201) {

            /* Retrieve the two URLs from the links property. */
            responseObject = new JSONObject(responseBody);
            String clientUrl = responseObject.getJSONObject(
                "links").getJSONObject("oneNoteClientUrl").getString("href");
            String webUrl = responseObject.getJSONObject(
                "links").getJSONObject("oneNoteWebUrl").getString("href");
            response.setOneNoteClientUrl(clientUrl);
            response.setOneNoteWebUrl(webUrl);
        }
    } catch (JSONException ex) {

        /* If the JSON was malformed or incomplete... */
        String msg = ex.getMessage();
        msg = msg;
    }
    return response;
}
```

<span data-ttu-id="e8d0d-127">Mediante las propiedades de la respuesta, la aplicación puede abrir OneNote Online como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-127">Using the response properties, your app can open OneNote Online, as shown in the following example.</span></span>

```java 
if (response.getResponseCode() == 201) {
    Uri uriUrl = Uri.parse(response.getOneNoteWebUrl);  
    Intent launchBrowser = new Intent(Intent.ACTION_VIEW, uriUrl); 
    startActivity(launchBrowser);
}
```
 
<span data-ttu-id="e8d0d-128">O bien, la aplicación puede abrir el cliente de OneNote en un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-128">Or your app can open the OneNote client on an Android device.</span></span> <span data-ttu-id="e8d0d-129">Cuando se usa la propiedad `oneNoteClientUrl`, debe delimitar las cadenas de GUID con llaves `{ }` antes de iniciar el intento.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-129">When using the `oneNoteClientUrl` property, you must surround the GUID strings with braces `{ }` before starting the Intent.</span></span> <span data-ttu-id="e8d0d-130">En el siguiente ejemplo se indica cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="e8d0d-130">The following example shows how to:</span></span>

```java 
if (response.getResponseCode() == 201) {

    // Get the URL from the OneNote API JSON response.
    String onenoteClientUrl = obtainClientLinkFromJSONResponse();
    String androidClientUrl = 
        onenoteClientUrl.replaceAll(
            "=([0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12})&",
            "={$1}&");

    // Open the URL: Open the newly created OneNote page.
    Uri uriUrl = Uri.parse(androidClientUrl);  
    Intent launchBrowser = new Intent(Intent.ACTION_VIEW, uriUrl); 
    startActivity(launchBrowser);
}
```

## <a name="see-also"></a><span data-ttu-id="e8d0d-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="e8d0d-131">See also</span></span>

- [<span data-ttu-id="e8d0d-132">Obtener el contenido y la estructura de OneNote</span><span class="sxs-lookup"><span data-stu-id="e8d0d-132">Get OneNote content and structure</span></span>](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-get-content)
- [<span data-ttu-id="e8d0d-133">Crear páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="e8d0d-133">Create OneNote pages</span></span>](../api-reference/v1.0/api/section_post_pages.md)