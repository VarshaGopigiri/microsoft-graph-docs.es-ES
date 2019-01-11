---
title: Actualizar grupo de calendario
description: Actualiza las propiedades del objeto calendargroup.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 18234705606596ff9ce258188877e4146eb2ea25
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857144"
---
# <a name="update-calendargroup"></a><span data-ttu-id="a54e6-103">Actualizar grupo de calendario</span><span class="sxs-lookup"><span data-stu-id="a54e6-103">Update calendargroup</span></span>

<span data-ttu-id="a54e6-104">Actualiza las propiedades del objeto calendargroup.</span><span class="sxs-lookup"><span data-stu-id="a54e6-104">Update the properties of calendargroup object.</span></span>

## <a name="permissions"></a><span data-ttu-id="a54e6-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a54e6-105">Permissions</span></span>

<span data-ttu-id="a54e6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a54e6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a54e6-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a54e6-108">Permission type</span></span>                        | <span data-ttu-id="a54e6-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a54e6-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="a54e6-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a54e6-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="a54e6-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a54e6-111">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="a54e6-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a54e6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a54e6-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a54e6-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="a54e6-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a54e6-114">Application</span></span>                            | <span data-ttu-id="a54e6-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a54e6-115">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="a54e6-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a54e6-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="a54e6-117">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a54e6-117">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
PATCH /me/calendarGroups/{id}
PATCH /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a54e6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a54e6-118">Request headers</span></span>

| <span data-ttu-id="a54e6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a54e6-119">Header</span></span>        | <span data-ttu-id="a54e6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a54e6-120">Value</span></span>                       |
| :------------ | :-------------------------- |
| <span data-ttu-id="a54e6-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a54e6-121">Authorization</span></span> | <span data-ttu-id="a54e6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a54e6-p102">Bearer {token}. Required.</span></span>   |
| <span data-ttu-id="a54e6-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a54e6-124">Content-Type</span></span>  | <span data-ttu-id="a54e6-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a54e6-p103">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a54e6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a54e6-127">Request body</span></span>

<span data-ttu-id="a54e6-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="a54e6-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a54e6-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a54e6-131">Property</span></span> | <span data-ttu-id="a54e6-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="a54e6-132">Type</span></span>   | <span data-ttu-id="a54e6-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="a54e6-133">Description</span></span>     |
| :------- | :----- | :-------------- |
| <span data-ttu-id="a54e6-134">name</span><span class="sxs-lookup"><span data-stu-id="a54e6-134">name</span></span>     | <span data-ttu-id="a54e6-135">String</span><span class="sxs-lookup"><span data-stu-id="a54e6-135">String</span></span> | <span data-ttu-id="a54e6-136">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="a54e6-136">The group name.</span></span> |

## <a name="response"></a><span data-ttu-id="a54e6-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a54e6-137">Response</span></span>

<span data-ttu-id="a54e6-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a54e6-138">If successful, this method returns a `200 OK` response code and updated [calendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a54e6-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a54e6-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a54e6-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a54e6-140">Request</span></span>

<span data-ttu-id="a54e6-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a54e6-141">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_calendargroup"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
Content-type: application/json
Content-length: 30

{
  "name": "name-value"
}
```

##### <a name="response"></a><span data-ttu-id="a54e6-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a54e6-142">Response</span></span>

<span data-ttu-id="a54e6-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a54e6-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
