---
title: 'user: reminderView'
description: 'Devuelve una lista de los avisos de calendario entre las horas de inicio y finalización especificadas. '
ms.openlocfilehash: d1e84620102400bebb9da7b7d14f77ae9e560dc1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029511"
---
# <a name="user-reminderview"></a><span data-ttu-id="a26ce-103">user: reminderView</span><span class="sxs-lookup"><span data-stu-id="a26ce-103">user: reminderView</span></span>
<span data-ttu-id="a26ce-104">Devuelve una lista de los avisos de calendario entre las horas de inicio y finalización especificadas.</span><span class="sxs-lookup"><span data-stu-id="a26ce-104">Return a list of calendar reminders within the specified start and end times.</span></span> 

## <a name="permissions"></a><span data-ttu-id="a26ce-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a26ce-105">Permissions</span></span>
<span data-ttu-id="a26ce-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a26ce-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a26ce-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a26ce-108">Permission type</span></span>      | <span data-ttu-id="a26ce-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a26ce-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a26ce-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a26ce-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a26ce-111">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a26ce-111">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="a26ce-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a26ce-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a26ce-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a26ce-113">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="a26ce-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a26ce-114">Application</span></span> | <span data-ttu-id="a26ce-115">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a26ce-115">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a26ce-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a26ce-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/reminderView(startDateTime=startDateTime-value,endDateTime=endDateTime-value)
```

## <a name="function-parameters"></a><span data-ttu-id="a26ce-117">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="a26ce-117">Function Parameters</span></span>
<span data-ttu-id="a26ce-118">En la dirección URL de la solicitud, proporcione los siguientes parámetros de función con valores.</span><span class="sxs-lookup"><span data-stu-id="a26ce-118">In the request URL, provide the following function parameters with values.</span></span>

| <span data-ttu-id="a26ce-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a26ce-119">Parameter</span></span>    | <span data-ttu-id="a26ce-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="a26ce-120">Type</span></span>   |<span data-ttu-id="a26ce-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a26ce-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a26ce-122">startDateTime</span><span class="sxs-lookup"><span data-stu-id="a26ce-122">startDateTime</span></span>|<span data-ttu-id="a26ce-123">String</span><span class="sxs-lookup"><span data-stu-id="a26ce-123">String</span></span>|<span data-ttu-id="a26ce-p102">Fecha y hora de inicio del evento para el que se configura el aviso. El valor se representa en formato ISO 8601, por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="a26ce-p102">The start date and time of the event for which the reminder is set up. The value is represented in ISO 8601 format, for example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="a26ce-126">endDateTime</span><span class="sxs-lookup"><span data-stu-id="a26ce-126">endDateTime</span></span>|<span data-ttu-id="a26ce-127">String</span><span class="sxs-lookup"><span data-stu-id="a26ce-127">String</span></span>|<span data-ttu-id="a26ce-p103">Fecha y hora de finalización del evento para el que se configura el aviso. El valor se representa en formato ISO 8601, por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="a26ce-p103">The end date and time of the event for which the reminder is set up. The value is represented in ISO 8601 format, for example, "2015-11-08T20:00:00.0000000".</span></span>|

## <a name="request-headers"></a><span data-ttu-id="a26ce-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a26ce-130">Request headers</span></span>
| <span data-ttu-id="a26ce-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a26ce-131">Header</span></span>       | <span data-ttu-id="a26ce-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a26ce-132">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="a26ce-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="a26ce-133">Authorization</span></span>  | <span data-ttu-id="a26ce-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a26ce-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a26ce-136">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a26ce-136">Content-Type</span></span>   | <span data-ttu-id="a26ce-137">application/json</span><span class="sxs-lookup"><span data-stu-id="a26ce-137">application/json</span></span> |
| <span data-ttu-id="a26ce-138">Prefer</span><span class="sxs-lookup"><span data-stu-id="a26ce-138">Prefer</span></span> | <span data-ttu-id="a26ce-p105">{Zona horaria}. Opcional, se supone la hora UTC si no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="a26ce-p105">{Time-zone}. Optional, UTC assumed if absent.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a26ce-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a26ce-141">Request body</span></span>
<span data-ttu-id="a26ce-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a26ce-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a26ce-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a26ce-143">Response</span></span>

<span data-ttu-id="a26ce-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [reminder](../resources/reminder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a26ce-144">If successful, this method returns `200 OK` response code and [reminder](../resources/reminder.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a26ce-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a26ce-145">Example</span></span>
<span data-ttu-id="a26ce-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a26ce-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a26ce-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a26ce-147">Request</span></span>
<span data-ttu-id="a26ce-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a26ce-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_reminderview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/reminderView(startDateTime='2017-06-05T10:00:00.0000000',endDateTime='2017-06-11T11:00:00.0000000')
```

##### <a name="response"></a><span data-ttu-id="a26ce-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a26ce-149">Response</span></span>
<span data-ttu-id="a26ce-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a26ce-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(microsoft.graph.reminder)",
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