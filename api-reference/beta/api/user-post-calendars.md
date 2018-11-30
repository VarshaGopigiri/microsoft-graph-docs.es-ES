---
title: Create Calendar
description: Use esta API para crear un calendario para un usuario.
ms.openlocfilehash: 7cb1dbf60cacfb86ee79d9cf9d344dae878fd1f0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084798"
---
# <a name="create-calendar"></a><span data-ttu-id="10594-103">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="10594-103">Create Calendar</span></span>

> <span data-ttu-id="10594-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="10594-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="10594-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="10594-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="10594-106">Use esta API para crear un calendario para un [usuario](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="10594-106">Use this API to create a new calendar for a [user](../resources/user.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="10594-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="10594-107">Permissions</span></span>
<span data-ttu-id="10594-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="10594-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="10594-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="10594-110">Permission type</span></span>      | <span data-ttu-id="10594-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="10594-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="10594-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="10594-112">Delegated (work or school account)</span></span> | <span data-ttu-id="10594-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="10594-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="10594-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="10594-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="10594-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="10594-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="10594-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="10594-116">Application</span></span> | <span data-ttu-id="10594-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="10594-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="10594-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="10594-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/calendars
```
## <a name="request-headers"></a><span data-ttu-id="10594-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="10594-119">Request headers</span></span>
| <span data-ttu-id="10594-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10594-120">Header</span></span>       | <span data-ttu-id="10594-121">Valor</span><span class="sxs-lookup"><span data-stu-id="10594-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="10594-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="10594-122">Authorization</span></span>  | <span data-ttu-id="10594-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="10594-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="10594-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="10594-125">Content-Type</span></span>  | <span data-ttu-id="10594-126">application/json</span><span class="sxs-lookup"><span data-stu-id="10594-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="10594-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="10594-127">Request body</span></span>
<span data-ttu-id="10594-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="10594-128">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="10594-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10594-129">Response</span></span>

<span data-ttu-id="10594-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10594-130">If successful, this method returns `201 Created` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="10594-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="10594-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="10594-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="10594-132">Request</span></span>
<span data-ttu-id="10594-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="10594-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_calendar_from_user"
}-->
```http
POST https://graph.microsoft.com/beta/me/calendars
Content-type: application/json

{
  "name": "Volunteer"
}

```
<span data-ttu-id="10594-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="10594-134">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="10594-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10594-135">Response</span></span>
<span data-ttu-id="10594-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="10594-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#me/calendars/$entity",
    "@odata.id":"https://graph.microsoft.com/beta/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/calendars('AAMkADJmMVAAA=')",
    "id":"AAMkADJmMVAAA=",
    "name":"Volunteer",
    "color":"auto",
    "isDefaultCalendar":false,
    "changeKey":"DxYSthXJXEWwAQSYQnXvIgAAIxGttg==",
    "canShare":true,
    "canViewPrivateItems":true,
    "hexColor": "",
    "isShared":false,
    "isSharedWithMe":false,
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