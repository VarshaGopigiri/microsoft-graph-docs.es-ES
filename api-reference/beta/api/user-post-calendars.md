---
title: Create Calendar
description: Use esta API para crear un calendario para un usuario.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 867641a47ca02e903c22a3338a0fe87f7c70bddf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887825"
---
# <a name="create-calendar"></a><span data-ttu-id="a45ad-103">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="a45ad-103">Create Calendar</span></span>

> <span data-ttu-id="a45ad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a45ad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a45ad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a45ad-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a45ad-106">Use esta API para crear un calendario para un [usuario](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="a45ad-106">Use this API to create a new calendar for a [user](../resources/user.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="a45ad-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a45ad-107">Permissions</span></span>
<span data-ttu-id="a45ad-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a45ad-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a45ad-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a45ad-110">Permission type</span></span>      | <span data-ttu-id="a45ad-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a45ad-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a45ad-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a45ad-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a45ad-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a45ad-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="a45ad-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a45ad-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a45ad-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a45ad-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="a45ad-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a45ad-116">Application</span></span> | <span data-ttu-id="a45ad-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a45ad-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a45ad-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a45ad-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/calendars
```
## <a name="request-headers"></a><span data-ttu-id="a45ad-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a45ad-119">Request headers</span></span>
| <span data-ttu-id="a45ad-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a45ad-120">Header</span></span>       | <span data-ttu-id="a45ad-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a45ad-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a45ad-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a45ad-122">Authorization</span></span>  | <span data-ttu-id="a45ad-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a45ad-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a45ad-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a45ad-125">Content-Type</span></span>  | <span data-ttu-id="a45ad-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a45ad-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a45ad-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a45ad-127">Request body</span></span>
<span data-ttu-id="a45ad-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="a45ad-128">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="a45ad-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a45ad-129">Response</span></span>

<span data-ttu-id="a45ad-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a45ad-130">If successful, this method returns `201 Created` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a45ad-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a45ad-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a45ad-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a45ad-132">Request</span></span>
<span data-ttu-id="a45ad-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a45ad-133">Here is an example of the request.</span></span>
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
<span data-ttu-id="a45ad-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="a45ad-134">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="a45ad-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a45ad-135">Response</span></span>
<span data-ttu-id="a45ad-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a45ad-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
