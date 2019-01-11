---
title: Enumerar tareas
description: Obtenga todas las tareas de Outlook en el buzón del usuario.
localization_priority: Normal
ms.openlocfilehash: e3d0753d639d4051ed03cbebf131e931a58fab30
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877920"
---
# <a name="list-tasks"></a><span data-ttu-id="c9911-103">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="c9911-103">List tasks</span></span>

> <span data-ttu-id="c9911-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c9911-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c9911-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c9911-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c9911-106">Obtenga todas las tareas de Outlook en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="c9911-106">Get all the Outlook tasks in the user's mailbox.</span></span>

<span data-ttu-id="c9911-107">De forma predeterminada, esta operación (y las operaciones de entrada, revisión y [completar](../api/outlooktask-complete.md) tareas) devuelve propiedades relacionadas con la fecha en UTC.</span><span class="sxs-lookup"><span data-stu-id="c9911-107">By default, this operation (and the POST, PATCH, and [complete](../api/outlooktask-complete.md) task operations) returns date-related properties in UTC.</span></span> <span data-ttu-id="c9911-108">Puede usar el `Prefer: outlook.timezone` encabezado para que todas las propiedades relacionadas con la fecha en la respuesta representada en una zona horaria diferente a la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="c9911-108">You can use the `Prefer: outlook.timezone` header to have all the date-related properties in the response represented in a time zone different than UTC.</span></span> <span data-ttu-id="c9911-109">Ver un [ejemplo](outlooktask-get.md#example-2) para obtener una única tarea.</span><span class="sxs-lookup"><span data-stu-id="c9911-109">See an [example](outlooktask-get.md#example-2) for getting a single task.</span></span> <span data-ttu-id="c9911-110">Puede aplicar el encabezado de forma similar para obtener varias tareas.</span><span class="sxs-lookup"><span data-stu-id="c9911-110">You can apply the header similarly to get multiple tasks.</span></span> 

## <a name="permissions"></a><span data-ttu-id="c9911-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="c9911-111">Permissions</span></span>
<span data-ttu-id="c9911-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c9911-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c9911-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c9911-114">Permission type</span></span>      | <span data-ttu-id="c9911-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c9911-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c9911-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c9911-116">Delegated (work or school account)</span></span> | <span data-ttu-id="c9911-117">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="c9911-117">Tasks.Read</span></span>    |
|<span data-ttu-id="c9911-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c9911-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c9911-119">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="c9911-119">Tasks.Read</span></span>    |
|<span data-ttu-id="c9911-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c9911-120">Application</span></span> | <span data-ttu-id="c9911-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c9911-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c9911-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c9911-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id|userPrincipalName}/outlook/tasks
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c9911-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c9911-123">Optional query parameters</span></span>
<span data-ttu-id="c9911-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9911-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c9911-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c9911-125">Request headers</span></span>
| <span data-ttu-id="c9911-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9911-126">Name</span></span>      |<span data-ttu-id="c9911-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9911-127">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c9911-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="c9911-128">Authorization</span></span>  | <span data-ttu-id="c9911-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c9911-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c9911-131">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="c9911-131">Prefer: outlook.timezone</span></span> | <span data-ttu-id="c9911-132">Especifica la zona horaria de propiedades de tiempo en la respuesta, que sería en UTC si no se especifica este encabezado.</span><span class="sxs-lookup"><span data-stu-id="c9911-132">Specifies the time zone for time properties in the response, which would be in UTC if this header is not specified.</span></span> <span data-ttu-id="c9911-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c9911-133">Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c9911-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c9911-134">Request body</span></span>
<span data-ttu-id="c9911-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c9911-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c9911-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9911-136">Response</span></span>

<span data-ttu-id="c9911-137">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [outlookTask](../resources/outlooktask.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9911-137">If successful, this method returns a `200 OK` response code and collection of [outlookTask](../resources/outlooktask.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c9911-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c9911-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c9911-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c9911-139">Request</span></span>
<span data-ttu-id="c9911-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c9911-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tasks"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/tasks
```
##### <a name="response"></a><span data-ttu-id="c9911-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9911-141">Response</span></span>
<span data-ttu-id="c9911-142">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9911-142">Here is an example of the response.</span></span> <span data-ttu-id="c9911-143">De forma predeterminada, las propiedades de fecha y hora de la respuesta están en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="c9911-143">By default, the date-time properties in the response are in UTC.</span></span> 

<span data-ttu-id="c9911-p107">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c9911-p107">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 465

{
  "value": [
   {
      "id": "AAMkADA1MTrfAAA=",
      "createdDateTime": "2016-04-22T05:44:01.2012012Z",
      "lastModifiedDateTime": "2016-04-22T05:44:02.9980882Z",
      "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIOJMxw==",
      "categories": [ ],
      "assignedTo": null,
      "body": {
        "contentType": "text",
        "content": ""
      },
      "completedDateTime": null,
      "dueDateTime": {
        "dateTime": "2016-04-25T07:00:00.0000000",
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
        "dateTime": "2016-04-23T07:00:00.0000000",
        "timeZone": "UTC"
      },
      "status": "notStarted",
      "subject": "Shop for dinner"
    },
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List Tasks",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
