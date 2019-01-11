---
title: Enumerar contratos
description: Recupera una lista de objetos contract asociados a un inquilino de partner.
localization_priority: Normal
ms.openlocfilehash: e1d3fa539a29a84a61c5e715edcfa773a7a705b4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866132"
---
# <a name="list-contracts"></a><span data-ttu-id="fafeb-103">Enumerar contratos</span><span class="sxs-lookup"><span data-stu-id="fafeb-103">List contracts</span></span>

> <span data-ttu-id="fafeb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fafeb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fafeb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fafeb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fafeb-106">Recupera una lista de objetos [contract](../resources/contract.md) asociados a un inquilino de partner.</span><span class="sxs-lookup"><span data-stu-id="fafeb-106">Retrieve a list of [contract](../resources/contract.md) objects associated to a partner tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="fafeb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="fafeb-107">Permissions</span></span>

<span data-ttu-id="fafeb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fafeb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="fafeb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fafeb-110">Permission type</span></span>      | <span data-ttu-id="fafeb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fafeb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fafeb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fafeb-112">Delegated (work or school account)</span></span> | <span data-ttu-id="fafeb-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="fafeb-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="fafeb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fafeb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fafeb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fafeb-115">Not supported.</span></span>    |
|<span data-ttu-id="fafeb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fafeb-116">Application</span></span> | <span data-ttu-id="fafeb-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fafeb-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="fafeb-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fafeb-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
GET /contracts
```

## <a name="optional-query-parameters"></a><span data-ttu-id="fafeb-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fafeb-119">Optional query parameters</span></span>

<span data-ttu-id="fafeb-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fafeb-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span> 

> <span data-ttu-id="fafeb-121">El filtrado es compatible con customerId, defaultDomainName y displayName.</span><span class="sxs-lookup"><span data-stu-id="fafeb-121">Filtering is supported for customerId, defaultDomainName, and displayName.</span></span>

## <a name="request-headers"></a><span data-ttu-id="fafeb-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fafeb-122">Request headers</span></span>

| <span data-ttu-id="fafeb-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="fafeb-123">Name</span></span>      |<span data-ttu-id="fafeb-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="fafeb-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="fafeb-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="fafeb-125">Authorization</span></span>  | <span data-ttu-id="fafeb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fafeb-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fafeb-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fafeb-128">Request body</span></span>

<span data-ttu-id="fafeb-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fafeb-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fafeb-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fafeb-130">Response</span></span>

<span data-ttu-id="fafeb-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contract](../resources/contract.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fafeb-131">If successful, this method returns a `200 OK` response code and a collection of [Contract](../resources/contract.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fafeb-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fafeb-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fafeb-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fafeb-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_contract"
}-->
```http
GET https://graph.microsoft.com/beta/contracts
```

##### <a name="response"></a><span data-ttu-id="fafeb-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fafeb-134">Response</span></span>

<span data-ttu-id="fafeb-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fafeb-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.Contract",
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
