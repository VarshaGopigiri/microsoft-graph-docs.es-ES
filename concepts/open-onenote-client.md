---
title: Abrir el cliente de OneNote
description: 'Puede usar la propiedad **links** de una página o un bloc de notas para abrir una aplicación de OneNote en una página o bloc de notas determinado. '
author: Jewan-microsoft
localization_priority: Normal
ms.openlocfilehash: 21f6d07c4a32f3e25c715172a2d18aa09c042920
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858348"
---
# <a name="open-the-onenote-client"></a>Abrir el cliente de OneNote

Puede usar la propiedad **links** de una página o un bloc de notas para abrir una aplicación de OneNote en una página o bloc de notas determinado. 

La propiedad **links** es un objeto JSON que contiene dos direcciones URL. Las direcciones URL abren la página o el bloc de notas en la aplicación cliente de OneNote o en OneNote Online.

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

- **oneNoteClientUrl** 

    - Abre el cliente de OneNote si ya está instalado en el dispositivo. Esta dirección URL incluye el prefijo *onenote*.
    - Abre la versión específica del idioma si hay una instalada en el dispositivo. En caso contrario, usa la configuración de idioma de la plataforma.

- **oneNoteWebUrl** 

    - Abre OneNote Online si es compatible con el explorador predeterminado del dispositivo. 
    - Usa la configuración de idioma del explorador


La API de OneNote devuelve la propiedad **links** en la respuesta HTTP para las siguientes operaciones:

- Cree una página enviando una solicitud [`POST pages`](/graph/api/section-post-pages?view=graph-rest-1.0).

- Cree un bloc de notas enviando una solicitud [`POST notebooks`](/graph/api/onenote-post-notebooks?view=graph-rest-1.0).

- Obtenga los metadatos de la página enviando una solicitud [`GET pages`](/graph/api/page-get?view=graph-rest-1.0) o [`GET pages/{id}`](/graph/api/page-get?view=graph-rest-1.0).

- Obtenga los metadatos del bloc de notas enviando una solicitud [`GET notebooks`](/graph/api/notebook-get?view=graph-rest-1.0) o [`GET notebooks/{id}`](/graph/api/notebook-get?view=graph-rest-1.0).

Los ejemplos siguientes muestran cómo comprobar el código de estado de la respuesta, analizar el JSON para extraer las direcciones URL y, después, abrir el cliente de OneNote.

## <a name="ios-example"></a>Ejemplo de iOS

En el ejemplo siguiente obtiene las direcciones URL de cliente de OneNote de la respuesta JSON. Usa la biblioteca de AFNetworking (https://afnetworking.com/) para extraer las dos direcciones URL. En el ejemplo, `created` es un puntero al objeto **ONSCPSStandardResponse** que se usa para almacenar los valores de respuesta y `responseObject` contiene el JSON analizado.

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

Después de analizar las direcciones URL de la respuesta, puede abrir OneNote mediante el código siguiente. Use `oneNoteClientUrl` para abrir el cliente de OneNote instalado o `oneNoteWebURL` para abrir OneNote Online.

```objc
NSURL *url = [NSURL URLWithString:standardResponse.oneNoteWebUrl];
[[UIApplication sharedApplication] openURL:url];
```

## <a name="android-example"></a>Ejemplo de Android

En primer lugar, compruebe si el código de estado es el correcto y después analice el JSON. El ejemplo supone que se ha enviado una solicitud POST, así que busca un código de estado `201 Created`. Si ha realizado una solicitud `GET`, busque un código de estado `200` en su lugar.

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

Mediante las propiedades de la respuesta, la aplicación puede abrir OneNote Online como se muestra en el ejemplo siguiente.

```java 
if (response.getResponseCode() == 201) {
    Uri uriUrl = Uri.parse(response.getOneNoteWebUrl);  
    Intent launchBrowser = new Intent(Intent.ACTION_VIEW, uriUrl); 
    startActivity(launchBrowser);
}
```

<br/>

O bien, la aplicación puede abrir el cliente de OneNote en un dispositivo Android. Cuando se usa la propiedad `oneNoteClientUrl`, debe delimitar las cadenas de GUID con llaves `{ }` antes de iniciar el intento. En el siguiente ejemplo se indica cómo hacerlo.

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

## <a name="see-also"></a>Ver también

- [Obtener el contenido y la estructura de OneNote](onenote-get-content.md)
- [Crear páginas de OneNote](onenote-create-page.md)
