---
title: Actualizar schemaExtensions
description: Actualice las propiedades de la definición del schemaExtension especificado.
ms.openlocfilehash: a09b3a4e2e48eb550acd5e77c60ab7213cc52de8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030808"
---
# <a name="update-schemaextension"></a><span data-ttu-id="960e5-103">Actualizar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="960e5-103">Update schemaExtension</span></span>

<span data-ttu-id="960e5-104">Actualice las propiedades de la definición del [schemaExtension](../resources/schemaextension.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="960e5-104">Update properties in the definition of the specified [schemaExtension](../resources/schemaextension.md).</span></span>

<span data-ttu-id="960e5-p101">La actualización se aplica a todos los recursos que se incluyen en la propiedad **targetTypes** de la extensión. Estos recursos se encuentran entre los [tipos de recurso admitidos](/graph/extensibility-overview#supported-resources).</span><span class="sxs-lookup"><span data-stu-id="960e5-p101">The update applies to all the resources that are included in the **targetTypes** property of the extension. These resources are among the [supporting resource types](/graph/extensibility-overview#supported-resources).</span></span>

<span data-ttu-id="960e5-p102">Solo la aplicación que ha creado una extensión de esquema (la aplicación propietaria) puede realizar cambios para agregar elementos a la extensión cuando esta se encuentra en los estados **InDevelopment** o **Available**. Esto significa que la aplicación no puede quitar propiedades personalizadas o tipos de recurso de destino de la definición. No obstante, sí puede cambiar la descripción de la extensión.</span><span class="sxs-lookup"><span data-stu-id="960e5-p102">Only the app that created a schema extension (owner app) can make additive updates to the extension when the extension is in the **InDevelopment** or **Available** status. That means the app cannot remove custom properties or target resource types from the definition. The app can, however, change the description of the extension.</span></span>

## <a name="permissions"></a><span data-ttu-id="960e5-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="960e5-110">Permissions</span></span>
<span data-ttu-id="960e5-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="960e5-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="960e5-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="960e5-113">Permission type</span></span>      | <span data-ttu-id="960e5-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="960e5-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="960e5-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="960e5-115">Delegated (work or school account)</span></span> | <span data-ttu-id="960e5-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="960e5-116">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="960e5-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="960e5-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="960e5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="960e5-118">Not supported.</span></span>    |
|<span data-ttu-id="960e5-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="960e5-119">Application</span></span> | <span data-ttu-id="960e5-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="960e5-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="960e5-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="960e5-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /schemaExtensions/{id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="960e5-122">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="960e5-122">Optional request headers</span></span>

| <span data-ttu-id="960e5-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="960e5-123">Name</span></span>      |<span data-ttu-id="960e5-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="960e5-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="960e5-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="960e5-125">Authorization</span></span>  | <span data-ttu-id="960e5-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="960e5-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="960e5-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="960e5-128">Content-Type</span></span>   | <span data-ttu-id="960e5-129">application/json</span><span class="sxs-lookup"><span data-stu-id="960e5-129">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="960e5-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="960e5-130">Request body</span></span>

<span data-ttu-id="960e5-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="960e5-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="960e5-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="960e5-134">Property</span></span>   | <span data-ttu-id="960e5-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="960e5-135">Type</span></span> |<span data-ttu-id="960e5-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="960e5-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="960e5-137">description</span><span class="sxs-lookup"><span data-stu-id="960e5-137">description</span></span>|<span data-ttu-id="960e5-138">String</span><span class="sxs-lookup"><span data-stu-id="960e5-138">String</span></span>|<span data-ttu-id="960e5-139">Descripción de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="960e5-139">Description for the schema extension.</span></span>|
|<span data-ttu-id="960e5-140">properties</span><span class="sxs-lookup"><span data-stu-id="960e5-140">properties</span></span>|<span data-ttu-id="960e5-141">Colección [extensionSchemaProperty](../resources/extensionschemaproperty.md)</span><span class="sxs-lookup"><span data-stu-id="960e5-141">[extensionSchemaProperty](../resources/extensionschemaproperty.md) collection</span></span>|<span data-ttu-id="960e5-p106">La colección de nombres de propiedad y tipos que conforman la definición de la extensión de esquema. Solo se admiten cambios para agregar elementos.</span><span class="sxs-lookup"><span data-stu-id="960e5-p106">The collection of property names and types that make up the schema extension definition. Only additive changes are permitted.</span></span> |
|<span data-ttu-id="960e5-144">status</span><span class="sxs-lookup"><span data-stu-id="960e5-144">status</span></span>|<span data-ttu-id="960e5-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="960e5-145">String</span></span>|<span data-ttu-id="960e5-146">El estado del ciclo de vida de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="960e5-146">The lifecycle state of the schema extension.</span></span> <span data-ttu-id="960e5-147">El estado inicial después de su creación es **InDevelopment**.</span><span class="sxs-lookup"><span data-stu-id="960e5-147">The initial state upon creation is **InDevelopment**.</span></span> <span data-ttu-id="960e5-148">Transiciones de los Estados posibles son de **InDevelopment** a **disponible** y **disponible** para **ya no se utiliza**.</span><span class="sxs-lookup"><span data-stu-id="960e5-148">Possible states transitions are from **InDevelopment** to **Available** and **Available** to **Deprecated**.</span></span>|
|<span data-ttu-id="960e5-149">targetTypes</span><span class="sxs-lookup"><span data-stu-id="960e5-149">targetTypes</span></span>|<span data-ttu-id="960e5-150">Colección string</span><span class="sxs-lookup"><span data-stu-id="960e5-150">String collection</span></span>|<span data-ttu-id="960e5-p108">Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema.  Solo se admiten cambios para agregar elementos.</span><span class="sxs-lookup"><span data-stu-id="960e5-p108">Set of Microsoft Graph types (that can support extensions) that the schema extension can be applied to.  Only additive changes are permitted.</span></span>|

## <a name="response"></a><span data-ttu-id="960e5-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="960e5-153">Response</span></span>

<span data-ttu-id="960e5-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="960e5-154">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="960e5-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="960e5-155">Example</span></span>

##### <a name="request"></a><span data-ttu-id="960e5-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="960e5-156">Request</span></span>

<span data-ttu-id="960e5-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="960e5-157">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_schemaextension"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/schemaExtensions/{id}
Content-type: application/json
Content-length: 201

{
  "properties": [
    {
      "name":"new-name-value",
      "type":"new-type-value"
    },
    {
      "name":"additional-name-value",
      "type":"additional-type-value"
    }
  ],
}
```

##### <a name="response"></a><span data-ttu-id="960e5-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="960e5-158">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="960e5-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="960e5-159">See also</span></span>

- [<span data-ttu-id="960e5-160">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="960e5-160">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="960e5-161">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="960e5-161">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update schemaextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->