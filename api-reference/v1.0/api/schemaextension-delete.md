---
title: Eliminar schemaExtensions
description: Elimine la definición de una extensión de esquema.
ms.openlocfilehash: 5ec3ee675de3b4f40133d836e7caca055fa603a0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032386"
---
# <a name="delete-schemaextension"></a><span data-ttu-id="dc89c-103">Eliminar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="dc89c-103">Delete schemaExtension</span></span>

<span data-ttu-id="dc89c-104">Elimine la definición de una [extensión de esquema](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="dc89c-104">Delete the definition of a [schema extension](../resources/schemaextension.md).</span></span>

<span data-ttu-id="dc89c-p101">Solo la aplicación que creó la extensión de esquema (la aplicación propietaria) puede eliminar la definición de la extensión de esquema, y solo cuando la extensión esté en el estado **InDevelopment**. Eliminar una definición de extensión de esquema no afecta al acceso a los datos personalizados que se han agregado a las instancias de recurso a partir de esa definición.</span><span class="sxs-lookup"><span data-stu-id="dc89c-p101">Only the app that created the schema extension (owner app) can delete the schema extension definition, and only when the extension is in the **InDevelopment** state. Deleting a schema extension definition does not affect accessing custom data that has been added to resource instances based on that definition.</span></span>


## <a name="permissions"></a><span data-ttu-id="dc89c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="dc89c-107">Permissions</span></span>
<span data-ttu-id="dc89c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc89c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="dc89c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc89c-110">Permission type</span></span>      | <span data-ttu-id="dc89c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc89c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dc89c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc89c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="dc89c-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="dc89c-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="dc89c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc89c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dc89c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc89c-115">Not supported.</span></span>    |
|<span data-ttu-id="dc89c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc89c-116">Application</span></span> | <span data-ttu-id="dc89c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc89c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dc89c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc89c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /schemaExtensions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="dc89c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc89c-119">Request headers</span></span>
| <span data-ttu-id="dc89c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="dc89c-120">Name</span></span>      |<span data-ttu-id="dc89c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc89c-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="dc89c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="dc89c-122">Authorization</span></span>  | <span data-ttu-id="dc89c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dc89c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dc89c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dc89c-125">Request body</span></span>
<span data-ttu-id="dc89c-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dc89c-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dc89c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc89c-127">Response</span></span>

<span data-ttu-id="dc89c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc89c-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dc89c-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc89c-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dc89c-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dc89c-131">Request</span></span>
<span data-ttu-id="dc89c-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dc89c-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_schemaextension"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/schemaExtensions/{id}
```
##### <a name="response"></a><span data-ttu-id="dc89c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc89c-133">Response</span></span>
<span data-ttu-id="dc89c-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc89c-134">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="dc89c-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc89c-135">See also</span></span>

- [<span data-ttu-id="dc89c-136">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="dc89c-136">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="dc89c-137">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="dc89c-137">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->