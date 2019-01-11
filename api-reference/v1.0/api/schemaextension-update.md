---
title: Actualizar schemaExtensions
description: Actualice las propiedades de la definición del schemaExtension especificado.
localization_priority: Normal
ms.openlocfilehash: 1316536f513ba126a504e1ad20d66591091157e6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855653"
---
# <a name="update-schemaextension"></a><span data-ttu-id="c3a93-103">Actualizar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="c3a93-103">Update schemaExtension</span></span>

<span data-ttu-id="c3a93-104">Actualice las propiedades de la definición del [schemaExtension](../resources/schemaextension.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="c3a93-104">Update properties in the definition of the specified [schemaExtension](../resources/schemaextension.md).</span></span>

<span data-ttu-id="c3a93-p101">La actualización se aplica a todos los recursos que se incluyen en la propiedad **targetTypes** de la extensión. Estos recursos se encuentran entre los [tipos de recurso admitidos](/graph/extensibility-overview#supported-resources).</span><span class="sxs-lookup"><span data-stu-id="c3a93-p101">The update applies to all the resources that are included in the **targetTypes** property of the extension. These resources are among the [supporting resource types](/graph/extensibility-overview#supported-resources).</span></span>

<span data-ttu-id="c3a93-p102">Solo la aplicación que ha creado una extensión de esquema (la aplicación propietaria) puede realizar cambios para agregar elementos a la extensión cuando esta se encuentra en los estados **InDevelopment** o **Available**. Esto significa que la aplicación no puede quitar propiedades personalizadas o tipos de recurso de destino de la definición. No obstante, sí puede cambiar la descripción de la extensión.</span><span class="sxs-lookup"><span data-stu-id="c3a93-p102">Only the app that created a schema extension (owner app) can make additive updates to the extension when the extension is in the **InDevelopment** or **Available** status. That means the app cannot remove custom properties or target resource types from the definition. The app can, however, change the description of the extension.</span></span>

## <a name="permissions"></a><span data-ttu-id="c3a93-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="c3a93-110">Permissions</span></span>
<span data-ttu-id="c3a93-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c3a93-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c3a93-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c3a93-113">Permission type</span></span>      | <span data-ttu-id="c3a93-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c3a93-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c3a93-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c3a93-115">Delegated (work or school account)</span></span> | <span data-ttu-id="c3a93-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c3a93-116">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c3a93-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c3a93-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c3a93-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3a93-118">Not supported.</span></span>    |
|<span data-ttu-id="c3a93-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c3a93-119">Application</span></span> | <span data-ttu-id="c3a93-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3a93-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c3a93-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3a93-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /schemaExtensions/{id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="c3a93-122">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="c3a93-122">Optional request headers</span></span>

| <span data-ttu-id="c3a93-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="c3a93-123">Name</span></span>      |<span data-ttu-id="c3a93-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3a93-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c3a93-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="c3a93-125">Authorization</span></span>  | <span data-ttu-id="c3a93-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3a93-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c3a93-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c3a93-128">Content-Type</span></span>   | <span data-ttu-id="c3a93-129">application/json</span><span class="sxs-lookup"><span data-stu-id="c3a93-129">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="c3a93-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c3a93-130">Request body</span></span>

<span data-ttu-id="c3a93-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c3a93-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c3a93-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c3a93-134">Property</span></span>   | <span data-ttu-id="c3a93-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3a93-135">Type</span></span> |<span data-ttu-id="c3a93-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3a93-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c3a93-137">description</span><span class="sxs-lookup"><span data-stu-id="c3a93-137">description</span></span>|<span data-ttu-id="c3a93-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="c3a93-138">String</span></span>|<span data-ttu-id="c3a93-139">Descripción de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a93-139">Description for the schema extension.</span></span>|
|<span data-ttu-id="c3a93-140">properties</span><span class="sxs-lookup"><span data-stu-id="c3a93-140">properties</span></span>|<span data-ttu-id="c3a93-141">Colección [extensionSchemaProperty](../resources/extensionschemaproperty.md)</span><span class="sxs-lookup"><span data-stu-id="c3a93-141">[extensionSchemaProperty](../resources/extensionschemaproperty.md) collection</span></span>|<span data-ttu-id="c3a93-p106">La colección de nombres de propiedad y tipos que conforman la definición de la extensión de esquema. Solo se admiten cambios para agregar elementos.</span><span class="sxs-lookup"><span data-stu-id="c3a93-p106">The collection of property names and types that make up the schema extension definition. Only additive changes are permitted.</span></span> |
|<span data-ttu-id="c3a93-144">status</span><span class="sxs-lookup"><span data-stu-id="c3a93-144">status</span></span>|<span data-ttu-id="c3a93-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="c3a93-145">String</span></span>|<span data-ttu-id="c3a93-146">El estado del ciclo de vida de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a93-146">The lifecycle state of the schema extension.</span></span> <span data-ttu-id="c3a93-147">El estado inicial después de su creación es **InDevelopment**.</span><span class="sxs-lookup"><span data-stu-id="c3a93-147">The initial state upon creation is **InDevelopment**.</span></span> <span data-ttu-id="c3a93-148">Transiciones de los Estados posibles son de **InDevelopment** a **disponible** y **disponible** para **ya no se utiliza**.</span><span class="sxs-lookup"><span data-stu-id="c3a93-148">Possible states transitions are from **InDevelopment** to **Available** and **Available** to **Deprecated**.</span></span>|
|<span data-ttu-id="c3a93-149">targetTypes</span><span class="sxs-lookup"><span data-stu-id="c3a93-149">targetTypes</span></span>|<span data-ttu-id="c3a93-150">Colección string</span><span class="sxs-lookup"><span data-stu-id="c3a93-150">String collection</span></span>|<span data-ttu-id="c3a93-p108">Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema.  Solo se admiten cambios para agregar elementos.</span><span class="sxs-lookup"><span data-stu-id="c3a93-p108">Set of Microsoft Graph types (that can support extensions) that the schema extension can be applied to.  Only additive changes are permitted.</span></span>|

## <a name="response"></a><span data-ttu-id="c3a93-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3a93-153">Response</span></span>

<span data-ttu-id="c3a93-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="c3a93-154">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="c3a93-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3a93-155">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c3a93-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c3a93-156">Request</span></span>

<span data-ttu-id="c3a93-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c3a93-157">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="c3a93-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3a93-158">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="c3a93-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3a93-159">See also</span></span>

- [<span data-ttu-id="c3a93-160">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="c3a93-160">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="c3a93-161">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="c3a93-161">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update schemaextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
