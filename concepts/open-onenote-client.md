---
title: Abrir el cliente de OneNote
description: 'Puede usar la propiedad **links** de una página o un bloc de notas para abrir una aplicación de OneNote en una página o bloc de notas determinado. '
ms.openlocfilehash: c82507243488777e557b18e599edb86b2ac15622
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092880"
---
# <a name="open-the-onenote-client"></a><span data-ttu-id="92689-103">Abrir el cliente de OneNote</span><span class="sxs-lookup"><span data-stu-id="92689-103">Open the OneNote client</span></span>

<span data-ttu-id="92689-104">Puede usar la propiedad **links** de una página o un bloc de notas para abrir una aplicación de OneNote en una página o bloc de notas determinado.</span><span class="sxs-lookup"><span data-stu-id="92689-104">You can use the **links** property of a page or notebook to open a OneNote application to a particular page or notebook.</span></span> 

<span data-ttu-id="92689-105">La propiedad **links** es un objeto JSON que contiene dos direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="92689-105">The **links** property is a JSON object that contains two URLs.</span></span> <span data-ttu-id="92689-106">Las direcciones URL abren la página o el bloc de notas en la aplicación cliente de OneNote o en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="92689-106">The URLs will open the page or notebook in the OneNote client application or in OneNote Online.</span></span>

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

- <span data-ttu-id="92689-107">**oneNoteClientUrl**</span><span class="sxs-lookup"><span data-stu-id="92689-107">**oneNoteClientUrl**</span></span> 

    - <span data-ttu-id="92689-108">Abre el cliente de OneNote si ya está instalado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92689-108">Opens the OneNote client if it is already installed on the device.</span></span> <span data-ttu-id="92689-109">Esta dirección URL incluye el prefijo *onenote*.</span><span class="sxs-lookup"><span data-stu-id="92689-109">This URL includes the *onenote* prefix.</span></span>
    - <span data-ttu-id="92689-110">Abre la versión específica del idioma si hay una instalada en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92689-110">Opens the language-specific version if one is installed on the device.</span></span> <span data-ttu-id="92689-111">En caso contrario, usa la configuración de idioma de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="92689-111">Otherwise, uses the platform language setting.</span></span>

- <span data-ttu-id="92689-112">**oneNoteWebUrl**</span><span class="sxs-lookup"><span data-stu-id="92689-112">**oneNoteWebUrl**</span></span> 

    - <span data-ttu-id="92689-113">Abre OneNote Online si es compatible con el explorador predeterminado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92689-113">Opens OneNote Online if the default browser on the device supports it.</span></span> 
    - <span data-ttu-id="92689-114">Usa la configuración de idioma del explorador</span><span class="sxs-lookup"><span data-stu-id="92689-114">Uses the browser language setting.</span></span>


<span data-ttu-id="92689-115">La API de OneNote devuelve la propiedad **links** en la respuesta HTTP para las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="92689-115">The OneNote API returns the **links** property in the HTTP response for the following operations:</span></span>

- <span data-ttu-id="92689-116">Cree una página enviando una solicitud [`POST pages`](/graph/api/section-post-pages?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="92689-116">Create a page by sending a [`POST pages`](/graph/api/section-post-pages?view=graph-rest-1.0) request.</span></span>

- <span data-ttu-id="92689-117">Cree un bloc de notas enviando una solicitud [`POST notebooks`](/graph/api/onenote-post-notebooks?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="92689-117">Create a notebook by sending a [`POST notebooks`](/graph/api/onenote-post-notebooks?view=graph-rest-1.0) request.</span></span>

- <span data-ttu-id="92689-118">Obtenga los metadatos de la página enviando una solicitud [`GET pages`](/graph/api/page-get?view=graph-rest-1.0) o [`GET pages/{id}`](/graph/api/page-get?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="92689-118">Get page metadata by sending a [`GET pages`](/graph/api/page-get?view=graph-rest-1.0) or [`GET pages/{id}`](/graph/api/page-get?view=graph-rest-1.0) request.</span></span>

- <span data-ttu-id="92689-119">Obtenga los metadatos del bloc de notas enviando una solicitud [`GET notebooks`](/graph/api/notebook-get?view=graph-rest-1.0) o [`GET notebooks/{id}`](/graph/api/notebook-get?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="92689-119">Get notebook metadata by sending a [`GET notebooks`](/graph/api/notebook-get?view=graph-rest-1.0) or [`GET notebooks/{id}`](/graph/api/notebook-get?view=graph-rest-1.0) request.</span></span>

<span data-ttu-id="92689-120">Los ejemplos siguientes muestran cómo comprobar el código de estado de la respuesta, analizar el JSON para extraer las direcciones URL y, después, abrir el cliente de OneNote.</span><span class="sxs-lookup"><span data-stu-id="92689-120">The following examples show how to check the status code of the response, parse the JSON to extract the URLs, and then open the OneNote client.</span></span>

## <a name="ios-example"></a><span data-ttu-id="92689-121">Ejemplo de iOS</span><span class="sxs-lookup"><span data-stu-id="92689-121">iOS example</span></span>

<span data-ttu-id="92689-122">En el ejemplo siguiente obtiene las direcciones URL de cliente de OneNote de la respuesta JSON.</span><span class="sxs-lookup"><span data-stu-id="92689-122">The following example gets the OneNote client URLs from the JSON response.</span></span> <span data-ttu-id="92689-123">Usa la biblioteca de AFNetworking (https://afnetworking.com/) para extraer las dos direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="92689-123">It uses the AFNetworking library (https://afnetworking.com/) to extract the two URLs.</span></span> <span data-ttu-id="92689-124">En el ejemplo, `created` es un puntero al objeto **ONSCPSStandardResponse** que se usa para almacenar los valores de respuesta y `responseObject` contiene el JSON analizado.</span><span class="sxs-lookup"><span data-stu-id="92689-124">In the example, `created` is a pointer to the **ONSCPSStandardResponse** object used to store the response values, and `responseObject` holds the parsed JSON.</span></span>

```objc
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

<br/>

<span data-ttu-id="92689-125">Después de analizar las direcciones URL de la respuesta, puede abrir OneNote mediante el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="92689-125">After you parse the URLs from the response, you can open OneNote by using the following code.</span></span> <span data-ttu-id="92689-126">Use `oneNoteClientUrl` para abrir el cliente de OneNote instalado o `oneNoteWebURL` para abrir OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="92689-126">Use `oneNoteClientUrl` to open the installed OneNote client or `oneNoteWebURL` to open OneNote Online.</span></span>

```objc
NSURL *url = [NSURL URLWithString:standardResponse.oneNoteWebUrl];
[[UIApplication sharedApplication] openURL:url];
```

## <a name="android-example"></a><span data-ttu-id="92689-127">Ejemplo de Android</span><span class="sxs-lookup"><span data-stu-id="92689-127">Android example</span></span>

<span data-ttu-id="92689-128">En primer lugar, compruebe si el código de estado es el correcto y después analice el JSON.</span><span class="sxs-lookup"><span data-stu-id="92689-128">First, check for the success status code, and then parse the JSON.</span></span> <span data-ttu-id="92689-129">El ejemplo supone que se ha enviado una solicitud POST, así que busca un código de estado `201 Created`.</span><span class="sxs-lookup"><span data-stu-id="92689-129">The example assumes a POST request was sent, so it checks for a `201 Created` status code.</span></span> <span data-ttu-id="92689-130">Si ha realizado una solicitud `GET`, busque un código de estado `200` en su lugar.</span><span class="sxs-lookup"><span data-stu-id="92689-130">If you made a `GET` request, check for a `200` status code instead.</span></span>

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

<br/>

<span data-ttu-id="92689-131">Mediante las propiedades de la respuesta, la aplicación puede abrir OneNote Online como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="92689-131">Using the response properties, your app can open OneNote Online, as shown in the following example.</span></span>

```java 
if (response.getResponseCode() == 201) {
    Uri uriUrl = Uri.parse(response.getOneNoteWebUrl);  
    Intent launchBrowser = new Intent(Intent.ACTION_VIEW, uriUrl); 
    startActivity(launchBrowser);
}
```

<br/>

<span data-ttu-id="92689-132">O bien, la aplicación puede abrir el cliente de OneNote en un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="92689-132">Or your app can open the OneNote client on an Android device.</span></span> <span data-ttu-id="92689-133">Cuando se usa la propiedad `oneNoteClientUrl`, debe delimitar las cadenas de GUID con llaves `{ }` antes de iniciar el intento.</span><span class="sxs-lookup"><span data-stu-id="92689-133">When using the `oneNoteClientUrl` property, you must surround the GUID strings with braces `{ }` before starting the Intent.</span></span> <span data-ttu-id="92689-134">En el siguiente ejemplo se indica cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="92689-134">The following example shows how to do that.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="92689-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="92689-135">See also</span></span>

- [<span data-ttu-id="92689-136">Obtener el contenido y la estructura de OneNote</span><span class="sxs-lookup"><span data-stu-id="92689-136">Get OneNote content and structure</span></span>](onenote-get-content.md)
- [<span data-ttu-id="92689-137">Crear páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="92689-137">Create OneNote pages</span></span>](onenote-create-page.md)