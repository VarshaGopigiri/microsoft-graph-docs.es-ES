---
title: Obtener schemaExtensions
description: Obtiene las propiedades de la definición schemaExtensions especificada.
localization_priority: Normal
author: dkershaw10
ms.openlocfilehash: 84c65e3a1b97046980150aa9ae254168da30b442
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982438"
---
# <a name="get-schemaextension"></a><span data-ttu-id="9c9b0-103">Obtener schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="9c9b0-103">Get schemaExtension</span></span>

> <span data-ttu-id="9c9b0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9c9b0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9c9b0-106">Obtiene las propiedades de la definición [schemaExtensions](../resources/schemaextension.md) especificada.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-106">Get the properties of the specified [schemaExtension](../resources/schemaextension.md) definition.</span></span>

## <a name="permissions"></a><span data-ttu-id="9c9b0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9c9b0-107">Permissions</span></span>
<span data-ttu-id="9c9b0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="9c9b0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9c9b0-110">Permission type</span></span>      | <span data-ttu-id="9c9b0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9c9b0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9c9b0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9c9b0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9c9b0-113">Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9c9b0-113">Directory.Read.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="9c9b0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9c9b0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9c9b0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-115">Not supported.</span></span>    |
|<span data-ttu-id="9c9b0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9c9b0-116">Application</span></span> | <span data-ttu-id="9c9b0-117">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="9c9b0-117">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9c9b0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9c9b0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /schemaExtensions/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9c9b0-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9c9b0-119">Optional query parameters</span></span>
<span data-ttu-id="9c9b0-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9c9b0-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9c9b0-121">Request headers</span></span>
| <span data-ttu-id="9c9b0-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="9c9b0-122">Name</span></span>      |<span data-ttu-id="9c9b0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c9b0-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9c9b0-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="9c9b0-124">Authorization</span></span>  | <span data-ttu-id="9c9b0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9c9b0-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9c9b0-127">Content-Type</span></span>   | <span data-ttu-id="9c9b0-128">application/json</span><span class="sxs-lookup"><span data-stu-id="9c9b0-128">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="9c9b0-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9c9b0-129">Request body</span></span>
<span data-ttu-id="9c9b0-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9c9b0-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c9b0-131">Response</span></span>

<span data-ttu-id="9c9b0-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [schemaExtensions](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-132">If successful, this method returns a `200 OK` response code and [schemaExtension](../resources/schemaextension.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9c9b0-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9c9b0-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9c9b0-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c9b0-134">Request</span></span>
<span data-ttu-id="9c9b0-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_schemaextension"
}-->
```http
GET https://graph.microsoft.com/beta/schemaExtensions/graphlearn_test
```
##### <a name="response"></a><span data-ttu-id="9c9b0-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c9b0-136">Response</span></span>
<span data-ttu-id="9c9b0-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
    "id":"graphlearn_test",
    "description": "Yet another test schema",
    "targetTypes": [
        "User", "Group"
    ],
    "status": "InDevelopment",
    "owner": "24d3b144-21ae-4080-943f-7067b395b913",
    "properties": [
        {
            "name": "testName",
            "type": "String"
        }
    ]
}
```

## <a name="see-also"></a><span data-ttu-id="9c9b0-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c9b0-140">See also</span></span>

- [<span data-ttu-id="9c9b0-141">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="9c9b0-141">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="9c9b0-142">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="9c9b0-142">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
