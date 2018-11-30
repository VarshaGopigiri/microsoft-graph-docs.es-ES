---
title: Enviar comando de dispositivo
description: 'Esta API permite capacidades de Roma de proyecto a un dispositivo asociado con una cuenta de Microsoft de comando. Después de realizar una llamada GET en `me/devices`, pase el identificador del dispositivo para emitir un comando al dispositivo. Se admiten dos tipos de comandos: LaunchURI y AppServices. Si está utilizando LaunchURI, especifique los parámetros de *tipo* y la *carga* . Para una llamada AppService, especifique el '
ms.openlocfilehash: bf330ab1234ef6ce22c6a43711621827b628a7ac
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087087"
---
# <a name="send-device-command"></a><span data-ttu-id="3b796-107">Enviar comando de dispositivo</span><span class="sxs-lookup"><span data-stu-id="3b796-107">Send device command</span></span>

> <span data-ttu-id="3b796-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b796-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b796-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b796-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3b796-110">Esta API permite capacidades de Roma de proyecto a un dispositivo asociado con una cuenta de Microsoft de comando.</span><span class="sxs-lookup"><span data-stu-id="3b796-110">This API enables Project Rome capabilities to command a device associated with a Microsoft account.</span></span> <span data-ttu-id="3b796-111">Después de realizar una llamada GET en `me/devices`, pase el identificador del dispositivo para emitir un comando al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b796-111">After doing a GET call on `me/devices`, pass in the ID of the device to issue a command to your device.</span></span> <span data-ttu-id="3b796-112">Se admiten dos tipos de comandos: LaunchURI y AppServices.</span><span class="sxs-lookup"><span data-stu-id="3b796-112">Two types of commands are supported: LaunchURI and AppServices.</span></span> <span data-ttu-id="3b796-113">Si está utilizando LaunchURI, especifique los parámetros de *tipo* y la *carga* .</span><span class="sxs-lookup"><span data-stu-id="3b796-113">If you're using LaunchURI, specify the *type* and *payload* parameters.</span></span> <span data-ttu-id="3b796-114">Para una llamada AppService, especifique el *tipo de* *carga*, *packageFamilyName*, *appServiceName* los parámetros y.</span><span class="sxs-lookup"><span data-stu-id="3b796-114">For an AppService call, specify the *type*, *payload*, *packageFamilyName*, and *appServiceName* parameters.</span></span>

## <a name="permissions"></a><span data-ttu-id="3b796-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="3b796-115">Permissions</span></span>

<span data-ttu-id="3b796-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3b796-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="3b796-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3b796-118">Permission type</span></span>      | <span data-ttu-id="3b796-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3b796-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3b796-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3b796-120">Delegated (work or school account)</span></span> | <span data-ttu-id="3b796-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b796-121">Not supported.</span></span>    |
|<span data-ttu-id="3b796-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3b796-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3b796-123">Device.Command</span><span class="sxs-lookup"><span data-stu-id="3b796-123">Device.Command</span></span>    |
|<span data-ttu-id="3b796-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3b796-124">Application</span></span> | <span data-ttu-id="3b796-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b796-125">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3b796-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3b796-126">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST me/devices/{id}/commands
```

## <a name="request-headers"></a><span data-ttu-id="3b796-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b796-127">Request headers</span></span>


| <span data-ttu-id="3b796-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b796-128">Header</span></span> |<span data-ttu-id="3b796-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3b796-129">Value</span></span>
|:----|:------|
|<span data-ttu-id="3b796-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="3b796-130">Authorization</span></span>| <span data-ttu-id="3b796-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b796-p105">Bearer {token}. Required.</span></span> |
|<span data-ttu-id="3b796-133">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3b796-133">Accept</span></span> | <span data-ttu-id="3b796-134">application/json</span><span class="sxs-lookup"><span data-stu-id="3b796-134">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="3b796-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3b796-135">Request body</span></span>

<span data-ttu-id="3b796-136">En el cuerpo de la solicitud, proporcionar una representación JSON de las propiedades de comando.</span><span class="sxs-lookup"><span data-stu-id="3b796-136">In the request body, supply a JSON representation of the command properties.</span></span>

```json
{
  "type": "appService",
  "payload": "payload-JSON",
  "packageFamilyName": "packageFamilyName",
  "appServiceName": "appServiceName",
  "postbackURI": "postbackURI"
}
```

## <a name="response"></a><span data-ttu-id="3b796-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b796-137">Response</span></span>

```http
HTTP/1.1 201 OK
```

```json
{
  "id": "0",
  "status": "requesting",
  "type": "appService",
  "appServiceName": "appServiceName",
  "packageFamilyName": "packageFamilyName",
  "error": "null",
  "responsePayload": "null",
  "payload": "payload-JSON",
  "permissionTicket": "null",
  "postBackUri": "postbackURI"
}
```
## <a name="command-properties"></a><span data-ttu-id="3b796-138">Propiedades del comando</span><span class="sxs-lookup"><span data-stu-id="3b796-138">Command properties</span></span> 

|<span data-ttu-id="3b796-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="3b796-139">**Name**</span></span>|<span data-ttu-id="3b796-140">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3b796-140">**Type**</span></span>|<span data-ttu-id="3b796-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b796-141">**Description**</span></span>|
|:----|:------|:------|
|<span data-ttu-id="3b796-142">carga útil</span><span class="sxs-lookup"><span data-stu-id="3b796-142">payload</span></span> | <span data-ttu-id="3b796-143">Microsoft.Graph.JSON</span><span class="sxs-lookup"><span data-stu-id="3b796-143">microsoft.graph.json</span></span>| <span data-ttu-id="3b796-144">Carga de enviar a un servicio de aplicación o para iniciar un identificador URI en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b796-144">Payload to send to an app service or to launch a URI on a device.</span></span> |
|<span data-ttu-id="3b796-145">responsePayload</span><span class="sxs-lookup"><span data-stu-id="3b796-145">responsePayload</span></span> | <span data-ttu-id="3b796-146">Microsoft.Graph.JSON</span><span class="sxs-lookup"><span data-stu-id="3b796-146">microsoft.graph.json</span></span>| <span data-ttu-id="3b796-147">Carga devuelto desde el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="3b796-147">Payload returned from target device.</span></span> |
|<span data-ttu-id="3b796-148">postBackURI</span><span class="sxs-lookup"><span data-stu-id="3b796-148">postBackURI</span></span> | <span data-ttu-id="3b796-149">String</span><span class="sxs-lookup"><span data-stu-id="3b796-149">String</span></span> | <span data-ttu-id="3b796-150">Entrada de hacer una copia de URI que se va a enviar notificaciones posteriores de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="3b796-150">Post back URI to send subsequent notifications of updates.</span></span> |
|<span data-ttu-id="3b796-151">packageFamilyName</span><span class="sxs-lookup"><span data-stu-id="3b796-151">packageFamilyName</span></span> | <span data-ttu-id="3b796-152">String</span><span class="sxs-lookup"><span data-stu-id="3b796-152">String</span></span> | <span data-ttu-id="3b796-153">Nombre de familia de Windows paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b796-153">Windows Package Family Name of application.</span></span> |
|<span data-ttu-id="3b796-154">appServiceName</span><span class="sxs-lookup"><span data-stu-id="3b796-154">appServiceName</span></span> | <span data-ttu-id="3b796-155">String</span><span class="sxs-lookup"><span data-stu-id="3b796-155">String</span></span> | <span data-ttu-id="3b796-156">Nombre del servicio de aplicación definido por la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="3b796-156">Name of app service defined by the target application.</span></span> <span data-ttu-id="3b796-157">Requerido si iniciar un servicio de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b796-157">Required if launching an app service.</span></span> |
|<span data-ttu-id="3b796-158">type</span><span class="sxs-lookup"><span data-stu-id="3b796-158">type</span></span>| <span data-ttu-id="3b796-159">String</span><span class="sxs-lookup"><span data-stu-id="3b796-159">String</span></span> | <span data-ttu-id="3b796-160">LaunchURI o AppService.</span><span class="sxs-lookup"><span data-stu-id="3b796-160">LaunchURI or AppService.</span></span> |
|<span data-ttu-id="3b796-161">id</span><span class="sxs-lookup"><span data-stu-id="3b796-161">id</span></span>| <span data-ttu-id="3b796-162">String</span><span class="sxs-lookup"><span data-stu-id="3b796-162">String</span></span> | <span data-ttu-id="3b796-163">El identificador de un comando que se ha enviado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b796-163">The ID of a command that has been sent to the device.</span></span> |
|<span data-ttu-id="3b796-164">actionStatus</span><span class="sxs-lookup"><span data-stu-id="3b796-164">actionStatus</span></span> | <span data-ttu-id="3b796-165">String</span><span class="sxs-lookup"><span data-stu-id="3b796-165">String</span></span> | <span data-ttu-id="3b796-166">El [estado](get-device-command-status.md) de un comando.</span><span class="sxs-lookup"><span data-stu-id="3b796-166">The [status](get-device-command-status.md) of a command.</span></span> |
|<span data-ttu-id="3b796-167">error</span><span class="sxs-lookup"><span data-stu-id="3b796-167">error</span></span>| <span data-ttu-id="3b796-168">String</span><span class="sxs-lookup"><span data-stu-id="3b796-168">String</span></span>| <span data-ttu-id="3b796-169">Cualquier error asociado con la solicitud de la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="3b796-169">Any errors associated with the request from the target application.</span></span> |

## <a name="launch-uri-example"></a><span data-ttu-id="3b796-170">Ejemplo URI de inicio</span><span class="sxs-lookup"><span data-stu-id="3b796-170">Launch URI example</span></span>

<span data-ttu-id="3b796-171">Este es un ejemplo de una solicitud de LaunchURI; se iniciará un URI o una aplicación en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="3b796-171">Here is an example of a LaunchURI request; it will launch a URI or an application on the target device.</span></span> <span data-ttu-id="3b796-172">Para iniciar un URI o una aplicación, emitir una entrada con el identificador del dispositivo (obtenida de haciendo una llamada GET en `me/devices`).</span><span class="sxs-lookup"><span data-stu-id="3b796-172">To launch a URI or an app, issue a POST using the ID of the device (obtained from doing a GET call on `me/devices`).</span></span> <span data-ttu-id="3b796-173">Establezca los parámetros de *tipo* en *LaunchURI* y proporcione un valor URI como https://bing.com.</span><span class="sxs-lookup"><span data-stu-id="3b796-173">Set the *Type* parameters to *LaunchURI* and provide a URI value such as https://bing.com.</span></span>

#### <a name="request"></a><span data-ttu-id="3b796-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b796-174">Request</span></span>

<span data-ttu-id="3b796-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b796-175">The following is an example of the request.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "post_command"
} -->

```http

POST me/devices/{id}/commands
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8

{ "type" : "LaunchUri", "payload" : {"uri":"https://bing.com"}}

```

#### <a name="response"></a><span data-ttu-id="3b796-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b796-176">Response</span></span> 

<span data-ttu-id="3b796-177">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b796-177">The following is an example of the response.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": false,
  "@odata.type": "microsoft.graph.commandobject",
  "isCollection": true
} -->

```http
HTTP/1.1 201 OK

{
  "id": "0158355AD4D680CC4E2994CC009EFFD7337D1B...",
  "status": "requesting",
  "type": null,
  "appServiceName": null,
  "packageFamilyName": null,
  "error": null,
  "permissionTicket": null,
  "postBackUri": null,
  "payload": {
    "uri": "https://bing.com"
  }
}

```


## <a name="app-service-example"></a><span data-ttu-id="3b796-178">Ejemplo de aplicación de servicio</span><span class="sxs-lookup"><span data-stu-id="3b796-178">App service example</span></span>

<span data-ttu-id="3b796-179">Este es un ejemplo de la consulta a un servicio de aplicación en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b796-179">Here is an example of querying an app service on a device.</span></span> <span data-ttu-id="3b796-180">Para usar un servicio de aplicación debe realizar una llamada de entrada mediante el identificador del dispositivo (obtenida de haciendo una llamada GET en `me/devices`).</span><span class="sxs-lookup"><span data-stu-id="3b796-180">To use an app service you must do a POST call using the id of the device (obtained from doing a GET call on `me/devices`).</span></span> <span data-ttu-id="3b796-181">Para utilizar el ejemplo siguiente, debe instalar la [aplicación de Roma](https://aka.ms/romanapp) en su dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="3b796-181">To use the following example, you must install the [Rome app](https://aka.ms/romanapp) on your target device.</span></span>

<span data-ttu-id="3b796-182">En la llamada, se deben establecer varias propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="3b796-182">Several additional properties must be set in the call.</span></span> <span data-ttu-id="3b796-183">*Tipo* se debe establecer en *AppService*, *AppServiceName* debe establecerse en el nombre del servicio de aplicación definido en la aplicación, *PackageFamilyName* debe establecerse en el nombre de la familia de paquete definido en el manifiesto de la aplicación y *carga* contiene las claves y valores para el servicio que se está llamando dentro de la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="3b796-183">*Type* must be set to *AppService*, *AppServiceName* must be set to the name of the app service defined in the application, *PackageFamilyName* must be set to the package family name defined in the app manifest, and *Payload* holds the keys and values for the service you are calling within the target application.</span></span>

#### <a name="request"></a><span data-ttu-id="3b796-184">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b796-184">Request</span></span>

<!-- {
  "blockType": "ignored",
  "name": "post_command_2"
} -->

```http

POST me/devices/{id}/commands
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8

{
  "type" : "AppService",
  "appServiceName" : "com.microsoft.test.cdppingpongservice",
  "packageFamilyName" : "5085ShawnHenry.RomanTestApp_jsjw7knzsgcce",
  "payload" : {
    "Type":"Toast","Title":"Hello","Subtitle":"World!"}
  }
```

#### <a name="response"></a><span data-ttu-id="3b796-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b796-185">Response</span></span>

<span data-ttu-id="3b796-186">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b796-186">The following is an example of the response.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": false,
  "@odata.type": "microsoft.graph.commandobject",
  "isCollection": true
} -->

```http
HTTP/1.1 201 OK

{
  "id": "0158355AD4D680CC4E2994CC009EFFD7EADA8307E96FF1C8D19B..",
  "status": "requesting",
  "type": null,
  "appServiceName": "com.microsoft.randomnumbergenerator",
  "packageFamilyName": "Microsoft.SDKSamples.AppServicesProvider.CS_8wekyb3d8bbwe",
  "error": null,
  "permissionTicket": null,
  "postBackUri": null,
  "payload": {
    "Type": "Toast",
    "Title": "Hello",
    "Subtitle": "World!"
  }
}
```
