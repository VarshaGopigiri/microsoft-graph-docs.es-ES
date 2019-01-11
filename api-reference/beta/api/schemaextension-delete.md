---
title: Eliminar schemaExtensions
description: Elimine la definición de una extensión de esquema.
localization_priority: Normal
ms.openlocfilehash: 8641b00b984380592f14ae366b9cc20ab11dc7b7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842199"
---
# <a name="delete-schemaextension"></a><span data-ttu-id="4b97b-103">Eliminar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="4b97b-103">Delete schemaExtension</span></span>

> <span data-ttu-id="4b97b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4b97b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4b97b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4b97b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4b97b-106">Elimine la definición de una [extensión de esquema](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="4b97b-106">Delete the definition of a [schema extension](../resources/schemaextension.md).</span></span>

<span data-ttu-id="4b97b-p102">Solo la aplicación que creó la extensión de esquema (la aplicación propietaria) puede eliminar la definición de la extensión de esquema, y solo cuando la extensión esté en el estado **InDevelopment**. Eliminar una definición de extensión de esquema no afecta al acceso a los datos personalizados que se han agregado a las instancias de recurso a partir de esa definición.</span><span class="sxs-lookup"><span data-stu-id="4b97b-p102">Only the app that created the schema extension (owner app) can delete the schema extension definition, and only when the extension is in the **InDevelopment** state. Deleting a schema extension definition does not affect accessing custom data that has been added to resource instances based on that definition.</span></span>


## <a name="permissions"></a><span data-ttu-id="4b97b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="4b97b-109">Permissions</span></span>
<span data-ttu-id="4b97b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4b97b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="4b97b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4b97b-112">Permission type</span></span>      | <span data-ttu-id="4b97b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4b97b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4b97b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4b97b-114">Delegated (work or school account)</span></span> | <span data-ttu-id="4b97b-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4b97b-115">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4b97b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4b97b-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4b97b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4b97b-117">Not supported.</span></span>    |
|<span data-ttu-id="4b97b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4b97b-118">Application</span></span> | <span data-ttu-id="4b97b-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4b97b-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4b97b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4b97b-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /schemaExtensions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="4b97b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4b97b-121">Request headers</span></span>
| <span data-ttu-id="4b97b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="4b97b-122">Name</span></span>      |<span data-ttu-id="4b97b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b97b-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="4b97b-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="4b97b-124">Authorization</span></span>  | <span data-ttu-id="4b97b-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4b97b-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4b97b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4b97b-127">Request body</span></span>
<span data-ttu-id="4b97b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4b97b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4b97b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b97b-129">Response</span></span>

<span data-ttu-id="4b97b-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b97b-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4b97b-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b97b-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4b97b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4b97b-133">Request</span></span>
<span data-ttu-id="4b97b-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b97b-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_schemaextension"
}-->
```http
DELETE https://graph.microsoft.com/beta/schemaExtensions/{id}
```
##### <a name="response"></a><span data-ttu-id="4b97b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b97b-135">Response</span></span>
<span data-ttu-id="4b97b-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b97b-136">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="4b97b-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4b97b-137">See also</span></span>

- [<span data-ttu-id="4b97b-138">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="4b97b-138">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="4b97b-139">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="4b97b-139">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
