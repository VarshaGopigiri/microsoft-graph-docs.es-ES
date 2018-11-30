---
title: Create Calendar
description: Use esta API para crear un calendario para un usuario.
ms.openlocfilehash: 8ffa88331478d7bbbe1e94c87d58505041d63d41
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032099"
---
# <a name="create-calendar"></a><span data-ttu-id="ef807-103">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="ef807-103">Create Calendar</span></span>

<span data-ttu-id="ef807-104">Use esta API para crear un calendario para un [usuario](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="ef807-104">Use this API to create a new calendar for a [user](../resources/user.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="ef807-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ef807-105">Permissions</span></span>
<span data-ttu-id="ef807-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ef807-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ef807-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ef807-108">Permission type</span></span>      | <span data-ttu-id="ef807-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ef807-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ef807-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ef807-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ef807-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ef807-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="ef807-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ef807-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ef807-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ef807-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="ef807-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ef807-114">Application</span></span> | <span data-ttu-id="ef807-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ef807-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ef807-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef807-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/calendars
```
## <a name="request-headers"></a><span data-ttu-id="ef807-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef807-117">Request headers</span></span>
| <span data-ttu-id="ef807-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef807-118">Header</span></span>       | <span data-ttu-id="ef807-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ef807-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ef807-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ef807-120">Authorization</span></span>  | <span data-ttu-id="ef807-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ef807-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ef807-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ef807-123">Content-Type</span></span>  | <span data-ttu-id="ef807-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ef807-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ef807-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef807-125">Request body</span></span>
<span data-ttu-id="ef807-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="ef807-126">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="ef807-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef807-127">Response</span></span>

<span data-ttu-id="ef807-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef807-128">If successful, this method returns `201 Created` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ef807-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef807-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ef807-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef807-130">Request</span></span>
<span data-ttu-id="ef807-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef807-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_calendar_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/calendars
Content-type: application/json

{
  "name": "Volunteer"
}
```
<span data-ttu-id="ef807-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="ef807-132">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="ef807-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef807-133">Response</span></span>
<span data-ttu-id="ef807-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ef807-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#me/calendars/$entity",
    "@odata.id":"https://graph.microsoft.com/v1.0/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/calendars('AAMkADJmMVAAA=')",
    "id":"AAMkADJmMVAAA=",
    "name":"Volunteer",
    "color":"auto",
    "changeKey":"DxYSthXJXEWwAQSYQnXvIgAAIxGttg==",
    "canShare":true,
    "canViewPrivateItems":true,
    "canEdit":true,
    "owner":{
        "name":"Samantha Booth",
        "address":"samanthab@adatum.onmicrosoft.com"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
