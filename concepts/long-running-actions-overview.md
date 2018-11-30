---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
ms.topic: conceptual
ms.openlocfilehash: 687ed04d3ddcede391e9f16a2046cb186a093323
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092816"
---
# <a name="working-with-long-running-actions-beta"></a><span data-ttu-id="3af74-101">Trabajar con acciones de larga duración (beta)</span><span class="sxs-lookup"><span data-stu-id="3af74-101">Working with long running actions (beta)</span></span>

> <span data-ttu-id="3af74-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3af74-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3af74-103">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3af74-103">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3af74-104">Algunas respuestas de API requieren un tiempo indeterminado para completarse.</span><span class="sxs-lookup"><span data-stu-id="3af74-104">Some API responses require indeterminate time to complete.</span></span>
<span data-ttu-id="3af74-105">En lugar de esperar hasta que se completa la acción antes de devolver una respuesta, Microsoft Graph puede usar un modelo de acciones de larga duración.</span><span class="sxs-lookup"><span data-stu-id="3af74-105">Instead of waiting until the action is complete before returning a response, Microsoft Graph may use a long running actions pattern.</span></span>
<span data-ttu-id="3af74-106">Este patrón le proporciona a su aplicación una espera para sondear actualizaciones de estado en una acción de larga duración, sin ninguna solicitud que espere a que se complete la acción.</span><span class="sxs-lookup"><span data-stu-id="3af74-106">This pattern provides your app a wait to poll for status updates on a long running action, without any request waiting for the action to complete.</span></span>

<span data-ttu-id="3af74-107">El modelo general sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="3af74-107">The general pattern follows these steps:</span></span>

1. <span data-ttu-id="3af74-108">La aplicación solicita una acción de larga duración mediante la API.</span><span class="sxs-lookup"><span data-stu-id="3af74-108">Your app requests a long running action via the API.</span></span> <span data-ttu-id="3af74-109">La API acepta la acción y devuelve una respuesta `202 Accepted` junto con un encabezado de ubicación para la dirección URL de la API para recuperar los informes de estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="3af74-109">The API accepts the action and returns a `202 Accepted` response along with a Location header for the API URL to retrieve action status reports.</span></span>
2. <span data-ttu-id="3af74-110">La aplicación solicita la dirección URL del informe de estado de la acción y recibe una respuesta [AsyncJobStatus](/graph/api/resources/asyncjobstatus?view=graph-rest-beta) con el progreso de la acción de larga duración</span><span class="sxs-lookup"><span data-stu-id="3af74-110">Your app requests the action status report URL and receives an [AsyncJobStatus](/graph/api/resources/asyncjobstatus?view=graph-rest-beta) response with the progress of the long running action.</span></span>
3. <span data-ttu-id="3af74-111">Se completa la acción de larga duración.</span><span class="sxs-lookup"><span data-stu-id="3af74-111">The long running action completes.</span></span> 
4. <span data-ttu-id="3af74-112">La aplicación vuelve a solicitar la dirección URL del informe de estado de la acción y recibe una respuesta [AsyncJobStatus](/graph/api/resources/asyncjobstatus?view=graph-rest-beta) en la que se muestra la finalización de la acción.</span><span class="sxs-lookup"><span data-stu-id="3af74-112">Your app requests the action status report URL again and receives an [AsyncJobStatus](/graph/api/resources/asyncjobstatus?view=graph-rest-beta) response showing the completion of the action.</span></span>

## <a name="initial-action-request"></a><span data-ttu-id="3af74-113">Solicitud de acción inicial</span><span class="sxs-lookup"><span data-stu-id="3af74-113">Initial action request</span></span>

<span data-ttu-id="3af74-114">Vamos a recorrer los pasos para obtener un ejemplo del escenario [copiar de DriveItem](/graph/api/driveitem-copy?view=graph-rest-beta).</span><span class="sxs-lookup"><span data-stu-id="3af74-114">Let's walk through the steps for an example [DriveItem Copy](/graph/api/driveitem-copy?view=graph-rest-beta) scenario.</span></span>
<span data-ttu-id="3af74-115">En este escenario, la aplicación solicita copiar una carpeta que contiene una gran cantidad de datos.</span><span class="sxs-lookup"><span data-stu-id="3af74-115">In this scenario, your app requests to copy a folder that contains a large amount of data.</span></span>
<span data-ttu-id="3af74-116">Esta solicitud probablemente tardará varios segundos en completarse ya que la cantidad de datos es grande.</span><span class="sxs-lookup"><span data-stu-id="3af74-116">This request will likely take several seconds to complete since the amount of data is large.</span></span>

<!-- { "blockType": "request", "name": "lro-copy-item-example", "scopes": "files.readwrite" } -->

```http
POST https://graph.microsoft.com/beta/me/drive/items/{folder-item-id}/copy
Content-Type: application/json

{
  "parentReference": {
    "path": "/drive/root:/Documents"
  },
  "name": "Copy of LargeFolder1"
}
```

<span data-ttu-id="3af74-117">La API responde que la acción se ha aceptado junto con la dirección URL para recuperar el estado de la acción de larga duración.</span><span class="sxs-lookup"><span data-stu-id="3af74-117">The API responds that the action was accepted and the URL for retrieving the status of the long running action.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 202 Accepted
Location: https://api.onedrive.com/monitor/4A3407B5-88FC-4504-8B21-0AABD3412717
```

<span data-ttu-id="3af74-118">**Nota**: La dirección URL devuelta no puede estar en el punto de conexión de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3af74-118">**Note:** The location URL returned may not be on the Microsoft Graph API endpoint.</span></span>

<span data-ttu-id="3af74-p105">En muchos casos esto puede ser el final de la solicitud, ya que la acción de copia se completará sin que la aplicación realice ninguna acción adicional. En cambio, si la aplicación tiene que mostrar el estado de la acción de copia o garantizar que finaliza sin errores, puede hacerlo con la dirección URL de supervisión.</span><span class="sxs-lookup"><span data-stu-id="3af74-p105">In many cases this may be the end of the request, since the copy action will complete without the app doing any additional work. However, if your app needs to show the status of the copy action or ensure that it completes without error, it can do so using the monitor URL.</span></span>

## <a name="retrieve-a-status-report-from-the-monitor-url"></a><span data-ttu-id="3af74-121">Recuperar un informe de estado desde la dirección URL de supervisión</span><span class="sxs-lookup"><span data-stu-id="3af74-121">Retrieve a status report from the monitor URL</span></span>

<span data-ttu-id="3af74-122">Para comprobar el estado de la acción de copia, la aplicación realiza una solicitud a la dirección URL proporcionada en la respuesta anterior.</span><span class="sxs-lookup"><span data-stu-id="3af74-122">To check on the status of the copy action, the app makes a request to the URL provided in the previous response.</span></span>
<span data-ttu-id="3af74-123">*Nota:* Esta solicitud no necesita autenticación, ya que la dirección URL es de corta duración y única para el autor de la llamada original.</span><span class="sxs-lookup"><span data-stu-id="3af74-123">*Note:* This request does not require authentication, since the URL is short-lived and unique to the original caller.</span></span> 

<!-- { "blockType": "request", "opaqueUrl": true, "name": "lro-check-status", "scopes": "files.readwrite" } -->

```http
GET https://api.onedrive.com/monitor/4A3407B5-88FC-4504-8B21-0AABD3412717
```

<span data-ttu-id="3af74-124">El servicio responde con información de que la acción de larga duración todavía está en curso:</span><span class="sxs-lookup"><span data-stu-id="3af74-124">The service responses with information that the long running action is still in progress:</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.asyncJobStatus" } -->

```http
HTTP/1.1 202 Accepted
Content-type: application/json

{
  "operation": "ItemCopy",
  "percentageComplete": 27.8,
  "status": "inProgress"
}
```

<span data-ttu-id="3af74-125">Esta información puede usarse para proporcionar una actualización al usuario sobre el progreso de la acción de copia.</span><span class="sxs-lookup"><span data-stu-id="3af74-125">This information can be used to provide an update to the user about the progress of the copy action.</span></span>
<span data-ttu-id="3af74-126">La aplicación puede continuar sondeando la dirección URL de supervisión para solicitar actualizaciones de estado y mantener el seguimiento del progreso de la acción.</span><span class="sxs-lookup"><span data-stu-id="3af74-126">The app can continue to poll the monitor URL to request status updates and keep track of the progress of the action.</span></span>

## <a name="retrieve-a-completed-status-report-from-the-monitor-url"></a><span data-ttu-id="3af74-127">Recuperar un informe de estado completado desde la dirección URL de supervisión</span><span class="sxs-lookup"><span data-stu-id="3af74-127">Retrieve a completed status report from the monitor URL</span></span>

<span data-ttu-id="3af74-128">Después de unos segundos, la operación de copia se ha completado.</span><span class="sxs-lookup"><span data-stu-id="3af74-128">After a few seconds the copy operation has completed.</span></span>
<span data-ttu-id="3af74-129">Esta vez, cuando la aplicación realiza una solicitud a la dirección URL de supervisión, la respuesta es un redireccionamiento al resultado finalizado de la acción.</span><span class="sxs-lookup"><span data-stu-id="3af74-129">This time when the app makes a request to the monitor URL the response is a redirection to the finished result of the action.</span></span>

<!-- { "blockType": "request", "opaqueUrl": true, "name": "lro-check-status-complete", "scopes": "files.readwrite" } -->

```http
GET https://api.onedrive.com/monitor/4A3407B5-88FC-4504-8B21-0AABD3412717
```

<span data-ttu-id="3af74-130">Una vez finalizada la acción, la respuesta del servicio de supervisión devolverá el valor resourceId de los resultados.</span><span class="sxs-lookup"><span data-stu-id="3af74-130">When the action has completed, the response from the monitor service will return the resourceId for the results.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.asyncJobStatus" } -->

```http
HTTP/1.1 202 Accepted
Content-type: application/json

{
    "percentageComplete": 100.0,
    "resourceId": "01MOWKYVJML57KN2ANMBA3JZJS2MBGC7KM",
    "status": "completed"
}
```

## <a name="retrieve-the-results-of-the-completed-operation"></a><span data-ttu-id="3af74-131">Recuperar los resultados de la operación completada</span><span class="sxs-lookup"><span data-stu-id="3af74-131">Retrieve the results of the completed operation</span></span>

<span data-ttu-id="3af74-132">Una vez que haya finalizado el trabajo, la dirección URL de supervisión devuelve el resourceId del resultado, en este caso la nueva copia del elemento original.</span><span class="sxs-lookup"><span data-stu-id="3af74-132">Once the job has completed, the monitor URL returns the resourceId of the result, in this case the new copy of the original item.</span></span>
<span data-ttu-id="3af74-133">Puede dirigir este nuevo elemento mediante resourceId, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3af74-133">You can address this new item using the resourceId, for example:</span></span>

<!-- {
  "blockType": "request",
  "name": "lro-copy-item-example-complete",
  "scopes": "files.readwrite"
} -->

```http
GET https://graph.microsoft.com/beta/me/drive/items/{item-id}
```

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "",
    "name": "Copy of LargeFolder1",
    "folder": { },
    "size": 12019
}
```

## <a name="supported-resources"></a><span data-ttu-id="3af74-134">Recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="3af74-134">Supported resources</span></span>

<span data-ttu-id="3af74-135">Las acciones de larga duración son compatibles con los siguientes métodos de la API</span><span class="sxs-lookup"><span data-stu-id="3af74-135">Long running actions are supported on the following API methods</span></span>

| <span data-ttu-id="3af74-136">**Recurso**</span><span class="sxs-lookup"><span data-stu-id="3af74-136">**Resource**</span></span> | <span data-ttu-id="3af74-137">**API**</span><span class="sxs-lookup"><span data-stu-id="3af74-137">**API**</span></span> |
|:------ | :------ |
| <span data-ttu-id="3af74-138">DriveItem</span><span class="sxs-lookup"><span data-stu-id="3af74-138">DriveItem</span></span> | [<span data-ttu-id="3af74-139">Copiar</span><span class="sxs-lookup"><span data-stu-id="3af74-139">Copy</span></span>](/graph/api/driveitem-copy?view=graph-rest-beta) |

## <a name="prerequisites"></a><span data-ttu-id="3af74-140">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3af74-140">Prerequisites</span></span>

<span data-ttu-id="3af74-141">Para consultar el estado de una acción de larga duración se requieren los mismos [permisos](./permissions-reference.md) que para realizarla.</span><span class="sxs-lookup"><span data-stu-id="3af74-141">The same [permissions](./permissions-reference.md) that are required to perform a long running action are also required to query the status of a long running action.</span></span>




<!-- {
  "type": "#page.annotation",
  "description": "Monitor the progress of long-running actions in the API.",
  "keywords": "monitor,long,running,operation,action",
  "section": "documentation",
  "suppressions": [
    "Error: lro-check-status:
      Unable to locate a definition for resource type: microsoft.graph.asyncJobStatus",
    "Error: lro-check-status-complete:
      Unable to locate a definition for resource type: microsoft.graph.asyncJobStatus"
  ],
  "tocPath": "Concepts/Long running actions"
} -->
