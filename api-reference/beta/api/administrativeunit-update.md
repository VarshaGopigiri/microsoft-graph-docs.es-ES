---
title: Actualizar administrativeunit
description: Actualizar las propiedades de un objeto administrativeUnit.
author: lleonard-msft
ms.openlocfilehash: 99ec27bc9a60e25d28202d2ebd82155089963c21
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362170"
---
# <a name="update-administrativeunit"></a><span data-ttu-id="c6b09-103">Actualizar administrativeunit</span><span class="sxs-lookup"><span data-stu-id="c6b09-103">Update administrativeunit</span></span>

> <span data-ttu-id="c6b09-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c6b09-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c6b09-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c6b09-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c6b09-106">Actualizar las propiedades de un objeto [administrativeUnit](../resources/administrativeunit.md) .</span><span class="sxs-lookup"><span data-stu-id="c6b09-106">Update the properties of an [administrativeUnit](../resources/administrativeunit.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c6b09-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6b09-107">Permissions</span></span>
<span data-ttu-id="c6b09-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c6b09-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c6b09-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6b09-110">Permission type</span></span>      | <span data-ttu-id="c6b09-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6b09-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6b09-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6b09-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c6b09-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c6b09-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c6b09-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6b09-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6b09-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6b09-115">Not supported.</span></span>    |
|<span data-ttu-id="c6b09-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6b09-116">Application</span></span> | <span data-ttu-id="c6b09-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6b09-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6b09-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6b09-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /administrativeUnits/{id}
```

## <a name="request-headers"></a><span data-ttu-id="c6b09-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6b09-119">Request headers</span></span>

| <span data-ttu-id="c6b09-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c6b09-120">Name</span></span>      |<span data-ttu-id="c6b09-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6b09-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c6b09-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c6b09-122">Authorization</span></span>  | <span data-ttu-id="c6b09-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6b09-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c6b09-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6b09-125">Request body</span></span>

<span data-ttu-id="c6b09-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c6b09-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c6b09-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c6b09-129">Property</span></span>   | <span data-ttu-id="c6b09-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6b09-130">Type</span></span> |<span data-ttu-id="c6b09-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6b09-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c6b09-132">description</span><span class="sxs-lookup"><span data-stu-id="c6b09-132">description</span></span>|<span data-ttu-id="c6b09-133">string</span><span class="sxs-lookup"><span data-stu-id="c6b09-133">string</span></span>|<span data-ttu-id="c6b09-134">Descripción de la unidad administrativa.</span><span class="sxs-lookup"><span data-stu-id="c6b09-134">Description for the administrative unit.</span></span>|
|<span data-ttu-id="c6b09-135">displayName</span><span class="sxs-lookup"><span data-stu-id="c6b09-135">displayName</span></span>|<span data-ttu-id="c6b09-136">string</span><span class="sxs-lookup"><span data-stu-id="c6b09-136">string</span></span>|<span data-ttu-id="c6b09-137">Nombre para mostrar para la unidad administrativa.</span><span class="sxs-lookup"><span data-stu-id="c6b09-137">Display name for the administrative unit.</span></span>|
|<span data-ttu-id="c6b09-138">visibility</span><span class="sxs-lookup"><span data-stu-id="c6b09-138">visibility</span></span>|<span data-ttu-id="c6b09-139">string</span><span class="sxs-lookup"><span data-stu-id="c6b09-139">string</span></span>|<span data-ttu-id="c6b09-140">Visibilidad de la unidad administrativa.</span><span class="sxs-lookup"><span data-stu-id="c6b09-140">Visibility for the administrative unit.</span></span> <span data-ttu-id="c6b09-141">Si no se establece, a continuación, el valor predeterminado es "public".</span><span class="sxs-lookup"><span data-stu-id="c6b09-141">If not set then the default is "public".</span></span> <span data-ttu-id="c6b09-142">Se puede establecer en "HiddenMembership", que se oculta la pertenencia de miembros que no sean.</span><span class="sxs-lookup"><span data-stu-id="c6b09-142">Can be set to "HiddenMembership", which hides the membership from non-members.</span></span>|

<span data-ttu-id="c6b09-143">Puesto que el recurso **administrativeUnit** admite [extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia de **administrativeUnit** existente.</span><span class="sxs-lookup"><span data-stu-id="c6b09-143">Since the **administrativeUnit** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **administrativeUnit** instance.</span></span>

## <a name="response"></a><span data-ttu-id="c6b09-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6b09-144">Response</span></span>

<span data-ttu-id="c6b09-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="c6b09-145">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="c6b09-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6b09-146">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c6b09-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6b09-147">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_administrativeunit"
}-->
```http
PATCH https://graph.microsoft.com/beta/administrativeUnits/{id}
Content-type: application/json
Content-length: 114

{
  "displayName": "displayName-value",
  "description": "description-value",
  "visibility": "visibility-value"
}
```

##### <a name="response"></a><span data-ttu-id="c6b09-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6b09-148">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.administrativeunit"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="c6b09-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6b09-149">See also</span></span>

- [<span data-ttu-id="c6b09-150">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="c6b09-150">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="c6b09-151">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="c6b09-151">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update administrativeunit",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->