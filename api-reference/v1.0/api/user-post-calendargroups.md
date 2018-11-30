---
title: Create CalendarGroup
description: Usa esta API para crear un objeto CalendarGroup.
ms.openlocfilehash: 523a9245c57878dc618b778b968d28c41fc7cd45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029239"
---
# <a name="create-calendargroup"></a><span data-ttu-id="55999-103">Create CalendarGroup</span><span class="sxs-lookup"><span data-stu-id="55999-103">Create CalendarGroup</span></span>

<span data-ttu-id="55999-104">Usa esta API para crear un objeto CalendarGroup.</span><span class="sxs-lookup"><span data-stu-id="55999-104">Use this API to create a new CalendarGroup.</span></span>
## <a name="permissions"></a><span data-ttu-id="55999-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="55999-105">Permissions</span></span>
<span data-ttu-id="55999-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="55999-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="55999-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55999-108">Permission type</span></span>      | <span data-ttu-id="55999-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55999-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="55999-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55999-110">Delegated (work or school account)</span></span> | <span data-ttu-id="55999-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="55999-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="55999-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55999-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="55999-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="55999-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="55999-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55999-114">Application</span></span> | <span data-ttu-id="55999-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="55999-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="55999-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55999-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/calendarGroups
```
## <a name="request-headers"></a><span data-ttu-id="55999-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55999-117">Request headers</span></span>
| <span data-ttu-id="55999-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55999-118">Header</span></span>       | <span data-ttu-id="55999-119">Valor</span><span class="sxs-lookup"><span data-stu-id="55999-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="55999-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="55999-120">Authorization</span></span>  | <span data-ttu-id="55999-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55999-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="55999-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="55999-123">Content-Type</span></span>  | <span data-ttu-id="55999-124">application/json</span><span class="sxs-lookup"><span data-stu-id="55999-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="55999-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55999-125">Request body</span></span>
<span data-ttu-id="55999-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [CalendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="55999-126">In the request body, supply a JSON representation of [CalendarGroup](../resources/calendargroup.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="55999-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55999-127">Response</span></span>

<span data-ttu-id="55999-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55999-128">If successful, this method returns `201 Created` response code and [CalendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55999-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55999-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="55999-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55999-130">Request</span></span>
<span data-ttu-id="55999-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55999-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_calendargroup_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/calendarGroups
Content-type: application/json
Content-length: 90

{
  "name": "name-value",
  "classId": "classId-value",
  "changeKey": "changeKey-value"
}
```
<span data-ttu-id="55999-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="55999-132">In the request body, supply a JSON representation of [calendarGroup](../resources/calendargroup.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="55999-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55999-133">Response</span></span>
<span data-ttu-id="55999-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="55999-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
