---
title: Create CalendarGroup
description: Usa esta API para crear un objeto CalendarGroup.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 1f4b720f8d293c9803c25a32329c3d4bb8ee7bf7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990211"
---
# <a name="create-calendargroup"></a><span data-ttu-id="d2202-103">Create CalendarGroup</span><span class="sxs-lookup"><span data-stu-id="d2202-103">Create CalendarGroup</span></span>

> <span data-ttu-id="d2202-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d2202-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d2202-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d2202-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d2202-106">Usa esta API para crear un objeto CalendarGroup.</span><span class="sxs-lookup"><span data-stu-id="d2202-106">Use this API to create a new CalendarGroup.</span></span>
## <a name="permissions"></a><span data-ttu-id="d2202-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2202-107">Permissions</span></span>
<span data-ttu-id="d2202-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2202-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2202-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2202-110">Permission type</span></span>      | <span data-ttu-id="d2202-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2202-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2202-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2202-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d2202-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2202-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d2202-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2202-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2202-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2202-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d2202-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2202-116">Application</span></span> | <span data-ttu-id="d2202-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2202-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2202-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2202-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/calendarGroups
```
## <a name="request-headers"></a><span data-ttu-id="d2202-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2202-119">Request headers</span></span>
| <span data-ttu-id="d2202-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2202-120">Header</span></span>       | <span data-ttu-id="d2202-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d2202-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d2202-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2202-122">Authorization</span></span>  | <span data-ttu-id="d2202-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2202-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d2202-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d2202-125">Content-Type</span></span>  | <span data-ttu-id="d2202-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d2202-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d2202-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2202-127">Request body</span></span>
<span data-ttu-id="d2202-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [CalendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="d2202-128">In the request body, supply a JSON representation of [CalendarGroup](../resources/calendargroup.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="d2202-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2202-129">Response</span></span>

<span data-ttu-id="d2202-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2202-130">If successful, this method returns `201 Created` response code and [CalendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2202-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2202-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d2202-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2202-132">Request</span></span>
<span data-ttu-id="d2202-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2202-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_calendargroup_from_user"
}-->
```http
POST https://graph.microsoft.com/beta/me/calendarGroups
Content-type: application/json
Content-length: 90

{
  "name": "name-value",
  "classId": "classId-value",
  "changeKey": "changeKey-value"
}
```
<span data-ttu-id="d2202-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="d2202-134">In the request body, supply a JSON representation of [calendarGroup](../resources/calendargroup.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="d2202-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2202-135">Response</span></span>
<span data-ttu-id="d2202-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2202-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 110

{
  "name": "name-value",
  "classId": "classId-value",
  "changeKey": "changeKey-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create CalendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
