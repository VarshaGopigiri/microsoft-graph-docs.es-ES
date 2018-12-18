---
title: Enumerar domainNameReferences
description: Recupere una lista de directoryObject con una referencia al dominio. La lista devuelta contendrá todos los objetos del directorio que tengan una dependencia en el dominio.
author: lleonard-msft
ms.openlocfilehash: d100855bf55c31d1c51308c0fd2330461b44981e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27322592"
---
# <a name="list-domainnamereferences"></a><span data-ttu-id="b13d3-104">Enumerar domainNameReferences</span><span class="sxs-lookup"><span data-stu-id="b13d3-104">List domainNameReferences</span></span>

> <span data-ttu-id="b13d3-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b13d3-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b13d3-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b13d3-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b13d3-p103">Recupere una lista de [directoryObject](../resources/directoryobject.md) con una referencia al dominio. La lista devuelta contendrá todos los objetos del directorio que tengan una dependencia en el dominio.</span><span class="sxs-lookup"><span data-stu-id="b13d3-p103">Retrieve a list of [directoryObject](../resources/directoryobject.md) with a reference to the domain. The returned list will contain all directory objects that have a dependency on the domain.</span></span>

## <a name="permissions"></a><span data-ttu-id="b13d3-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="b13d3-109">Permissions</span></span>

<span data-ttu-id="b13d3-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b13d3-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="b13d3-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b13d3-112">Permission type</span></span>      | <span data-ttu-id="b13d3-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b13d3-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b13d3-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b13d3-114">Delegated (work or school account)</span></span> | <span data-ttu-id="b13d3-115">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="b13d3-115">Directory.Read.All</span></span>    |
|<span data-ttu-id="b13d3-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b13d3-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b13d3-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b13d3-117">Not supported.</span></span>    |
|<span data-ttu-id="b13d3-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b13d3-118">Application</span></span> | <span data-ttu-id="b13d3-119">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b13d3-119">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b13d3-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b13d3-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/domainNameReferences
```

> <span data-ttu-id="b13d3-121">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="b13d3-121">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="b13d3-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b13d3-122">Optional query parameters</span></span>

<span data-ttu-id="b13d3-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b13d3-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b13d3-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b13d3-124">Request headers</span></span>

| <span data-ttu-id="b13d3-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="b13d3-125">Name</span></span>      |<span data-ttu-id="b13d3-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b13d3-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b13d3-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="b13d3-127">Authorization</span></span>  | <span data-ttu-id="b13d3-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b13d3-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b13d3-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b13d3-130">Request body</span></span>

<span data-ttu-id="b13d3-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b13d3-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b13d3-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b13d3-132">Response</span></span>

<span data-ttu-id="b13d3-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b13d3-133">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b13d3-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b13d3-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b13d3-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b13d3-135">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domainnamereferences"
}-->
```http
GET https://graph.microsoft.com/beta/domains/contoso.com/domainNameReferences
```

##### <a name="response"></a><span data-ttu-id="b13d3-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b13d3-136">Response</span></span>
<span data-ttu-id="b13d3-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b13d3-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
        "odata.type": "Microsoft.DirectoryServices.User",
        "objectType": "User",
        "objectId": "567a0db6-289c-43f7-a650-2645c03cbbbb",
        "accountEnabled": true,
        "displayName": "TestUser1",
        "facsimileTelephoneNumber": null,
        "mailNickname": "testuser1",
        "mobile": null,
        "userPrincipalName": "testuser1@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List domainNameReferences",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->