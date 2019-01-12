---
title: Obtener contrato
description: Recupera las propiedades y las relaciones del objeto contract.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: ba6ba3dd1e0dc631f5aeb61dd6d714e9d7a81bb6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917429"
---
# <a name="get-contract"></a><span data-ttu-id="b410b-103">Obtener contrato</span><span class="sxs-lookup"><span data-stu-id="b410b-103">Get Contract</span></span>

<span data-ttu-id="b410b-104">Recupera las propiedades y las relaciones del objeto [contract](../resources/contract.md).</span><span class="sxs-lookup"><span data-stu-id="b410b-104">Retrieve the properties and relationships of [contract](../resources/contract.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="b410b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b410b-105">Permissions</span></span>

<span data-ttu-id="b410b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b410b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="b410b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b410b-108">Permission type</span></span>      | <span data-ttu-id="b410b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b410b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b410b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b410b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b410b-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="b410b-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="b410b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b410b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b410b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b410b-113">Not supported.</span></span>    |
|<span data-ttu-id="b410b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b410b-114">Application</span></span> | <span data-ttu-id="b410b-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b410b-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b410b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b410b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /contracts/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b410b-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b410b-117">Optional query parameters</span></span>

<span data-ttu-id="b410b-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b410b-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b410b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b410b-119">Request headers</span></span>

| <span data-ttu-id="b410b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b410b-120">Name</span></span>      |<span data-ttu-id="b410b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b410b-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b410b-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b410b-122">Authorization</span></span>  | <span data-ttu-id="b410b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b410b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b410b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b410b-125">Request body</span></span>

<span data-ttu-id="b410b-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b410b-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b410b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b410b-127">Response</span></span>

<span data-ttu-id="b410b-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Contract](../resources/contract.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b410b-128">If successful, this method returns a `200 OK` response code and [Contract](../resources/contract.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b410b-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b410b-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b410b-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b410b-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_contract"
}-->
```http
GET https://graph.microsoft.com/v1.0/contracts/{id}
```

##### <a name="response"></a><span data-ttu-id="b410b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b410b-131">Response</span></span>
<span data-ttu-id="b410b-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b410b-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contract"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 186

{
  "contractType": "contractType-value",
  "customerId": "customerId-value",
  "defaultDomainName": "defaultDomainName-value",
  "displayName": "displayName-value",
  "id": "id-value"
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
