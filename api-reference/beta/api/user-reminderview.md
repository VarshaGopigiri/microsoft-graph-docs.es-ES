---
title: 'user: reminderView'
description: 'Devuelve una lista de los avisos de calendario entre las horas de inicio y finalización especificadas. '
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 3fb0283aaae4f814f06b59a8a6ad6183cc18fec1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918213"
---
# <a name="user-reminderview"></a><span data-ttu-id="5ad45-103">user: reminderView</span><span class="sxs-lookup"><span data-stu-id="5ad45-103">user: reminderView</span></span>

> <span data-ttu-id="5ad45-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5ad45-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5ad45-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5ad45-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5ad45-106">Devolver una lista de los avisos de eventos en un calendario de usuario dentro de la especificada tiempos inicial y final.</span><span class="sxs-lookup"><span data-stu-id="5ad45-106">Return a list of event reminders in a user calendar within the specified start and end times.</span></span> 

## <a name="permissions"></a><span data-ttu-id="5ad45-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5ad45-107">Permissions</span></span>
<span data-ttu-id="5ad45-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5ad45-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5ad45-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5ad45-110">Permission type</span></span>      | <span data-ttu-id="5ad45-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5ad45-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5ad45-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5ad45-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5ad45-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5ad45-113">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="5ad45-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5ad45-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5ad45-115">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5ad45-115">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="5ad45-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5ad45-116">Application</span></span> | <span data-ttu-id="5ad45-117">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5ad45-117">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="5ad45-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5ad45-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/reminderView(startDateTime=startDateTime-value,endDateTime=endDateTime-value)
```

## <a name="function-parameters"></a><span data-ttu-id="5ad45-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="5ad45-119">Function parameters</span></span>
<span data-ttu-id="5ad45-120">En la dirección URL de la solicitud, proporcione los siguientes parámetros de función con valores.</span><span class="sxs-lookup"><span data-stu-id="5ad45-120">In the request URL, provide the following function parameters with values.</span></span>

| <span data-ttu-id="5ad45-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5ad45-121">Parameter</span></span>    | <span data-ttu-id="5ad45-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad45-122">Type</span></span>   |<span data-ttu-id="5ad45-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad45-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5ad45-124">startDateTime</span><span class="sxs-lookup"><span data-stu-id="5ad45-124">startDateTime</span></span>|<span data-ttu-id="5ad45-125">String</span><span class="sxs-lookup"><span data-stu-id="5ad45-125">String</span></span>|<span data-ttu-id="5ad45-p103">Fecha y hora de inicio del evento para el que se configura el aviso. El valor se representa en formato ISO 8601, por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="5ad45-p103">The start date and time of the event for which the reminder is set up. The value is represented in ISO 8601 format, for example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="5ad45-128">endDateTime</span><span class="sxs-lookup"><span data-stu-id="5ad45-128">endDateTime</span></span>|<span data-ttu-id="5ad45-129">String</span><span class="sxs-lookup"><span data-stu-id="5ad45-129">String</span></span>|<span data-ttu-id="5ad45-p104">Fecha y hora de finalización del evento para el que se configura el aviso. El valor se representa en formato ISO 8601, por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="5ad45-p104">The end date and time of the event for which the reminder is set up. The value is represented in ISO 8601 format, for example, "2015-11-08T20:00:00.0000000".</span></span>|

## <a name="request-headers"></a><span data-ttu-id="5ad45-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5ad45-132">Request headers</span></span>
| <span data-ttu-id="5ad45-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ad45-133">Header</span></span>       | <span data-ttu-id="5ad45-134">Valor</span><span class="sxs-lookup"><span data-stu-id="5ad45-134">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="5ad45-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="5ad45-135">Authorization</span></span>  | <span data-ttu-id="5ad45-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5ad45-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="5ad45-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5ad45-138">Content-Type</span></span>   | <span data-ttu-id="5ad45-139">application/json</span><span class="sxs-lookup"><span data-stu-id="5ad45-139">application/json</span></span> |
| <span data-ttu-id="5ad45-140">Prefer</span><span class="sxs-lookup"><span data-stu-id="5ad45-140">Prefer</span></span> | <span data-ttu-id="5ad45-p106">{Zona horaria}. Opcional, se supone la hora UTC si no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="5ad45-p106">{Time-zone}. Optional, UTC assumed if absent.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5ad45-143">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5ad45-143">Request body</span></span>
<span data-ttu-id="5ad45-144">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5ad45-144">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5ad45-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ad45-145">Response</span></span>

<span data-ttu-id="5ad45-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [reminder](../resources/reminder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5ad45-146">If successful, this method returns `200 OK` response code and [reminder](../resources/reminder.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5ad45-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5ad45-147">Example</span></span>
<span data-ttu-id="5ad45-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5ad45-148">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5ad45-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5ad45-149">Request</span></span>
<span data-ttu-id="5ad45-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5ad45-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_reminderview"
}-->
```http
GET https://graph.microsoft.com/beta/me/reminderView(startDateTime='2017-06-05T10:00:00.0000000',endDateTime='2017-06-11T11:00:00.0000000')
```

##### <a name="response"></a><span data-ttu-id="5ad45-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ad45-151">Response</span></span>
<span data-ttu-id="5ad45-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5ad45-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.reminder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 673

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.reminder)",
    "value": [
        {
            "eventId": "AAMkADNsvAAA=",
            "changeKey": "SuFHwDRP1EeXJUopWbSLlgAAmBvk2g==",
            "eventSubject": "Plan summer company picnic",
            "eventWebLink": "https://outlook.office365.com/owa/?itemid=AAMkADNsvAAA%3D&exvsurl=1&path=/calendar/item",
            "eventStartTime": {
                "dateTime": "2017-06-09T18:00:00.0000000",
                "timeZone": "UTC"
            },
            "eventEndTime": {
                "dateTime": "2017-06-09T19:00:00.0000000",
                "timeZone": "UTC"
            },
            "eventLocation": {
                "displayName": "Conf Room 3"
            },
            "reminderFireTime": {
                "dateTime": "2017-06-09T17:45:00.0000000",
                "timeZone": "UTC"
            }
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: reminderView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
