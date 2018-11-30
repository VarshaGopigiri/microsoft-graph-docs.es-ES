---
title: Obtener servicePrincipal
description: Recuperar las propiedades y relaciones del objeto serviceprincipal.
ms.openlocfilehash: 903bec11787b4b5acc5da688f7b73bf2bbd76262
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090630"
---
# <a name="get-serviceprincipal"></a><span data-ttu-id="11624-103">Obtener servicePrincipal</span><span class="sxs-lookup"><span data-stu-id="11624-103">Get servicePrincipal</span></span>

> <span data-ttu-id="11624-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11624-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11624-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11624-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="11624-106">Recuperar las propiedades y relaciones del objeto serviceprincipal.</span><span class="sxs-lookup"><span data-stu-id="11624-106">Retrieve the properties and relationships of serviceprincipal object.</span></span>
## <a name="permissions"></a><span data-ttu-id="11624-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="11624-107">Permissions</span></span>
<span data-ttu-id="11624-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="11624-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="11624-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11624-110">Permission type</span></span>      | <span data-ttu-id="11624-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11624-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="11624-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11624-112">Delegated (work or school account)</span></span> | <span data-ttu-id="11624-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="11624-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="11624-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11624-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="11624-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11624-115">Not supported.</span></span>    |
|<span data-ttu-id="11624-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11624-116">Application</span></span> | <span data-ttu-id="11624-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="11624-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="11624-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11624-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /servicePrincipals/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="11624-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="11624-119">Optional query parameters</span></span>
<span data-ttu-id="11624-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11624-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="11624-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11624-121">Request headers</span></span>
| <span data-ttu-id="11624-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="11624-122">Name</span></span>       | <span data-ttu-id="11624-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="11624-123">Type</span></span> | <span data-ttu-id="11624-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="11624-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="11624-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="11624-125">Authorization</span></span>  | <span data-ttu-id="11624-126">string</span><span class="sxs-lookup"><span data-stu-id="11624-126">string</span></span>  | <span data-ttu-id="11624-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="11624-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="11624-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11624-129">Request body</span></span>
<span data-ttu-id="11624-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="11624-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="11624-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11624-131">Response</span></span>

<span data-ttu-id="11624-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [servicePrincipal](../resources/serviceprincipal.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11624-132">If successful, this method returns a `200 OK` response code and [servicePrincipal](../resources/serviceprincipal.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="11624-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11624-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="11624-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11624-134">Request</span></span>
<span data-ttu-id="11624-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="11624-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_serviceprincipal"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}
```
##### <a name="response"></a><span data-ttu-id="11624-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11624-136">Response</span></span>
<span data-ttu-id="11624-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11624-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.serviceprincipal"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 391

{
  "accountEnabled": true,
  "addIns": [
    {
      "id": "id-value",
      "type": "type-value",
      "properties": [
        {
          "key": "key-value",
          "value": "value-value"
        }
      ]
    }
  ],
  "appDisplayName": "appDisplayName-value",
  "appId": "appId-value",
  "appOwnerOrganizationId": "appOwnerOrganizationId-value",
  "appRoleAssignmentRequired": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get servicePrincipal",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->