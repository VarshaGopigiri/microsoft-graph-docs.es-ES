---
title: List calendarGroups
description: Obtiene los grupos de calendarios del usuario.
ms.openlocfilehash: 5afdac039ad4e03eb61776c5a3eed92fee2bd577
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029042"
---
# <a name="list-calendargroups"></a><span data-ttu-id="af752-103">List calendarGroups</span><span class="sxs-lookup"><span data-stu-id="af752-103">List calendarGroups</span></span>

<span data-ttu-id="af752-104">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="af752-104">Get the user's calendar groups.</span></span>
## <a name="permissions"></a><span data-ttu-id="af752-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="af752-105">Permissions</span></span>
<span data-ttu-id="af752-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="af752-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="af752-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="af752-108">Permission type</span></span>      | <span data-ttu-id="af752-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="af752-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="af752-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="af752-110">Delegated (work or school account)</span></span> | <span data-ttu-id="af752-111">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="af752-111">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="af752-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="af752-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="af752-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="af752-113">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="af752-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="af752-114">Application</span></span> | <span data-ttu-id="af752-115">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="af752-115">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="af752-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="af752-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/calendarGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="af752-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="af752-117">Optional query parameters</span></span>
<span data-ttu-id="af752-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="af752-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="af752-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="af752-119">Request headers</span></span>
| <span data-ttu-id="af752-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af752-120">Header</span></span>       | <span data-ttu-id="af752-121">Valor</span><span class="sxs-lookup"><span data-stu-id="af752-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="af752-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="af752-122">Authorization</span></span>  | <span data-ttu-id="af752-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="af752-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="af752-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="af752-125">Content-Type</span></span>  | <span data-ttu-id="af752-126">application/json</span><span class="sxs-lookup"><span data-stu-id="af752-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="af752-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="af752-127">Request body</span></span>
<span data-ttu-id="af752-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="af752-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="af752-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="af752-129">Response</span></span>

<span data-ttu-id="af752-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="af752-130">If successful, this method returns a `200 OK` response code and collection of [CalendarGroup](../resources/calendargroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="af752-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="af752-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="af752-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="af752-132">Request</span></span>
<span data-ttu-id="af752-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="af752-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendargroups"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups
```
##### <a name="response"></a><span data-ttu-id="af752-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="af752-134">Response</span></span>
<span data-ttu-id="af752-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="af752-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
