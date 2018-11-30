---
title: Actualizar grupo de calendario
description: Actualiza las propiedades del objeto calendargroup.
ms.openlocfilehash: a201981d53b581085bd765dbe5a280adeb747fcf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083064"
---
# <a name="update-calendargroup"></a><span data-ttu-id="a4511-103">Actualizar grupo de calendario</span><span class="sxs-lookup"><span data-stu-id="a4511-103">Update calendargroup</span></span>

> <span data-ttu-id="a4511-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a4511-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a4511-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a4511-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a4511-106">Actualiza las propiedades del objeto calendargroup.</span><span class="sxs-lookup"><span data-stu-id="a4511-106">Update the properties of calendargroup object.</span></span>

## <a name="permissions"></a><span data-ttu-id="a4511-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a4511-107">Permissions</span></span>

<span data-ttu-id="a4511-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a4511-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a4511-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4511-110">Permission type</span></span>                        | <span data-ttu-id="a4511-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4511-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="a4511-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4511-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="a4511-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a4511-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="a4511-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4511-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a4511-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a4511-115">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="a4511-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4511-116">Application</span></span>                            | <span data-ttu-id="a4511-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a4511-117">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="a4511-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4511-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="a4511-119">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a4511-119">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
PATCH /me/calendarGroups/{id}
PATCH /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a4511-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4511-120">Request headers</span></span>

| <span data-ttu-id="a4511-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4511-121">Header</span></span>        | <span data-ttu-id="a4511-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a4511-122">Value</span></span>                       |
| :------------ | :-------------------------- |
| <span data-ttu-id="a4511-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a4511-123">Authorization</span></span> | <span data-ttu-id="a4511-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a4511-p103">Bearer {token}. Required.</span></span>   |
| <span data-ttu-id="a4511-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a4511-126">Content-Type</span></span>  | <span data-ttu-id="a4511-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a4511-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a4511-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4511-129">Request body</span></span>

<span data-ttu-id="a4511-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="a4511-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a4511-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4511-133">Property</span></span> | <span data-ttu-id="a4511-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4511-134">Type</span></span>   | <span data-ttu-id="a4511-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4511-135">Description</span></span>     |
| :------- | :----- | :-------------- |
| <span data-ttu-id="a4511-136">name</span><span class="sxs-lookup"><span data-stu-id="a4511-136">name</span></span>     | <span data-ttu-id="a4511-137">String</span><span class="sxs-lookup"><span data-stu-id="a4511-137">String</span></span> | <span data-ttu-id="a4511-138">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="a4511-138">The group name.</span></span> |

## <a name="response"></a><span data-ttu-id="a4511-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4511-139">Response</span></span>

<span data-ttu-id="a4511-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4511-140">If successful, this method returns a `200 OK` response code and updated [calendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4511-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4511-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a4511-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4511-142">Request</span></span>

<span data-ttu-id="a4511-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4511-143">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_calendargroup"
}-->

```http
PATCH https://graph.microsoft.com/beta/me/calendarGroups/{id}
Content-type: application/json
Content-length: 30

{
  "name": "name-value"
}
```

##### <a name="response"></a><span data-ttu-id="a4511-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4511-144">Response</span></span>

<span data-ttu-id="a4511-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a4511-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
  "description": "Update calendargroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->