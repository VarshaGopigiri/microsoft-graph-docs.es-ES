---
title: List calendars
description: Recupera una lista de calendarios que pertenecen a un grupo de calendarios.
ms.openlocfilehash: af4ad93d0544fa90bbf9ae8dd31c7907ef7bc1bf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029112"
---
# <a name="list-calendars"></a><span data-ttu-id="72825-103">List calendars</span><span class="sxs-lookup"><span data-stu-id="72825-103">List calendars</span></span>

<span data-ttu-id="72825-104">Recupera una lista de calendarios que pertenecen a un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="72825-104">Retrieve a list of calendars belonging to a calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="72825-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="72825-105">Permissions</span></span>

<span data-ttu-id="72825-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="72825-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="72825-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="72825-108">Permission type</span></span>                        | <span data-ttu-id="72825-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="72825-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="72825-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="72825-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="72825-111">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="72825-111">Calendars.Read</span></span>                              |
| <span data-ttu-id="72825-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="72825-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="72825-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="72825-113">Calendars.Read</span></span>                              |
| <span data-ttu-id="72825-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="72825-114">Application</span></span>                            | <span data-ttu-id="72825-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="72825-115">Calendars.Read</span></span>                              |

## <a name="http-request"></a><span data-ttu-id="72825-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="72825-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="72825-117">[calendarGroup](../resources/calendargroup.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="72825-117">A user's default [calendarGroup](../resources/calendargroup.md).</span></span>

```http
GET /me/calendarGroup/calendars
GET /users/{id | userPrincipalName}/calendarGroup/calendars
```

<span data-ttu-id="72825-118">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="72825-118">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
GET /me/calendarGroups/{id}/calendars
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars
```

## <a name="optional-query-parameters"></a><span data-ttu-id="72825-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="72825-119">Optional query parameters</span></span>

<span data-ttu-id="72825-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72825-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="72825-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="72825-121">Request headers</span></span>

| <span data-ttu-id="72825-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="72825-122">Name</span></span>          | <span data-ttu-id="72825-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="72825-123">Type</span></span>   | <span data-ttu-id="72825-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="72825-124">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="72825-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="72825-125">Authorization</span></span> | <span data-ttu-id="72825-126">string</span><span class="sxs-lookup"><span data-stu-id="72825-126">string</span></span> | <span data-ttu-id="72825-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="72825-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="72825-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="72825-129">Request body</span></span>

<span data-ttu-id="72825-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="72825-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="72825-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72825-131">Response</span></span>

<span data-ttu-id="72825-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72825-132">If successful, this method returns a `200 OK` response code and collection of [Calendar](../resources/calendar.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="72825-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72825-133">Example</span></span>

##### <a name="request"></a><span data-ttu-id="72825-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="72825-134">Request</span></span>

<span data-ttu-id="72825-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="72825-135">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendars"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups/{id}/calendars
```

##### <a name="response"></a><span data-ttu-id="72825-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72825-136">Response</span></span>

<span data-ttu-id="72825-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="72825-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 147

{
  "value": [
    {
      "name": "name-value",
      "color": {
      },
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
  "description": "List calendars",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
