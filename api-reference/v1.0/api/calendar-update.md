---
title: Actualizar calendario
description: 'Actualiza las propiedades de un objeto de calendario. El calendario puede ser una de un usuario '
localization_priority: Normal
ms.openlocfilehash: f56ce185718c2a639f32606b9db79f0154a824e7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857116"
---
# <a name="update-calendar"></a><span data-ttu-id="6cf4b-104">Actualizar calendario</span><span class="sxs-lookup"><span data-stu-id="6cf4b-104">Update calendar</span></span>

<span data-ttu-id="6cf4b-105">Actualiza las propiedades de un objeto de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="6cf4b-105">Update the properties of of a [calendar](../resources/calendar.md) object.</span></span> <span data-ttu-id="6cf4b-106">El calendario puede ser de un [usuario](../resources/user.md) o el calendario predeterminado de un [grupo](../resources/group.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-106">The calendar can be one for a [user](../resources/user.md), or the default calendar of an Office 365 [group](../resources/group.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="6cf4b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6cf4b-107">Permissions</span></span>
<span data-ttu-id="6cf4b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6cf4b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6cf4b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6cf4b-110">Permission type</span></span>      | <span data-ttu-id="6cf4b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6cf4b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6cf4b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6cf4b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6cf4b-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6cf4b-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="6cf4b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6cf4b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6cf4b-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6cf4b-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="6cf4b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6cf4b-116">Application</span></span> | <span data-ttu-id="6cf4b-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6cf4b-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="6cf4b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6cf4b-118">HTTP request</span></span>
<span data-ttu-id="6cf4b-119"><!-- { "blockType": "ignored" } -->Un usuario o del grupo predeterminado de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="6cf4b-119"><!-- { "blockType": "ignored" } --> A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
PATCH /me/calendar
PATCH /users/{id | userPrincipalName}/calendar
PATCH /groups/{id}/calendar
```
<span data-ttu-id="6cf4b-120">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-120">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
PATCH /me/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendars/{id}

PATCH /me/calendarGroup/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="6cf4b-121">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-121">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
PATCH /me/calendarGroups/{id}/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="6cf4b-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6cf4b-122">Request headers</span></span>
| <span data-ttu-id="6cf4b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cf4b-123">Header</span></span>       | <span data-ttu-id="6cf4b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6cf4b-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6cf4b-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="6cf4b-125">Authorization</span></span>  | <span data-ttu-id="6cf4b-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="6cf4b-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6cf4b-128">Content-Type</span></span>  | <span data-ttu-id="6cf4b-p105">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-p105">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6cf4b-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6cf4b-131">Request body</span></span>
<span data-ttu-id="6cf4b-p106">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-p106">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6cf4b-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6cf4b-135">Property</span></span>     | <span data-ttu-id="6cf4b-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="6cf4b-136">Type</span></span>   |<span data-ttu-id="6cf4b-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cf4b-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6cf4b-138">color</span><span class="sxs-lookup"><span data-stu-id="6cf4b-138">color</span></span>|<span data-ttu-id="6cf4b-139">String</span><span class="sxs-lookup"><span data-stu-id="6cf4b-139">String</span></span>|<span data-ttu-id="6cf4b-p107">Especifica el tema de color para distinguir el calendario de otros calendarios en una interfaz de usuario. Los valores de propiedad son: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span><span class="sxs-lookup"><span data-stu-id="6cf4b-p107">Specifies the color theme to distinguish the calendar from other calendars in a UI. The property values are: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span></span>|
|<span data-ttu-id="6cf4b-142">name</span><span class="sxs-lookup"><span data-stu-id="6cf4b-142">name</span></span>|<span data-ttu-id="6cf4b-143">String</span><span class="sxs-lookup"><span data-stu-id="6cf4b-143">String</span></span>|<span data-ttu-id="6cf4b-144">El nombre del calendario.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-144">The calendar name.</span></span>|

## <a name="response"></a><span data-ttu-id="6cf4b-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6cf4b-145">Response</span></span>

<span data-ttu-id="6cf4b-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendar](../resources/calendar.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-146">If successful, this method returns a `200 OK` response code and updated [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6cf4b-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6cf4b-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6cf4b-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6cf4b-148">Request</span></span>
<span data-ttu-id="6cf4b-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_calendar"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/calendar
Content-type: application/json

{
  "name": "Social events"
}
```
##### <a name="response"></a><span data-ttu-id="6cf4b-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6cf4b-150">Response</span></span>
<span data-ttu-id="6cf4b-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6cf4b-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#me/calendars/$entity",
    "@odata.id":"https://graph.microsoft.com/v1.0/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/calendars('AAMkADJmMVAAA=')",
    "id":"AAMkADJmMVAAA=",
    "name":"Social events",
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
  "description": "Update calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
