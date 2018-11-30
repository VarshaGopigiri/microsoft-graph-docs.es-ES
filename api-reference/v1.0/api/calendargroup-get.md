---
title: Get calendarGroup
description: Recupera las propiedades y relaciones de un objeto de grupo de calendarios.
ms.openlocfilehash: ffaf4fa4fbc96649bb93a430e77be758e8768ceb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031104"
---
# <a name="get-calendargroup"></a><span data-ttu-id="8a8bb-103">Get calendarGroup</span><span class="sxs-lookup"><span data-stu-id="8a8bb-103">Get calendarGroup</span></span>

<span data-ttu-id="8a8bb-104">Recupera las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="8a8bb-104">Retrieve the properties and relationships of a calendar group object.</span></span>

## <a name="permissions"></a><span data-ttu-id="8a8bb-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="8a8bb-105">Permissions</span></span>

<span data-ttu-id="8a8bb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8a8bb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="8a8bb-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a8bb-108">Permission type</span></span>                        | <span data-ttu-id="8a8bb-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a8bb-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="8a8bb-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a8bb-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="8a8bb-111">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="8a8bb-111">Calendars.Read</span></span>                              |
| <span data-ttu-id="8a8bb-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a8bb-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8a8bb-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="8a8bb-113">Calendars.Read</span></span>                              |
| <span data-ttu-id="8a8bb-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a8bb-114">Application</span></span>                            | <span data-ttu-id="8a8bb-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="8a8bb-115">Calendars.Read</span></span>                              |

## <a name="http-request"></a><span data-ttu-id="8a8bb-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a8bb-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="8a8bb-117">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8a8bb-117">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
GET /me/calendarGroups/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8a8bb-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8a8bb-118">Optional query parameters</span></span>

<span data-ttu-id="8a8bb-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a8bb-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8a8bb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a8bb-120">Request headers</span></span>

| <span data-ttu-id="8a8bb-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="8a8bb-121">Name</span></span>          | <span data-ttu-id="8a8bb-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a8bb-122">Type</span></span>   | <span data-ttu-id="8a8bb-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a8bb-123">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="8a8bb-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="8a8bb-124">Authorization</span></span> | <span data-ttu-id="8a8bb-125">string</span><span class="sxs-lookup"><span data-stu-id="8a8bb-125">string</span></span> | <span data-ttu-id="8a8bb-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a8bb-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8a8bb-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a8bb-128">Request body</span></span>

<span data-ttu-id="8a8bb-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8a8bb-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8a8bb-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a8bb-130">Response</span></span>

<span data-ttu-id="8a8bb-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a8bb-131">If successful, this method returns a `200 OK` response code and [calendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a8bb-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a8bb-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="8a8bb-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a8bb-133">Request</span></span>

<span data-ttu-id="8a8bb-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a8bb-134">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendargroup"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="8a8bb-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a8bb-135">Response</span></span>

<span data-ttu-id="8a8bb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a8bb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 110

{
  "name": "name-value",
  "classId": "11b0131d-43c8-4bbb-b2c8-e80f9a50834a",
  "changeKey": "changeKey-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "Get calendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
