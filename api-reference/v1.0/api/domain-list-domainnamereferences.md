---
title: Enumerar domainNameReferences
description: Recupere una lista de directoryObject con una referencia al dominio. La lista devuelta contendrá todos los objetos del directorio que tengan una dependencia en el dominio.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 4b9846f1a24b393609494542cf1785ec511f5b49
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963664"
---
# <a name="list-domainnamereferences"></a><span data-ttu-id="9d58e-104">Enumerar domainNameReferences</span><span class="sxs-lookup"><span data-stu-id="9d58e-104">List domainNameReferences</span></span>

<span data-ttu-id="9d58e-p102">Recupere una lista de [directoryObject](../resources/directoryobject.md) con una referencia al dominio. La lista devuelta contendrá todos los objetos del directorio que tengan una dependencia en el dominio.</span><span class="sxs-lookup"><span data-stu-id="9d58e-p102">Retrieve a list of [directoryObject](../resources/directoryobject.md) with a reference to the domain. The returned list will contain all directory objects that have a dependency on the domain.</span></span>

## <a name="permissions"></a><span data-ttu-id="9d58e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9d58e-107">Permissions</span></span>

<span data-ttu-id="9d58e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9d58e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="9d58e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9d58e-110">Permission type</span></span>      | <span data-ttu-id="9d58e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9d58e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9d58e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9d58e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9d58e-113">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="9d58e-113">Directory.Read.All</span></span>    |
|<span data-ttu-id="9d58e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9d58e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9d58e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d58e-115">Not supported.</span></span>    |
|<span data-ttu-id="9d58e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9d58e-116">Application</span></span> | <span data-ttu-id="9d58e-117">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d58e-117">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9d58e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9d58e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/domainNameReferences
```

> <span data-ttu-id="9d58e-119">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="9d58e-119">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="9d58e-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9d58e-120">Optional query parameters</span></span>

<span data-ttu-id="9d58e-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d58e-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9d58e-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9d58e-122">Request headers</span></span>

| <span data-ttu-id="9d58e-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d58e-123">Name</span></span>      |<span data-ttu-id="9d58e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d58e-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9d58e-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="9d58e-125">Authorization</span></span>  | <span data-ttu-id="9d58e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d58e-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9d58e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9d58e-128">Request body</span></span>

<span data-ttu-id="9d58e-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9d58e-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9d58e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d58e-130">Response</span></span>

<span data-ttu-id="9d58e-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d58e-131">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9d58e-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d58e-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9d58e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9d58e-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domainnamereferences"
}-->
```http
GET https://graph.microsoft.com/v1.0/domains/{domain-name}/domainNameReferences
```

##### <a name="response"></a><span data-ttu-id="9d58e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d58e-134">Response</span></span>
<span data-ttu-id="9d58e-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9d58e-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
