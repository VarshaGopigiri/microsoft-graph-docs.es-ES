---
title: List calendars
description: 'Obtiene todos los calendarios del usuario (propiedad de navegación `/calendars`), los calendarios del grupo de calendarios predeterminado o de un grupo de calendarios específico. '
localization_priority: Normal
ms.openlocfilehash: c59ee99c900aa39221530473c9323dfcaab721b5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886522"
---
# <a name="list-calendars"></a><span data-ttu-id="f6199-103">List calendars</span><span class="sxs-lookup"><span data-stu-id="f6199-103">List calendars</span></span>

> <span data-ttu-id="f6199-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f6199-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f6199-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f6199-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f6199-106">Obtiene todos los calendarios del usuario (propiedad de navegación `/calendars`), los calendarios del grupo de calendarios predeterminado o de un grupo de calendarios específico.</span><span class="sxs-lookup"><span data-stu-id="f6199-106">Get all the user's calendars (`/calendars` navigation property), get the calendars from the default calendar group or from a specific calendar group.</span></span> 
## <a name="permissions"></a><span data-ttu-id="f6199-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f6199-107">Permissions</span></span>
<span data-ttu-id="f6199-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f6199-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f6199-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f6199-110">Permission type</span></span>      | <span data-ttu-id="f6199-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f6199-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f6199-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f6199-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f6199-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f6199-113">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="f6199-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f6199-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f6199-115">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f6199-115">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="f6199-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f6199-116">Application</span></span> | <span data-ttu-id="f6199-117">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f6199-117">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="f6199-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6199-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

<span data-ttu-id="f6199-119">Todos los calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="f6199-119">All the user's calendars.</span></span>
```http
GET /me/calendars
GET /users/{id | userPrincipalName}/calendars
```

<span data-ttu-id="f6199-120">Calendarios del usuario en el [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f6199-120">The user's calendars in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendargroups/{calendar_group_id}/calendars
GET /users/{id | userPrincipalName}/calendarGroup/calendars
```

<span data-ttu-id="f6199-121">Calendarios del usuario en un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="f6199-121">The user's calendars in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroups/{calendar_group_id}/calendars
GET /users/{id | userPrincipalName}/calendarGroups/{calendar_group_id}/calendars
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f6199-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f6199-122">Optional query parameters</span></span>
<span data-ttu-id="f6199-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6199-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f6199-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6199-124">Request headers</span></span>
| <span data-ttu-id="f6199-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6199-125">Header</span></span>       | <span data-ttu-id="f6199-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f6199-126">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f6199-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="f6199-127">Authorization</span></span>  | <span data-ttu-id="f6199-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f6199-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="f6199-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f6199-130">Content-Type</span></span>   | <span data-ttu-id="f6199-131">application/json</span><span class="sxs-lookup"><span data-stu-id="f6199-131">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="f6199-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6199-132">Request body</span></span>
<span data-ttu-id="f6199-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f6199-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f6199-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6199-134">Response</span></span>

<span data-ttu-id="f6199-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6199-135">If successful, this method returns a `200 OK` response code and collection of [Calendar](../resources/calendar.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f6199-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6199-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f6199-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6199-137">Request</span></span>
<span data-ttu-id="f6199-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6199-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendars"
}-->
```http
GET https://graph.microsoft.com/beta/me/calendars
```
##### <a name="response"></a><span data-ttu-id="f6199-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6199-139">Response</span></span>
<span data-ttu-id="f6199-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f6199-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#me/calendars",
    "value": [
        {
            "@odata.id": "https://graph.microsoft.com/beta/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/calendars('AAMkAGI2TGuLAAA=')",
            "id": "AAMkAGI2TGuLAAA=",
            "name": "Calendar",
            "color": "auto",
            "changeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w==",
            "isDefaultCalendar": true,
            "canShare":true,
            "canViewPrivateItems":true,
            "hexColor": "",
            "isShared":false,
            "isSharedWithMe":false,
            "canEdit":true,
            "owner":{
                "name":"Samantha Booth",
                "address":"samanthab@adatum.onmicrosoft.com"
            }
        }
    ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List calendars",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
