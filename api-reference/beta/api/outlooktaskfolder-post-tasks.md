---
title: Crear outlookTask
description: Crear una tarea de Outlook en la carpeta de la tarea especificada.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 477ddf32b790da5b5d43560119d7a2529e773ad0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841422"
---
# <a name="create-outlooktask"></a><span data-ttu-id="8f81e-103">Crear outlookTask</span><span class="sxs-lookup"><span data-stu-id="8f81e-103">Create outlookTask</span></span>

> <span data-ttu-id="8f81e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8f81e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8f81e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8f81e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8f81e-106">Crear una tarea de Outlook en la carpeta de la tarea especificada.</span><span class="sxs-lookup"><span data-stu-id="8f81e-106">Create an Outlook task in the specified task folder.</span></span>

<span data-ttu-id="8f81e-107">El método POST siempre omite la parte de tiempo de **startDateTime** y **dueDateTime** en el cuerpo de la solicitud y supone el tiempo para que siempre se medianoche en la zona horaria especificada.</span><span class="sxs-lookup"><span data-stu-id="8f81e-107">The POST method always ignores the time portion of **startDateTime** and **dueDateTime** in the request body, and assumes the time to be always midnight in the specified time zone.</span></span>

## <a name="permissions"></a><span data-ttu-id="8f81e-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="8f81e-108">Permissions</span></span>
<span data-ttu-id="8f81e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8f81e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8f81e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f81e-111">Permission type</span></span>      | <span data-ttu-id="8f81e-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f81e-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8f81e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f81e-113">Delegated (work or school account)</span></span> | <span data-ttu-id="8f81e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f81e-114">Not supported.</span></span>    |
|<span data-ttu-id="8f81e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f81e-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8f81e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f81e-116">Not supported.</span></span>    |
|<span data-ttu-id="8f81e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f81e-117">Application</span></span> | <span data-ttu-id="8f81e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f81e-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8f81e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f81e-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks
POST /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks
```
## <a name="request-headers"></a><span data-ttu-id="8f81e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f81e-120">Request headers</span></span>
| <span data-ttu-id="8f81e-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f81e-121">Name</span></span>       | <span data-ttu-id="8f81e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f81e-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="8f81e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f81e-123">Authorization</span></span>  | <span data-ttu-id="8f81e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f81e-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8f81e-126">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="8f81e-126">Prefer: outlook.timezone</span></span> | <span data-ttu-id="8f81e-127">Especifica la zona horaria de propiedades de tiempo en la respuesta, que sería en UTC si no se especifica este encabezado.</span><span class="sxs-lookup"><span data-stu-id="8f81e-127">Specifies the time zone for time properties in the response, which would be in UTC if this header is not specified.</span></span> <span data-ttu-id="8f81e-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8f81e-128">Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="8f81e-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f81e-129">Request body</span></span>
<span data-ttu-id="8f81e-130">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTask](../resources/outlooktask.md) .</span><span class="sxs-lookup"><span data-stu-id="8f81e-130">In the request body, supply a JSON representation of [outlookTask](../resources/outlooktask.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="8f81e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f81e-131">Response</span></span>

<span data-ttu-id="8f81e-132">Si tiene éxito, este método devuelve `201 Created` objeto de código y [outlookTask](../resources/outlooktask.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f81e-132">If successful, this method returns `201 Created` response code and [outlookTask](../resources/outlooktask.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f81e-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f81e-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8f81e-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f81e-134">Request</span></span>
<span data-ttu-id="8f81e-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f81e-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_outlooktask_from_outlooktaskfolder"
}-->
```http
POST https://graph.microsoft.com/beta/me/taskfolders('AAMkADIyAAAhrbPXAAA=')/tasks
Content-type: application/json
Content-length: 376

{
  "subject": "Shop for dinner",
  "startDateTime": {
      "dateTime": "2016-04-23T18:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "dueDateTime":  {
      "dateTime": "2016-04-25T13:00:00",
      "timeZone": "Pacific Standard Time"
  }
}
```
<span data-ttu-id="8f81e-136">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTask](../resources/outlooktask.md) .</span><span class="sxs-lookup"><span data-stu-id="8f81e-136">In the request body, supply a JSON representation of [outlookTask](../resources/outlooktask.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="8f81e-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f81e-137">Response</span></span>
<span data-ttu-id="8f81e-138">El método POST omite la parte de tiempo en el cuerpo de la solicitud y se da por supuesto la hora a estar siempre medianoche en la zona horaria especificada (PST).</span><span class="sxs-lookup"><span data-stu-id="8f81e-138">The POST method ignores the time portion in the request body and assumes the time to be always midnight in the specified time zone (PST).</span></span> <span data-ttu-id="8f81e-139">A continuación, de forma predeterminada, el método POST convierte y muestra todas las propiedades relacionadas con la fecha en UTC en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f81e-139">Then, by default, the POST method converts and shows all the date-related properties in UTC in the response.</span></span>

<span data-ttu-id="8f81e-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f81e-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 376

{
  "createdDateTime": "2016-04-22T05:44:01.2012012Z",
  "lastModifiedDateTime": "2016-04-22T05:44:02.9980882Z",
  "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIOJMxw==",
  "categories": [ ],
  "assignedTo": "null",
  "body": {
    "contentType": "Text",
    "content": ""
  },
  "completedDateTime": null,
  "dueDateTime": {
    "dateTime": "2016-04-25T07:00:00.0000000",
    "timeZone": "UTC"
  },
  "hasAttachments":false,
  "importance": "Normal",
  "isReminderOn": false,
  "owner": "Administrator",
  "parentFolderId": "AQMkADA1MTkAAAAIBEgAAAA==",
  "recurrence": null,
  "reminderDateTime": null,
  "sensitivity": "Normal",
  "startDateTime": {
    "dateTime": "2016-04-23T07:00:00.0000000",
    "timeZone": "UTC"
  },
  "status": "NotStarted",
  "subject": "Shop for dinner"
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
