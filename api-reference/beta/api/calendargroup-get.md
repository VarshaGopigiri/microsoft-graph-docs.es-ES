---
title: Get calendarGroup
description: Recupera las propiedades y relaciones de un objeto de grupo de calendarios.
ms.openlocfilehash: 0fdaefb75e2b93f84e2f7351b3067fdad2e01c58
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084646"
---
# <a name="get-calendargroup"></a><span data-ttu-id="77a81-103">Get calendarGroup</span><span class="sxs-lookup"><span data-stu-id="77a81-103">Get calendarGroup</span></span>

> <span data-ttu-id="77a81-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77a81-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77a81-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77a81-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="77a81-106">Recupera las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="77a81-106">Retrieve the properties and relationships of a calendar group object.</span></span>

## <a name="permissions"></a><span data-ttu-id="77a81-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="77a81-107">Permissions</span></span>

<span data-ttu-id="77a81-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77a81-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="77a81-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77a81-110">Permission type</span></span>                        | <span data-ttu-id="77a81-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77a81-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="77a81-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77a81-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="77a81-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="77a81-113">Calendars.Read</span></span>                              |
| <span data-ttu-id="77a81-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77a81-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="77a81-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="77a81-115">Calendars.Read</span></span>                              |
| <span data-ttu-id="77a81-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77a81-116">Application</span></span>                            | <span data-ttu-id="77a81-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="77a81-117">Calendars.Read</span></span>                              |

## <a name="http-request"></a><span data-ttu-id="77a81-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77a81-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="77a81-119">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="77a81-119">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
GET /me/calendarGroups/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="77a81-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="77a81-120">Optional query parameters</span></span>

<span data-ttu-id="77a81-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77a81-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="77a81-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77a81-122">Request headers</span></span>

| <span data-ttu-id="77a81-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="77a81-123">Name</span></span>          | <span data-ttu-id="77a81-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="77a81-124">Type</span></span>   | <span data-ttu-id="77a81-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="77a81-125">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="77a81-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="77a81-126">Authorization</span></span> | <span data-ttu-id="77a81-127">string</span><span class="sxs-lookup"><span data-stu-id="77a81-127">string</span></span> | <span data-ttu-id="77a81-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77a81-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="77a81-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77a81-130">Request body</span></span>

<span data-ttu-id="77a81-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="77a81-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="77a81-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77a81-132">Response</span></span>

<span data-ttu-id="77a81-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77a81-133">If successful, this method returns a `200 OK` response code and [calendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77a81-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77a81-134">Example</span></span>

##### <a name="request"></a><span data-ttu-id="77a81-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77a81-135">Request</span></span>

<span data-ttu-id="77a81-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77a81-136">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendargroup"
}-->

```http
GET https://graph.microsoft.com/beta/me/calendarGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="77a81-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77a81-137">Response</span></span>

<span data-ttu-id="77a81-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77a81-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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