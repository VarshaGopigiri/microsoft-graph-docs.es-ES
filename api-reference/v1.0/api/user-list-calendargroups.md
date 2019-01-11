---
title: List calendarGroups
description: Obtiene los grupos de calendarios del usuario.
localization_priority: Normal
ms.openlocfilehash: 932fa9767ecd8ff6957cad825ad4a2864500d41a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808725"
---
# <a name="list-calendargroups"></a><span data-ttu-id="c0582-103">List calendarGroups</span><span class="sxs-lookup"><span data-stu-id="c0582-103">List calendarGroups</span></span>

<span data-ttu-id="c0582-104">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="c0582-104">Get the user's calendar groups.</span></span>
## <a name="permissions"></a><span data-ttu-id="c0582-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c0582-105">Permissions</span></span>
<span data-ttu-id="c0582-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0582-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c0582-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0582-108">Permission type</span></span>      | <span data-ttu-id="c0582-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0582-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c0582-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0582-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c0582-111">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c0582-111">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="c0582-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0582-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0582-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c0582-113">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="c0582-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0582-114">Application</span></span> | <span data-ttu-id="c0582-115">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c0582-115">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c0582-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0582-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/calendarGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c0582-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c0582-117">Optional query parameters</span></span>
<span data-ttu-id="c0582-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0582-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c0582-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0582-119">Request headers</span></span>
| <span data-ttu-id="c0582-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0582-120">Header</span></span>       | <span data-ttu-id="c0582-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c0582-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c0582-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c0582-122">Authorization</span></span>  | <span data-ttu-id="c0582-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0582-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c0582-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c0582-125">Content-Type</span></span>  | <span data-ttu-id="c0582-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c0582-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c0582-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0582-127">Request body</span></span>
<span data-ttu-id="c0582-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c0582-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c0582-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0582-129">Response</span></span>

<span data-ttu-id="c0582-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0582-130">If successful, this method returns a `200 OK` response code and collection of [CalendarGroup](../resources/calendargroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c0582-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0582-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c0582-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0582-132">Request</span></span>
<span data-ttu-id="c0582-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0582-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendargroups"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups
```
##### <a name="response"></a><span data-ttu-id="c0582-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0582-134">Response</span></span>
<span data-ttu-id="c0582-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c0582-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
