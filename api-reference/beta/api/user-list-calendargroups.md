---
title: List calendarGroups
description: Obtiene los grupos de calendarios del usuario.
ms.openlocfilehash: 560dd09d42b59e68b6282d7dec4305f7b10ea9f2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091045"
---
# <a name="list-calendargroups"></a><span data-ttu-id="d61b2-103">List calendarGroups</span><span class="sxs-lookup"><span data-stu-id="d61b2-103">List calendarGroups</span></span>

> <span data-ttu-id="d61b2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d61b2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d61b2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d61b2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d61b2-106">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="d61b2-106">Get the user's calendar groups.</span></span>
## <a name="permissions"></a><span data-ttu-id="d61b2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d61b2-107">Permissions</span></span>
<span data-ttu-id="d61b2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d61b2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d61b2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d61b2-110">Permission type</span></span>      | <span data-ttu-id="d61b2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d61b2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d61b2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d61b2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d61b2-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d61b2-113">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d61b2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d61b2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d61b2-115">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d61b2-115">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d61b2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d61b2-116">Application</span></span> | <span data-ttu-id="d61b2-117">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d61b2-117">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d61b2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d61b2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/calendarGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d61b2-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d61b2-119">Optional query parameters</span></span>
<span data-ttu-id="d61b2-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d61b2-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="d61b2-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d61b2-121">Request headers</span></span>
| <span data-ttu-id="d61b2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d61b2-122">Header</span></span>       | <span data-ttu-id="d61b2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d61b2-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d61b2-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="d61b2-124">Authorization</span></span>  | <span data-ttu-id="d61b2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d61b2-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d61b2-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d61b2-127">Content-Type</span></span>  | <span data-ttu-id="d61b2-128">application/json</span><span class="sxs-lookup"><span data-stu-id="d61b2-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d61b2-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d61b2-129">Request body</span></span>
<span data-ttu-id="d61b2-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d61b2-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d61b2-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d61b2-131">Response</span></span>

<span data-ttu-id="d61b2-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d61b2-132">If successful, this method returns a `200 OK` response code and collection of [CalendarGroup](../resources/calendargroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d61b2-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d61b2-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d61b2-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d61b2-134">Request</span></span>
<span data-ttu-id="d61b2-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d61b2-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendargroups"
}-->
```http
GET https://graph.microsoft.com/beta/me/calendarGroups
```
##### <a name="response"></a><span data-ttu-id="d61b2-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d61b2-136">Response</span></span>
<span data-ttu-id="d61b2-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d61b2-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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