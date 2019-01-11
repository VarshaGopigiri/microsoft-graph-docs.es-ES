---
title: List calendars
description: Recupera una lista de calendarios que pertenecen a un grupo de calendarios.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 9ffa22a25fcc5c42ca9a61ea09a5cc68d2f3351b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814206"
---
# <a name="list-calendars"></a><span data-ttu-id="91e1e-103">List calendars</span><span class="sxs-lookup"><span data-stu-id="91e1e-103">List calendars</span></span>

> <span data-ttu-id="91e1e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="91e1e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="91e1e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="91e1e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="91e1e-106">Recupera una lista de calendarios que pertenecen a un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="91e1e-106">Retrieve a list of calendars belonging to a calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="91e1e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="91e1e-107">Permissions</span></span>

<span data-ttu-id="91e1e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="91e1e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="91e1e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="91e1e-110">Permission type</span></span>                        | <span data-ttu-id="91e1e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="91e1e-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="91e1e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="91e1e-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="91e1e-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="91e1e-113">Calendars.Read</span></span>                              |
| <span data-ttu-id="91e1e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="91e1e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="91e1e-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="91e1e-115">Calendars.Read</span></span>                              |
| <span data-ttu-id="91e1e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="91e1e-116">Application</span></span>                            | <span data-ttu-id="91e1e-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="91e1e-117">Calendars.Read</span></span>                              |

## <a name="http-request"></a><span data-ttu-id="91e1e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="91e1e-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="91e1e-119">[calendarGroup](../resources/calendargroup.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="91e1e-119">A user's default [calendarGroup](../resources/calendargroup.md).</span></span>

```http
GET /me/calendarGroup/calendars
GET /users/{id | userPrincipalName}/calendarGroup/calendars
```

<span data-ttu-id="91e1e-120">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="91e1e-120">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
GET /me/calendarGroups/{id}/calendars
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars
```

## <a name="optional-query-parameters"></a><span data-ttu-id="91e1e-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="91e1e-121">Optional query parameters</span></span>

<span data-ttu-id="91e1e-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91e1e-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="91e1e-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="91e1e-123">Request headers</span></span>

| <span data-ttu-id="91e1e-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="91e1e-124">Name</span></span>          | <span data-ttu-id="91e1e-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="91e1e-125">Type</span></span>   | <span data-ttu-id="91e1e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="91e1e-126">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="91e1e-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="91e1e-127">Authorization</span></span> | <span data-ttu-id="91e1e-128">string</span><span class="sxs-lookup"><span data-stu-id="91e1e-128">string</span></span> | <span data-ttu-id="91e1e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="91e1e-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="91e1e-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="91e1e-131">Request body</span></span>

<span data-ttu-id="91e1e-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="91e1e-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="91e1e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91e1e-133">Response</span></span>

<span data-ttu-id="91e1e-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91e1e-134">If successful, this method returns a `200 OK` response code and collection of [Calendar](../resources/calendar.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="91e1e-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="91e1e-135">Example</span></span>

##### <a name="request"></a><span data-ttu-id="91e1e-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="91e1e-136">Request</span></span>

<span data-ttu-id="91e1e-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="91e1e-137">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendars"
}-->

```http
GET https://graph.microsoft.com/beta/me/calendarGroups/{id}/calendars
```

##### <a name="response"></a><span data-ttu-id="91e1e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91e1e-138">Response</span></span>

<span data-ttu-id="91e1e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="91e1e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
