---
title: Enumerar schemaExtensions
description: 'Obtener una lista de objetos de schemaExtension creados por cualquier propietario en el inquilino actual (que puede ser de aplicaciones '
ms.openlocfilehash: b5e11856156094cc797b9e620c8e2d3ff82da349
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032387"
---
# <a name="list-schemaextensions"></a><span data-ttu-id="21cb1-103">Enumerar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="21cb1-103">List schemaExtensions</span></span>

<span data-ttu-id="21cb1-104">Obtenga una lista de objetos [schemaExtension](../resources/schemaextension.md) creada por cualquier aplicación de su propiedad en el inquilino actual (que puede estar **InDevelopment** (en desarrollo), **Available** (disponible) o **Deprecated** (en desuso) y el resto de extensiones de esquema propiedad de las otras aplicaciones que estén marcadas como **Available**.</span><span class="sxs-lookup"><span data-stu-id="21cb1-104">Get a list of [schemaExtension](../resources/schemaextension.md) objects created by any apps you own in the current tenant (that can be **InDevelopment**, **Available**, or **Deprecated**), and all other schema extensions owned by other apps that are marked as **Available**.</span></span> 

## <a name="permissions"></a><span data-ttu-id="21cb1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="21cb1-105">Permissions</span></span>
<span data-ttu-id="21cb1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21cb1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="21cb1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21cb1-108">Permission type</span></span>      | <span data-ttu-id="21cb1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21cb1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="21cb1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21cb1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="21cb1-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="21cb1-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="21cb1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21cb1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="21cb1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21cb1-113">Not supported.</span></span>    |
|<span data-ttu-id="21cb1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21cb1-114">Application</span></span> | <span data-ttu-id="21cb1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21cb1-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="21cb1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21cb1-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /schemaExtensions
```
## <a name="optional-query-parameters"></a><span data-ttu-id="21cb1-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="21cb1-117">Optional query parameters</span></span>
<span data-ttu-id="21cb1-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21cb1-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="21cb1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21cb1-119">Request headers</span></span>
| <span data-ttu-id="21cb1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="21cb1-120">Name</span></span>      |<span data-ttu-id="21cb1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="21cb1-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="21cb1-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="21cb1-122">Authorization</span></span>  | <span data-ttu-id="21cb1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="21cb1-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="21cb1-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="21cb1-125">Content-Type</span></span>   | <span data-ttu-id="21cb1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="21cb1-126">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="21cb1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21cb1-127">Request body</span></span>
<span data-ttu-id="21cb1-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="21cb1-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="21cb1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21cb1-129">Response</span></span>

<span data-ttu-id="21cb1-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [schemaExtension](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21cb1-130">If successful, this method returns a `200 OK` response code and collection of [schemaExtension](../resources/schemaextension.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="21cb1-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21cb1-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="21cb1-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21cb1-132">Request</span></span>
<span data-ttu-id="21cb1-133">En el ejemplo siguiente se muestra cómo buscar una extensión accesible concreta entre todas las demás filtrando por su **id.** único.</span><span class="sxs-lookup"><span data-stu-id="21cb1-133">The following example shows how to look among all the accessible extensions for a specific one by filtering on its unique **id**.</span></span> 
<!-- {
  "blockType": "request",
  "name": "get_schemaextensions"
}-->
```http
GET https://graph.microsoft.com/v1.0/schemaExtensions?$filter=id%20eq%20'graphlearn_test'
```
##### <a name="response"></a><span data-ttu-id="21cb1-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21cb1-134">Response</span></span>
<span data-ttu-id="21cb1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="21cb1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 274

{
  "value": [
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
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="21cb1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="21cb1-138">See also</span></span>

- [<span data-ttu-id="21cb1-139">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="21cb1-139">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="21cb1-140">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="21cb1-140">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List schemaExtensions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->