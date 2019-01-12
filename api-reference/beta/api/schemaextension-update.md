---
title: Actualizar schemaExtensions
description: Actualice las propiedades de la definición del schemaExtension especificado.
localization_priority: Normal
author: dkershaw10
ms.openlocfilehash: cdd0ac41e65e72ba16f5111c8b67869321f934dc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938499"
---
# <a name="update-schemaextension"></a><span data-ttu-id="38af2-103">Actualizar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="38af2-103">Update schemaExtension</span></span>

> <span data-ttu-id="38af2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="38af2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38af2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="38af2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="38af2-106">Actualice las propiedades de la definición del [schemaExtension](../resources/schemaextension.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="38af2-106">Update properties in the definition of the specified [schemaExtension](../resources/schemaextension.md).</span></span>

<span data-ttu-id="38af2-p102">La actualización se aplica a todos los recursos que se incluyen en la propiedad **targetTypes** de la extensión. Estos recursos se encuentran entre los [tipos de recurso admitidos](/graph/extensibility-overview#supported-resources).</span><span class="sxs-lookup"><span data-stu-id="38af2-p102">The update applies to all the resources that are included in the **targetTypes** property of the extension. These resources are among the [supporting resource types](/graph/extensibility-overview#supported-resources).</span></span>

<span data-ttu-id="38af2-p103">Solo la aplicación que ha creado una extensión de esquema (la aplicación propietaria) puede realizar cambios para agregar elementos a la extensión cuando esta se encuentra en los estados **InDevelopment** o **Available**. Esto significa que la aplicación no puede quitar propiedades personalizadas o tipos de recurso de destino de la definición. No obstante, sí puede cambiar la descripción de la extensión.</span><span class="sxs-lookup"><span data-stu-id="38af2-p103">Only the app that created a schema extension (owner app) can make additive updates to the extension when the extension is in the **InDevelopment** or **Available** status. That means the app cannot remove custom properties or target resource types from the definition. The app can, however, change the description of the extension.</span></span>

## <a name="permissions"></a><span data-ttu-id="38af2-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="38af2-112">Permissions</span></span>

<span data-ttu-id="38af2-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38af2-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="38af2-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38af2-115">Permission type</span></span>      | <span data-ttu-id="38af2-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38af2-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="38af2-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38af2-117">Delegated (work or school account)</span></span> | <span data-ttu-id="38af2-118">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="38af2-118">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="38af2-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38af2-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="38af2-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38af2-120">Not supported.</span></span>    |
|<span data-ttu-id="38af2-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38af2-121">Application</span></span> | <span data-ttu-id="38af2-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38af2-122">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="38af2-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38af2-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /schemaExtensions/{id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="38af2-124">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="38af2-124">Optional request headers</span></span>

| <span data-ttu-id="38af2-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="38af2-125">Name</span></span>      |<span data-ttu-id="38af2-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="38af2-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="38af2-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="38af2-127">Authorization</span></span>  | <span data-ttu-id="38af2-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38af2-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="38af2-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="38af2-130">Content-Type</span></span>   | <span data-ttu-id="38af2-131">application/json</span><span class="sxs-lookup"><span data-stu-id="38af2-131">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="38af2-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38af2-132">Request body</span></span>

<span data-ttu-id="38af2-p106">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="38af2-p106">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="38af2-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38af2-136">Property</span></span>   | <span data-ttu-id="38af2-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="38af2-137">Type</span></span> |<span data-ttu-id="38af2-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="38af2-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="38af2-139">description</span><span class="sxs-lookup"><span data-stu-id="38af2-139">description</span></span>|<span data-ttu-id="38af2-140">String</span><span class="sxs-lookup"><span data-stu-id="38af2-140">String</span></span>|<span data-ttu-id="38af2-141">Descripción de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="38af2-141">Description for the schema extension.</span></span>|
|<span data-ttu-id="38af2-142">properties</span><span class="sxs-lookup"><span data-stu-id="38af2-142">properties</span></span>|<span data-ttu-id="38af2-143">Colección [extensionSchemaProperty](../resources/extensionschemaproperty.md)</span><span class="sxs-lookup"><span data-stu-id="38af2-143">[extensionSchemaProperty](../resources/extensionschemaproperty.md) collection</span></span>|<span data-ttu-id="38af2-p107">La colección de nombres de propiedad y tipos que conforman la definición de la extensión de esquema. Solo se admiten cambios para agregar elementos.</span><span class="sxs-lookup"><span data-stu-id="38af2-p107">The collection of property names and types that make up the schema extension definition. Only additive changes are permitted.</span></span> |
|<span data-ttu-id="38af2-146">status</span><span class="sxs-lookup"><span data-stu-id="38af2-146">status</span></span>|<span data-ttu-id="38af2-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="38af2-147">String</span></span>|<span data-ttu-id="38af2-148">El estado del ciclo de vida de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="38af2-148">The lifecycle state of the schema extension.</span></span> <span data-ttu-id="38af2-149">El estado inicial después de su creación es **InDevelopment**.</span><span class="sxs-lookup"><span data-stu-id="38af2-149">The initial state upon creation is **InDevelopment**.</span></span> <span data-ttu-id="38af2-150">Transiciones de los Estados posibles son de **InDevelopment** a **disponible** y **disponible** para **ya no se utiliza**.</span><span class="sxs-lookup"><span data-stu-id="38af2-150">Possible states transitions are from **InDevelopment** to **Available** and **Available** to **Deprecated**.</span></span>|
|<span data-ttu-id="38af2-151">targetTypes</span><span class="sxs-lookup"><span data-stu-id="38af2-151">targetTypes</span></span>|<span data-ttu-id="38af2-152">Colección string</span><span class="sxs-lookup"><span data-stu-id="38af2-152">String collection</span></span>|<span data-ttu-id="38af2-p109">Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema.  Solo se admiten cambios para agregar elementos.</span><span class="sxs-lookup"><span data-stu-id="38af2-p109">Set of Microsoft Graph types (that can support extensions) that the schema extension can be applied to.  Only additive changes are permitted.</span></span>|

## <a name="response"></a><span data-ttu-id="38af2-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38af2-155">Response</span></span>

<span data-ttu-id="38af2-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="38af2-156">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="38af2-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38af2-157">Example</span></span>

##### <a name="request"></a><span data-ttu-id="38af2-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38af2-158">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_schemaextension"
}-->
```http
PATCH https://graph.microsoft.com/beta/schemaExtensions/{id}
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

##### <a name="response"></a><span data-ttu-id="38af2-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38af2-159">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="38af2-160">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="38af2-160">See also</span></span>

- [<span data-ttu-id="38af2-161">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="38af2-161">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="38af2-162">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="38af2-162">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update schemaextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
