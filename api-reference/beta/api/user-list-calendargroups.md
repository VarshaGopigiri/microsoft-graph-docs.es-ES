---
title: List calendarGroups
description: Obtiene los grupos de calendarios del usuario.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 646a2566c11778282e5473258f867143b85a88ef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925395"
---
# <a name="list-calendargroups"></a><span data-ttu-id="65f71-103">List calendarGroups</span><span class="sxs-lookup"><span data-stu-id="65f71-103">List calendarGroups</span></span>

> <span data-ttu-id="65f71-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="65f71-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="65f71-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="65f71-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="65f71-106">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="65f71-106">Get the user's calendar groups.</span></span>
## <a name="permissions"></a><span data-ttu-id="65f71-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="65f71-107">Permissions</span></span>
<span data-ttu-id="65f71-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="65f71-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="65f71-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65f71-110">Permission type</span></span>      | <span data-ttu-id="65f71-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65f71-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="65f71-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="65f71-112">Delegated (work or school account)</span></span> | <span data-ttu-id="65f71-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="65f71-113">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="65f71-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="65f71-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="65f71-115">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="65f71-115">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="65f71-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="65f71-116">Application</span></span> | <span data-ttu-id="65f71-117">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="65f71-117">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="65f71-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65f71-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/calendarGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="65f71-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="65f71-119">Optional query parameters</span></span>
<span data-ttu-id="65f71-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65f71-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="65f71-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="65f71-121">Request headers</span></span>
| <span data-ttu-id="65f71-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65f71-122">Header</span></span>       | <span data-ttu-id="65f71-123">Valor</span><span class="sxs-lookup"><span data-stu-id="65f71-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="65f71-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="65f71-124">Authorization</span></span>  | <span data-ttu-id="65f71-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="65f71-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="65f71-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="65f71-127">Content-Type</span></span>  | <span data-ttu-id="65f71-128">application/json</span><span class="sxs-lookup"><span data-stu-id="65f71-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="65f71-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="65f71-129">Request body</span></span>
<span data-ttu-id="65f71-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="65f71-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="65f71-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65f71-131">Response</span></span>

<span data-ttu-id="65f71-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65f71-132">If successful, this method returns a `200 OK` response code and collection of [CalendarGroup](../resources/calendargroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="65f71-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65f71-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="65f71-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="65f71-134">Request</span></span>
<span data-ttu-id="65f71-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="65f71-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendargroups"
}-->
```http
GET https://graph.microsoft.com/beta/me/calendarGroups
```
##### <a name="response"></a><span data-ttu-id="65f71-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65f71-136">Response</span></span>
<span data-ttu-id="65f71-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="65f71-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 155

{
  "value": [
    {
      "name": "name-value",
      "classId": "classId-value",
      "changeKey": "changeKey-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List calendarGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
