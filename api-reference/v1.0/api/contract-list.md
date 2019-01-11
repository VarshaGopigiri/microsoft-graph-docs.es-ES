---
title: Enumerar contratos
description: Recupera una lista de objetos contract asociados a un inquilino de partner.
localization_priority: Normal
ms.openlocfilehash: 69fdb62c7e3a89f8e4ebff5065a20ec8334bad88
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821003"
---
# <a name="list-contracts"></a><span data-ttu-id="14c5c-103">Enumerar contratos</span><span class="sxs-lookup"><span data-stu-id="14c5c-103">List contracts</span></span>

<span data-ttu-id="14c5c-104">Recupera una lista de objetos [contract](../resources/contract.md) asociados a un inquilino de partner.</span><span class="sxs-lookup"><span data-stu-id="14c5c-104">Retrieve a list of [contract](../resources/contract.md) objects associated to a partner tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="14c5c-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="14c5c-105">Permissions</span></span>

<span data-ttu-id="14c5c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="14c5c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="14c5c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="14c5c-108">Permission type</span></span>      | <span data-ttu-id="14c5c-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="14c5c-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="14c5c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="14c5c-110">Delegated (work or school account)</span></span> | <span data-ttu-id="14c5c-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="14c5c-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="14c5c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="14c5c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="14c5c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="14c5c-113">Not supported.</span></span>    |
|<span data-ttu-id="14c5c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="14c5c-114">Application</span></span> | <span data-ttu-id="14c5c-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="14c5c-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="14c5c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="14c5c-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
GET /contracts
```

## <a name="optional-query-parameters"></a><span data-ttu-id="14c5c-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="14c5c-117">Optional query parameters</span></span>

<span data-ttu-id="14c5c-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14c5c-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span> 

> <span data-ttu-id="14c5c-119">El filtrado es compatible con customerId, defaultDomainName y displayName.</span><span class="sxs-lookup"><span data-stu-id="14c5c-119">Filtering is supported for customerId, defaultDomainName, and displayName.</span></span>

## <a name="request-headers"></a><span data-ttu-id="14c5c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="14c5c-120">Request headers</span></span>

| <span data-ttu-id="14c5c-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="14c5c-121">Name</span></span>      |<span data-ttu-id="14c5c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="14c5c-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="14c5c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="14c5c-123">Authorization</span></span>  | <span data-ttu-id="14c5c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="14c5c-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="14c5c-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="14c5c-126">Request body</span></span>

<span data-ttu-id="14c5c-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="14c5c-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="14c5c-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14c5c-128">Response</span></span>

<span data-ttu-id="14c5c-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contract](../resources/contract.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14c5c-129">If successful, this method returns a `200 OK` response code and a collection of [Contract](../resources/contract.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="14c5c-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14c5c-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="14c5c-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="14c5c-131">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_contract"
}-->
```http
GET https://graph.microsoft.com/v1.0/contracts
```

##### <a name="response"></a><span data-ttu-id="14c5c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14c5c-132">Response</span></span>

<span data-ttu-id="14c5c-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="14c5c-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contract",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
    {
      "contractType": "contractType-value",
      "customerId": "customerId-value",
      "defaultDomainName": "defaultDomainName-value",
      "displayName": "displayName-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get Contract",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
