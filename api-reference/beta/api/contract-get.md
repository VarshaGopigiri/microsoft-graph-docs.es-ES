---
title: Obtener contrato
description: Recupera las propiedades y las relaciones del objeto contract.
localization_priority: Normal
ms.openlocfilehash: 6e23594c0c897bd5827e1eb251907c9a1a646a1f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843851"
---
# <a name="get-contract"></a><span data-ttu-id="ff7e3-103">Obtener contrato</span><span class="sxs-lookup"><span data-stu-id="ff7e3-103">Get Contract</span></span>

> <span data-ttu-id="ff7e3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff7e3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ff7e3-106">Recupera las propiedades y las relaciones del objeto [contract](../resources/contract.md).</span><span class="sxs-lookup"><span data-stu-id="ff7e3-106">Retrieve the properties and relationships of [contract](../resources/contract.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ff7e3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ff7e3-107">Permissions</span></span>

<span data-ttu-id="ff7e3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ff7e3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="ff7e3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ff7e3-110">Permission type</span></span>      | <span data-ttu-id="ff7e3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ff7e3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ff7e3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ff7e3-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ff7e3-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ff7e3-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ff7e3-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ff7e3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ff7e3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-115">Not supported.</span></span>    |
|<span data-ttu-id="ff7e3-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ff7e3-116">Application</span></span> | <span data-ttu-id="ff7e3-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ff7e3-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ff7e3-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ff7e3-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /contracts/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ff7e3-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ff7e3-119">Optional query parameters</span></span>

<span data-ttu-id="ff7e3-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ff7e3-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ff7e3-121">Request headers</span></span>

| <span data-ttu-id="ff7e3-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff7e3-122">Name</span></span>      |<span data-ttu-id="ff7e3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff7e3-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ff7e3-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ff7e3-124">Authorization</span></span>  | <span data-ttu-id="ff7e3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ff7e3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ff7e3-127">Request body</span></span>

<span data-ttu-id="ff7e3-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ff7e3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff7e3-129">Response</span></span>

<span data-ttu-id="ff7e3-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Contract](../resources/contract.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-130">If successful, this method returns a `200 OK` response code and [Contract](../resources/contract.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ff7e3-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff7e3-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ff7e3-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ff7e3-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_contract"
}-->
```http
GET https://graph.microsoft.com/beta/contracts/{id}
```

##### <a name="response"></a><span data-ttu-id="ff7e3-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff7e3-133">Response</span></span>
<span data-ttu-id="ff7e3-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.Contract"
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
