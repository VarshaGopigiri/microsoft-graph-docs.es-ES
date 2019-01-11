---
title: Lista servicePrincipals
description: Recuperar una lista de objetos de servicePrincipal.
localization_priority: Normal
ms.openlocfilehash: d7e0a9a34ac0ab7a166c40336671ec4d0a89ddd6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837614"
---
# <a name="list-serviceprincipals"></a><span data-ttu-id="a63dc-103">Lista servicePrincipals</span><span class="sxs-lookup"><span data-stu-id="a63dc-103">List servicePrincipals</span></span>

> <span data-ttu-id="a63dc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a63dc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a63dc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a63dc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a63dc-106">Recuperar una lista de objetos de servicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="a63dc-106">Retrieve a list of servicePrincipal objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="a63dc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a63dc-107">Permissions</span></span>

<span data-ttu-id="a63dc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a63dc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="a63dc-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a63dc-110">Permission type</span></span>      | <span data-ttu-id="a63dc-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a63dc-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a63dc-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a63dc-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a63dc-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a63dc-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a63dc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a63dc-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a63dc-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a63dc-115">Not supported.</span></span>    |
|<span data-ttu-id="a63dc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a63dc-116">Application</span></span> | <span data-ttu-id="a63dc-117">Application.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="a63dc-117">Application.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a63dc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a63dc-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /servicePrincipals
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a63dc-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a63dc-119">Optional query parameters</span></span>

<span data-ttu-id="a63dc-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a63dc-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a63dc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a63dc-121">Request headers</span></span>
| <span data-ttu-id="a63dc-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="a63dc-122">Name</span></span> | <span data-ttu-id="a63dc-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a63dc-123">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="a63dc-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="a63dc-124">Authorization</span></span>  | <span data-ttu-id="a63dc-125">string</span><span class="sxs-lookup"><span data-stu-id="a63dc-125">string</span></span>  | <span data-ttu-id="a63dc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a63dc-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a63dc-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a63dc-128">Request body</span></span>

<span data-ttu-id="a63dc-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a63dc-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a63dc-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a63dc-130">Response</span></span>

<span data-ttu-id="a63dc-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [servicePrincipal](../resources/serviceprincipal.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a63dc-131">If successful, this method returns a `200 OK` response code and collection of [servicePrincipal](../resources/serviceprincipal.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a63dc-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a63dc-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a63dc-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a63dc-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_serviceprincipals"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals
```
##### <a name="response"></a><span data-ttu-id="a63dc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a63dc-134">Response</span></span>

<span data-ttu-id="a63dc-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a63dc-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.serviceprincipal",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 488

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List servicePrincipals",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
