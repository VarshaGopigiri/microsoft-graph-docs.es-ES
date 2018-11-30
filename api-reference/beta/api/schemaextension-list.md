---
title: Enumerar schemaExtensions
description: 'Obtener una lista de objetos de schemaExtension creados por cualquier propietario en el inquilino actual (que puede ser de aplicaciones '
ms.openlocfilehash: 9e366ae62276198ad08f322646c920816d25ec64
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087907"
---
# <a name="list-schemaextensions"></a><span data-ttu-id="491e8-103">Enumerar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="491e8-103">List schemaExtensions</span></span>

> <span data-ttu-id="491e8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="491e8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="491e8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="491e8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="491e8-106">Obtenga una lista de objetos [schemaExtension](../resources/schemaextension.md) creada por cualquier aplicación de su propiedad en el inquilino actual (que puede estar **InDevelopment** (en desarrollo), **Available** (disponible) o **Deprecated** (en desuso) y el resto de extensiones de esquema propiedad de las otras aplicaciones que estén marcadas como **Available**.</span><span class="sxs-lookup"><span data-stu-id="491e8-106">Get a list of [schemaExtension](../resources/schemaextension.md) objects created by any apps you own in the current tenant (that can be **InDevelopment**, **Available**, or **Deprecated**), and all other schema extensions owned by other apps that are marked as **Available**.</span></span> 

## <a name="permissions"></a><span data-ttu-id="491e8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="491e8-107">Permissions</span></span>
<span data-ttu-id="491e8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="491e8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="491e8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="491e8-110">Permission type</span></span>      | <span data-ttu-id="491e8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="491e8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="491e8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="491e8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="491e8-113">Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="491e8-113">Directory.Read.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="491e8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="491e8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="491e8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="491e8-115">Not supported.</span></span>    |
|<span data-ttu-id="491e8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="491e8-116">Application</span></span> | <span data-ttu-id="491e8-117">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="491e8-117">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="491e8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="491e8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /schemaExtensions
```
## <a name="optional-query-parameters"></a><span data-ttu-id="491e8-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="491e8-119">Optional query parameters</span></span>
<span data-ttu-id="491e8-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="491e8-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="491e8-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="491e8-121">Request headers</span></span>
| <span data-ttu-id="491e8-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="491e8-122">Name</span></span>      |<span data-ttu-id="491e8-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="491e8-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="491e8-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="491e8-124">Authorization</span></span>  | <span data-ttu-id="491e8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="491e8-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="491e8-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="491e8-127">Content-Type</span></span>   | <span data-ttu-id="491e8-128">application/json</span><span class="sxs-lookup"><span data-stu-id="491e8-128">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="491e8-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="491e8-129">Request body</span></span>
<span data-ttu-id="491e8-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="491e8-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="491e8-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="491e8-131">Response</span></span>

<span data-ttu-id="491e8-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [schemaExtension](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="491e8-132">If successful, this method returns a `200 OK` response code and collection of [schemaExtension](../resources/schemaextension.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="491e8-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="491e8-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="491e8-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="491e8-134">Request</span></span>
<span data-ttu-id="491e8-135">En el ejemplo siguiente se muestra cómo buscar una extensión accesible concreta entre todas las demás filtrando por su **id.** único.</span><span class="sxs-lookup"><span data-stu-id="491e8-135">The following example shows how to look among all the accessible extensions for a specific one by filtering on its unique **id**.</span></span> 
<!-- {
  "blockType": "request",
  "name": "get_schemaextensions"
}-->
```http
GET https://graph.microsoft.com/beta/schemaExtensions?$filter=id%20eq%20'graphlearn_test'
```
##### <a name="response"></a><span data-ttu-id="491e8-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="491e8-136">Response</span></span>
<span data-ttu-id="491e8-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="491e8-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="491e8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="491e8-140">See also</span></span>

- [<span data-ttu-id="491e8-141">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="491e8-141">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="491e8-142">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="491e8-142">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List schemaExtensions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->