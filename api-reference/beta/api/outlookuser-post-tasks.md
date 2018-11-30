---
title: Crear outlookTask
description: Crear una tarea de Outlook en el grupo de tarea predeterminado (`My Tasks`) y la carpeta de tareas predeterminada (`Tasks`) en el buzón del usuario.
ms.openlocfilehash: c9019db8e36151c70c5e3d2abe1ea4fea2e94ef0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089588"
---
# <a name="create-outlooktask"></a><span data-ttu-id="b128d-103">Crear outlookTask</span><span class="sxs-lookup"><span data-stu-id="b128d-103">Create outlookTask</span></span>

> <span data-ttu-id="b128d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b128d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b128d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b128d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b128d-106">Crear una tarea de Outlook en el grupo de tarea predeterminado (`My Tasks`) y la carpeta de tareas predeterminada (`Tasks`) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="b128d-106">Create an Outlook task in the default task group (`My Tasks`) and default task folder (`Tasks`) in the user's mailbox.</span></span>

<span data-ttu-id="b128d-107">El método POST siempre omite la parte de tiempo de **startDateTime** y **dueDateTime** en el cuerpo de la solicitud y supone el tiempo para que siempre se medianoche en la zona horaria especificada.</span><span class="sxs-lookup"><span data-stu-id="b128d-107">The POST method always ignores the time portion of **startDateTime** and **dueDateTime** in the request body, and assumes the time to be always midnight in the specified time zone.</span></span>

<span data-ttu-id="b128d-108">De forma predeterminada, esta operación (y las operaciones de tarea GET, revisión y [completar](../api/outlooktask-complete.md) ) devuelve propiedades relacionadas con la fecha en UTC.</span><span class="sxs-lookup"><span data-stu-id="b128d-108">By default, this operation (and the GET, PATCH, and [complete](../api/outlooktask-complete.md) task operations) returns date-related properties in UTC.</span></span> <span data-ttu-id="b128d-109">Puede usar el `Prefer: outlook.timezone` encabezado para que todas las propiedades relacionadas con la fecha en la respuesta representada en una zona horaria diferente a la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="b128d-109">You can use the `Prefer: outlook.timezone` header to have all the date-related properties in the response represented in a time zone different than UTC.</span></span>

## <a name="permissions"></a><span data-ttu-id="b128d-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="b128d-110">Permissions</span></span>
<span data-ttu-id="b128d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b128d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b128d-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b128d-113">Permission type</span></span>      | <span data-ttu-id="b128d-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b128d-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b128d-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b128d-115">Delegated (work or school account)</span></span> | <span data-ttu-id="b128d-116">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b128d-116">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="b128d-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b128d-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b128d-118">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b128d-118">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="b128d-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b128d-119">Application</span></span> | <span data-ttu-id="b128d-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b128d-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b128d-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b128d-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/outlook/tasks
```
## <a name="request-headers"></a><span data-ttu-id="b128d-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b128d-122">Request headers</span></span>
| <span data-ttu-id="b128d-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="b128d-123">Name</span></span>       | <span data-ttu-id="b128d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b128d-124">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b128d-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="b128d-125">Authorization</span></span>  | <span data-ttu-id="b128d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b128d-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b128d-128">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="b128d-128">Prefer: outlook.timezone</span></span> | <span data-ttu-id="b128d-129">Especifica la zona horaria de propiedades de tiempo en la respuesta, que sería en UTC si no se especifica este encabezado.</span><span class="sxs-lookup"><span data-stu-id="b128d-129">Specifies the time zone for time properties in the response, which would be in UTC if this header is not specified.</span></span> <span data-ttu-id="b128d-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b128d-130">Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b128d-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b128d-131">Request body</span></span>
<span data-ttu-id="b128d-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTask](../resources/outlooktask.md) .</span><span class="sxs-lookup"><span data-stu-id="b128d-132">In the request body, supply a JSON representation of [outlookTask](../resources/outlooktask.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="b128d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b128d-133">Response</span></span>

<span data-ttu-id="b128d-134">Si tiene éxito, este método devuelve `201 Created` objeto de código y [outlookTask](../resources/outlooktask.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b128d-134">If successful, this method returns `201 Created` response code and [outlookTask](../resources/outlooktask.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b128d-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b128d-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b128d-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b128d-136">Request</span></span>
<span data-ttu-id="b128d-137">En el ejemplo siguiente se muestra el uso de la `Prefer: outlook.timezone` encabezado.</span><span class="sxs-lookup"><span data-stu-id="b128d-137">The following example shows the use of the `Prefer: outlook.timezone` header.</span></span> <span data-ttu-id="b128d-138">Crea una tarea, expresa **startDateTime** y **dueDateTime** en la hora estándar (EST) e incluye un `Prefer` encabezado de hora estándar del Pacífico (PST).</span><span class="sxs-lookup"><span data-stu-id="b128d-138">It creates a task, expresses **startDateTime** and **dueDateTime** in Eastern Standard Time (EST), and includes a `Prefer` header of Pacific Standard Time (PST).</span></span>
<!-- {
  "blockType": "request",
  "name": "create_outlooktask_from_outlookuser"
}-->
```http
POST https://graph.microsoft.com/beta/me/outlook/tasks
Prefer: outlook.timezone="Pacific Standard Time"
Content-type: application/json
Content-length: 276

{
  "assignedTo": "Dana Swope",
  "subject": "Shop for children's weekend",
  "startDateTime": {
      "dateTime": "2016-05-03T09:00:00",
      "timeZone": "Eastern Standard Time"
  },
  "dueDateTime":  {
      "dateTime": "2016-05-05T16:00:00",
      "timeZone": "Eastern Standard Time"
  }
}
```
<span data-ttu-id="b128d-139">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTask](../resources/outlooktask.md) .</span><span class="sxs-lookup"><span data-stu-id="b128d-139">In the request body, supply a JSON representation of [outlookTask](../resources/outlooktask.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="b128d-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b128d-140">Response</span></span>
<span data-ttu-id="b128d-141">El método POST omite la parte de tiempo de **startDateTime** y **dueDateTime** en el cuerpo de la solicitud y se da por supuesto la hora a estar siempre medianoche en la zona horaria especificada (EST).</span><span class="sxs-lookup"><span data-stu-id="b128d-141">The POST method ignores the time portion of **startDateTime** and **dueDateTime** in the request body and assumes the time to be always midnight in the specified time zone (EST).</span></span>

<span data-ttu-id="b128d-142">Dado que el `Prefer` encabezado especifica PST, el método POST expresa todas las propiedades relacionadas con la fecha en la respuesta en PST.</span><span class="sxs-lookup"><span data-stu-id="b128d-142">Since the `Prefer` header specifies PST, the POST method expresses all the date-related properties in the response in PST.</span></span> <span data-ttu-id="b128d-143">En concreto, para las propiedades **startDateTime** y **dueDateTime** , el método POST convierte medianoche en EST a PST y devuelve en PST en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b128d-143">In particular, for the **startDateTime** and **dueDateTime** properties, the POST method converts midnight in EST to PST and returns them in PST in the response.</span></span>

<span data-ttu-id="b128d-p108">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b128d-p108">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask"
} -->
```http
HTTP/1.1 201 Created
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
    "contentType": "Text",
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
  "sensitivity": "Normal",
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
  "description": "Create outlookTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->