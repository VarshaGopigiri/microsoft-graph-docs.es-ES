---
title: List events
description: Recupera una lista de objetos event.
author: dkershaw10
ms.openlocfilehash: fdb996f9be5193c5f18e6adb7de0b16938221e58
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27355548"
---
# <a name="list-events"></a><span data-ttu-id="a96d0-103">List events</span><span class="sxs-lookup"><span data-stu-id="a96d0-103">List events</span></span>

> <span data-ttu-id="a96d0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a96d0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a96d0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a96d0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a96d0-106">Recupera una lista de objetos [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="a96d0-106">Retrieve a list of [event](../resources/event.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="a96d0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a96d0-107">Permissions</span></span>
<span data-ttu-id="a96d0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a96d0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a96d0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a96d0-110">Permission type</span></span>      | <span data-ttu-id="a96d0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a96d0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a96d0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a96d0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a96d0-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a96d0-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a96d0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a96d0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a96d0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a96d0-115">Not supported.</span></span>    |
|<span data-ttu-id="a96d0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a96d0-116">Application</span></span> | <span data-ttu-id="a96d0-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a96d0-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a96d0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a96d0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events
GET /groups/{id}/calendar/events
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a96d0-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a96d0-119">Optional query parameters</span></span>
<span data-ttu-id="a96d0-120">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a96d0-120">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a96d0-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a96d0-121">Request headers</span></span>
| <span data-ttu-id="a96d0-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="a96d0-122">Name</span></span>       | <span data-ttu-id="a96d0-123">Type</span><span class="sxs-lookup"><span data-stu-id="a96d0-123">Type</span></span> | <span data-ttu-id="a96d0-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a96d0-124">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="a96d0-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="a96d0-125">Authorization</span></span>  | <span data-ttu-id="a96d0-126">string</span><span class="sxs-lookup"><span data-stu-id="a96d0-126">string</span></span> | <span data-ttu-id="a96d0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a96d0-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a96d0-129">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="a96d0-129">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="a96d0-130">string</span><span class="sxs-lookup"><span data-stu-id="a96d0-130">string</span></span> | <span data-ttu-id="a96d0-131">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a96d0-131">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="a96d0-132">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="a96d0-132">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="a96d0-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a96d0-133">Optional.</span></span> |
| <span data-ttu-id="a96d0-134">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="a96d0-134">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="a96d0-135">string</span><span class="sxs-lookup"><span data-stu-id="a96d0-135">string</span></span> | <span data-ttu-id="a96d0-136">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="a96d0-136">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="a96d0-137">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="a96d0-137">Values can be "text" or "html".</span></span> <span data-ttu-id="a96d0-138">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="a96d0-138">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="a96d0-139">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="a96d0-139">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="a96d0-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a96d0-140">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a96d0-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a96d0-141">Request body</span></span>
<span data-ttu-id="a96d0-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a96d0-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a96d0-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a96d0-143">Response</span></span>
<span data-ttu-id="a96d0-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos de [evento](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a96d0-144">If successful, this method returns a `200 OK` response code and a collection of [event](../resources/event.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a96d0-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a96d0-145">Example</span></span>
#### <a name="request"></a><span data-ttu-id="a96d0-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a96d0-146">Request</span></span>
<span data-ttu-id="a96d0-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a96d0-147">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group_events"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/events
```

#### <a name="response"></a><span data-ttu-id="a96d0-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a96d0-148">Response</span></span>
<span data-ttu-id="a96d0-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a96d0-149">The following is an example of the response.</span></span>
><span data-ttu-id="a96d0-150">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a96d0-150">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="a96d0-151">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a96d0-151">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 354

{
  "value": [
    {
      "originalStartTimeZone": "originalStartTimeZone-value",
      "originalEndTimeZone": "originalEndTimeZone-value",
      "responseStatus": {
        "response": "",
        "time": "2016-10-19T10:37:00Z"
      },
      "uid": "iCalUId-value",
      "reminderMinutesBeforeStart": 99,
      "isReminderOn": true
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List group events",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
