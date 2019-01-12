---
title: Create CalendarGroup
description: Usa esta API para crear un objeto CalendarGroup.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: d4a65099101b3e32e92dc4ba1cad62ed265f161a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916127"
---
# <a name="create-calendargroup"></a><span data-ttu-id="162d9-103">Create CalendarGroup</span><span class="sxs-lookup"><span data-stu-id="162d9-103">Create CalendarGroup</span></span>

<span data-ttu-id="162d9-104">Usa esta API para crear un objeto CalendarGroup.</span><span class="sxs-lookup"><span data-stu-id="162d9-104">Use this API to create a new CalendarGroup.</span></span>
## <a name="permissions"></a><span data-ttu-id="162d9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="162d9-105">Permissions</span></span>
<span data-ttu-id="162d9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="162d9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="162d9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="162d9-108">Permission type</span></span>      | <span data-ttu-id="162d9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="162d9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="162d9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="162d9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="162d9-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="162d9-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="162d9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="162d9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="162d9-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="162d9-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="162d9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="162d9-114">Application</span></span> | <span data-ttu-id="162d9-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="162d9-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="162d9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="162d9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/calendarGroups
```
## <a name="request-headers"></a><span data-ttu-id="162d9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="162d9-117">Request headers</span></span>
| <span data-ttu-id="162d9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="162d9-118">Header</span></span>       | <span data-ttu-id="162d9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="162d9-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="162d9-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="162d9-120">Authorization</span></span>  | <span data-ttu-id="162d9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="162d9-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="162d9-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="162d9-123">Content-Type</span></span>  | <span data-ttu-id="162d9-124">application/json</span><span class="sxs-lookup"><span data-stu-id="162d9-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="162d9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="162d9-125">Request body</span></span>
<span data-ttu-id="162d9-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [CalendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="162d9-126">In the request body, supply a JSON representation of [CalendarGroup](../resources/calendargroup.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="162d9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="162d9-127">Response</span></span>

<span data-ttu-id="162d9-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="162d9-128">If successful, this method returns `201 Created` response code and [CalendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="162d9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="162d9-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="162d9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="162d9-130">Request</span></span>
<span data-ttu-id="162d9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="162d9-131">Here is an example of the request.</span></span>
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
<span data-ttu-id="162d9-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="162d9-132">In the request body, supply a JSON representation of [calendarGroup](../resources/calendargroup.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="162d9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="162d9-133">Response</span></span>
<span data-ttu-id="162d9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="162d9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
