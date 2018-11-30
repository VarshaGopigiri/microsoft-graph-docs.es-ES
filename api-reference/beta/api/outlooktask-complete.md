---
title: 'outlookTask: completa'
description: 'Completar una tarea de Outlook que establece la propiedad **completedDateTime** a la fecha actual, '
ms.openlocfilehash: 732da0f3eb03f6a4674e1254586ae21b5f3334bb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089374"
---
# <a name="outlooktask-complete"></a><span data-ttu-id="7daf6-103">outlookTask: completa</span><span class="sxs-lookup"><span data-stu-id="7daf6-103">outlookTask: complete</span></span>

> <span data-ttu-id="7daf6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7daf6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7daf6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7daf6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7daf6-106">Completar una tarea de Outlook que establece la propiedad **completedDateTime** a la fecha actual y la propiedad **status** para `completed`.</span><span class="sxs-lookup"><span data-stu-id="7daf6-106">Complete an Outlook task which sets the **completedDateTime** property to the current date, and the **status** property to `completed`.</span></span>

<span data-ttu-id="7daf6-107">Si se está realizando una tarea en una serie periódica, en la respuesta, la colección de tareas contendrá la tarea completada en la serie y la siguiente tarea de la serie.</span><span class="sxs-lookup"><span data-stu-id="7daf6-107">If you are completing a task in a recurring series, in the response, the task collection will contain the completed task in the series, and the next task in the series.</span></span>

<span data-ttu-id="7daf6-108">La propiedad **completedDateTime** representa la fecha cuando termina la tarea.</span><span class="sxs-lookup"><span data-stu-id="7daf6-108">The **completedDateTime** property represents the date when the task is finished.</span></span> <span data-ttu-id="7daf6-109">La parte de **completedDateTime** la hora se establece en medianoche UTC de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7daf6-109">The time portion of **completedDateTime** is set to midnight UTC by default.</span></span> 

<span data-ttu-id="7daf6-110">De forma predeterminada, esta operación (y las operaciones de tarea de revisión, GET y POST) devuelve propiedades relacionadas con la fecha en UTC.</span><span class="sxs-lookup"><span data-stu-id="7daf6-110">By default, this operation (and the POST, GET, and PATCH task operations) returns date-related properties in UTC.</span></span> <span data-ttu-id="7daf6-111">Puede usar el `Prefer: outlook.timezone` encabezado para que todas las propiedades relacionadas con la fecha en la respuesta representada en una zona horaria diferente a la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="7daf6-111">You can use the `Prefer: outlook.timezone` header to have all the date-related properties in the response represented in a time zone different than UTC.</span></span>

## <a name="permissions"></a><span data-ttu-id="7daf6-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="7daf6-112">Permissions</span></span>
<span data-ttu-id="7daf6-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7daf6-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7daf6-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7daf6-115">Permission type</span></span>      | <span data-ttu-id="7daf6-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7daf6-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7daf6-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7daf6-117">Delegated (work or school account)</span></span> | <span data-ttu-id="7daf6-118">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7daf6-118">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="7daf6-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7daf6-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7daf6-120">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7daf6-120">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="7daf6-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7daf6-121">Application</span></span> | <span data-ttu-id="7daf6-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7daf6-122">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7daf6-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7daf6-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/outlook/tasks/{id}/complete
POST /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks/{id}/complete
POST /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}/complete

```
## <a name="request-headers"></a><span data-ttu-id="7daf6-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7daf6-124">Request headers</span></span>
| <span data-ttu-id="7daf6-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="7daf6-125">Name</span></span>       | <span data-ttu-id="7daf6-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="7daf6-126">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="7daf6-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="7daf6-127">Authorization</span></span>  | <span data-ttu-id="7daf6-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7daf6-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7daf6-130">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="7daf6-130">Prefer: outlook.timezone</span></span> | <span data-ttu-id="7daf6-131">Especifica la zona horaria de propiedades de tiempo en la respuesta, que sería en UTC si no se especifica este encabezado.</span><span class="sxs-lookup"><span data-stu-id="7daf6-131">Specifies the time zone for time properties in the response, which would be in UTC if this header is not specified.</span></span> <span data-ttu-id="7daf6-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7daf6-132">Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7daf6-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7daf6-133">Request body</span></span>

## <a name="response"></a><span data-ttu-id="7daf6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7daf6-134">Response</span></span>

<span data-ttu-id="7daf6-135">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [outlookTask](../resources/outlooktask.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7daf6-135">If successful, this method returns `200 OK` response code and [outlookTask](../resources/outlooktask.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7daf6-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7daf6-136">Example</span></span>
<span data-ttu-id="7daf6-137">En el ejemplo siguiente se marca la tarea como completada especificada.</span><span class="sxs-lookup"><span data-stu-id="7daf6-137">The following example marks the specified task as complete.</span></span> <span data-ttu-id="7daf6-138">Especifica la hora estándar del Pacífico (PST) en el `Prefer: outlook.timezone` encabezado.</span><span class="sxs-lookup"><span data-stu-id="7daf6-138">It specifies Pacific Standard Time (PST) in the `Prefer: outlook.timezone` header.</span></span>
##### <a name="request"></a><span data-ttu-id="7daf6-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7daf6-139">Request</span></span>
<span data-ttu-id="7daf6-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7daf6-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "outlooktask_complete"
}-->
```http
POST https://graph.microsoft.com/beta/me/tasks('AAMkADA1MT15rfAAA=')/complete
Prefer: outlook.timezone="Pacific Standard Time"
```

##### <a name="response"></a><span data-ttu-id="7daf6-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7daf6-141">Response</span></span>
<span data-ttu-id="7daf6-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7daf6-142">Here is an example of the response.</span></span> <span data-ttu-id="7daf6-143">El **completedDateTime** y otras propiedades relacionadas con la fecha en la respuesta se expresan en PST.</span><span class="sxs-lookup"><span data-stu-id="7daf6-143">The **completedDateTime** and other date-related properties in the response are expressed in PST.</span></span> 

<span data-ttu-id="7daf6-p109">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7daf6-p109">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "id": "AAMkADA1MT15rfAAA=",
      "createdDateTime": "2016-04-21T22:44:01.2012012-07:00",
      "lastModifiedDateTime": "2016-04-22T19:28:38.5300447-07:00",
      "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIW9XYQ==",
      "categories": [
      ],
      "assignedTo": null,
      "body": {
          "contentType": "text",
          "content": ""
      },
      "completedDateTime": {
          "dateTime": "2016-04-22T00:00:00.0000000",
          "timeZone": "Pacific Standard Time"
      },
      "dueDateTime": {
          "dateTime": "2016-04-25T00:00:00.0000000",
          "timeZone": "Pacific Standard Time"
      },
      "hasAttachments":false,
      "importance": "normal",
      "isReminderOn": false,
      "owner": "Administrator",
      "parentFolderId": "AQMkADA1MTIBEgAAAA==",
      "recurrence": null,
      "reminderDateTime": null,
      "sensitivity": "normal",
      "startDateTime": {
          "dateTime": "2016-04-21T00:00:00.0000000",
          "timeZone": "Pacific Standard Time"
      },
      "status": "completed",
      "subject": "Shop for dinner"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookTask: complete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->