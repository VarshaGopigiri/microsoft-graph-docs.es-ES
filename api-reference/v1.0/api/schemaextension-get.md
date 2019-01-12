---
title: Obtener schemaExtensions
description: Obtiene las propiedades de la definición schemaExtensions especificada.
localization_priority: Normal
author: dkershaw10
ms.openlocfilehash: 70a4fdc5e51a5965098a6b0331a31c200b553ec9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980317"
---
# <a name="get-schemaextension"></a><span data-ttu-id="1097b-103">Obtener schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="1097b-103">Get schemaExtension</span></span>
<span data-ttu-id="1097b-104">Obtiene las propiedades de la definición [schemaExtensions](../resources/schemaextension.md) especificada.</span><span class="sxs-lookup"><span data-stu-id="1097b-104">Get the properties of the specified [schemaExtension](../resources/schemaextension.md) definition.</span></span>

## <a name="permissions"></a><span data-ttu-id="1097b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1097b-105">Permissions</span></span>
<span data-ttu-id="1097b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1097b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="1097b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1097b-108">Permission type</span></span>      | <span data-ttu-id="1097b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1097b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1097b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1097b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1097b-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="1097b-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="1097b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1097b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1097b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1097b-113">Not supported.</span></span>    |
|<span data-ttu-id="1097b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1097b-114">Application</span></span> | <span data-ttu-id="1097b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1097b-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1097b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1097b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /schemaExtensions/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1097b-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1097b-117">Optional query parameters</span></span>
<span data-ttu-id="1097b-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1097b-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1097b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1097b-119">Request headers</span></span>
| <span data-ttu-id="1097b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1097b-120">Name</span></span>      |<span data-ttu-id="1097b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1097b-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="1097b-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1097b-122">Authorization</span></span>  | <span data-ttu-id="1097b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1097b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1097b-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1097b-125">Content-Type</span></span>   | <span data-ttu-id="1097b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1097b-126">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="1097b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1097b-127">Request body</span></span>
<span data-ttu-id="1097b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1097b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1097b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1097b-129">Response</span></span>

<span data-ttu-id="1097b-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [schemaExtensions](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1097b-130">If successful, this method returns a `200 OK` response code and [schemaExtension](../resources/schemaextension.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1097b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1097b-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1097b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1097b-132">Request</span></span>
<span data-ttu-id="1097b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1097b-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_schemaextension"
}-->
```http
GET https://graph.microsoft.com/v1.0/schemaExtensions/graphlearn_test
```
##### <a name="response"></a><span data-ttu-id="1097b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1097b-134">Response</span></span>
<span data-ttu-id="1097b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1097b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
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

## <a name="see-also"></a><span data-ttu-id="1097b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1097b-138">See also</span></span>

- [<span data-ttu-id="1097b-139">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="1097b-139">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="1097b-140">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="1097b-140">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
