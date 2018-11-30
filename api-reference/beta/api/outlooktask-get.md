---
title: Obtener outlookTask
description: Obtener las propiedades y relaciones de una tarea de Outlook en el buzón del usuario.
ms.openlocfilehash: d7d985614a37f0a4a70a074f63f4182130948495
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083683"
---
# <a name="get-outlooktask"></a><span data-ttu-id="a2882-103">Obtener outlookTask</span><span class="sxs-lookup"><span data-stu-id="a2882-103">Get outlookTask</span></span>

> <span data-ttu-id="a2882-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2882-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2882-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2882-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a2882-106">Obtener las propiedades y relaciones de una tarea de Outlook en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="a2882-106">Get the properties and relationships of an Outlook task in the user's mailbox.</span></span>

<span data-ttu-id="a2882-107">De forma predeterminada, esta operación (y las operaciones de entrada, revisión y [completar](../api/outlooktask-complete.md) tareas) devuelve propiedades relacionadas con la fecha en UTC.</span><span class="sxs-lookup"><span data-stu-id="a2882-107">By default, this operation (and the POST, PATCH, and [complete](../api/outlooktask-complete.md) task operations) returns date-related properties in UTC.</span></span> <span data-ttu-id="a2882-108">Puede usar el `Prefer: outlook.timezone` encabezado para que todas las propiedades relacionadas con la fecha en la respuesta representada en una zona horaria diferente a la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="a2882-108">You can use the `Prefer: outlook.timezone` header to have all the date-related properties in the response represented in a time zone different than UTC.</span></span>

## <a name="permissions"></a><span data-ttu-id="a2882-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="a2882-109">Permissions</span></span>
<span data-ttu-id="a2882-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2882-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a2882-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2882-112">Permission type</span></span>      | <span data-ttu-id="a2882-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2882-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a2882-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2882-114">Delegated (work or school account)</span></span> | <span data-ttu-id="a2882-115">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a2882-115">Tasks.Read</span></span>    |
|<span data-ttu-id="a2882-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2882-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a2882-117">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a2882-117">Tasks.Read</span></span>    |
|<span data-ttu-id="a2882-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2882-118">Application</span></span> | <span data-ttu-id="a2882-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2882-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a2882-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2882-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id|userPrincipalName}/outlook/tasks/{id}
GET /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks/{id}
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a2882-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a2882-121">Optional query parameters</span></span>
<span data-ttu-id="a2882-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2882-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a2882-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2882-123">Request headers</span></span>
| <span data-ttu-id="a2882-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="a2882-124">Name</span></span>      |<span data-ttu-id="a2882-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2882-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a2882-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="a2882-126">Authorization</span></span>  | <span data-ttu-id="a2882-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a2882-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a2882-129">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="a2882-129">Prefer: outlook.timezone</span></span> | <span data-ttu-id="a2882-130">Especifica la zona horaria de propiedades de tiempo en la respuesta, que sería en UTC si no se especifica este encabezado.</span><span class="sxs-lookup"><span data-stu-id="a2882-130">Specifies the time zone for time properties in the response, which would be in UTC if this header is not specified.</span></span> <span data-ttu-id="a2882-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a2882-131">Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a2882-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2882-132">Request body</span></span>
<span data-ttu-id="a2882-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a2882-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a2882-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2882-134">Response</span></span>

<span data-ttu-id="a2882-135">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [outlookTask](../resources/outlooktask.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2882-135">If successful, this method returns a `200 OK` response code and [outlookTask](../resources/outlooktask.md) object in the response body.</span></span>
## <a name="example-1"></a><span data-ttu-id="a2882-136">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2882-136">Example 1</span></span>
##### <a name="request"></a><span data-ttu-id="a2882-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2882-137">Request</span></span>
<span data-ttu-id="a2882-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2882-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_outlooktask"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/tasks('AAMkADA1MTrgAAA=')
```
##### <a name="response"></a><span data-ttu-id="a2882-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2882-139">Response</span></span>
<span data-ttu-id="a2882-140">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2882-140">Here is an example of the response.</span></span> <span data-ttu-id="a2882-141">De forma predeterminada, las propiedades de fecha y hora de la respuesta están en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="a2882-141">By default, the date-time properties in the response are in UTC.</span></span> 

<span data-ttu-id="a2882-p107">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2882-p107">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 376

{
  "id": "AAMkADA1MTrgAAA=",
  "createdDateTime": "2016-04-22T06:03:35.9279794Z",
  "lastModifiedDateTime": "2016-04-22T06:03:35.9436052Z",
  "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIOJMyQ==",
  "categories": [ ],
  "assignedTo": null,
  "body": {
    "contentType": "text",
    "content": ""
  },
  "completedDateTime": null,
  "dueDateTime": {
    "dateTime": "2016-04-27T04:00:00.0000000",
    "timeZone": "UTC"
  },
  "hasAttachments":false,
  "importance": "normal",
  "isReminderOn": false,
  "owner": "Administrator",
  "parentFolderId": "AQMkADA1MTBEgAAAA==",
  "recurrence": null,
  "reminderDateTime": null,
  "sensitivity": "normal",
  "startDateTime": {
    "dateTime": "2016-04-26T04:00:00.0000000",
    "timeZone": "UTC"
  },
  "status": "notStarted",
  "subject": "Shop for dinner"
}
```


## <a name="example-2"></a><span data-ttu-id="a2882-144">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="a2882-144">Example 2</span></span>
##### <a name="request"></a><span data-ttu-id="a2882-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2882-145">Request</span></span>
<span data-ttu-id="a2882-146">En este ejemplo se usa el `Prefer: outlook.timezone` encabezado para especificar la visualización de las propiedades de fecha y hora en la respuesta</span><span class="sxs-lookup"><span data-stu-id="a2882-146">This example uses the `Prefer: outlook.timezone` header to specify displaying date-time properties in the response</span></span>  
<span data-ttu-id="a2882-147">Hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="a2882-147">in Pacific Standard Time.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_outlooktask"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/tasks('AAMkADA1MHgwAAA=')
Prefer: outlook.timezone="Pacific Standard Time"
```
##### <a name="response"></a><span data-ttu-id="a2882-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2882-148">Response</span></span>
<span data-ttu-id="a2882-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2882-149">Here is an example of the response.</span></span> <span data-ttu-id="a2882-150">Se muestran las propiedades de fecha y hora en la respuesta en el tiempo de estándar del Pacífico especificado.</span><span class="sxs-lookup"><span data-stu-id="a2882-150">The date-time properties in the response are displayed in the specified Pacific Standard Time.</span></span> 

<span data-ttu-id="a2882-p109">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2882-p109">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 576

{
  "id": "AAMkADA1MHgwAAA=",
  "createdDateTime": "2016-04-22T15:19:18.9526004-07:00",
  "lastModifiedDateTime": "2016-04-22T15:19:19.015101-07:00",
  "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIW9XXA==",
  "categories": [ ],
  "assignedTo": "Dana Swope",
  "body": {
    "contentType": "text",
    "content": ""
  },
  "completedDateTime": null,
  "dueDateTime": {
    "dateTime": "2016-05-04T021:00:00.0000000",
    "timeZone": "Pacific Standard Time"
  },
  "hasAttachments":false,
  "importance": "normal",
  "isReminderOn": false,
  "owner": "Administrator",
  "parentFolderId": "AQMkADA1MTEgAAAA==",
  "recurrence": null,
  "reminderDateTime": null,
  "sensitivity": "normal",
  "startDateTime": {
    "dateTime": "2016-05-02T21:00:00.0000000",
    "timeZone": "Pacific Standard Time"
  },
  "status": "notStarted",
  "subject": "Shop for children's weekend"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get outlookTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->