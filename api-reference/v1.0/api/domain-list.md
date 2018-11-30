---
title: Enumerar dominios
description: Recupera una lista de objetos de dominio.
ms.openlocfilehash: 51c9e4035c44567589ba2f9c7b86453e48db6a9f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029778"
---
# <a name="list-domains"></a><span data-ttu-id="49bcd-103">Enumerar dominios</span><span class="sxs-lookup"><span data-stu-id="49bcd-103">List domains</span></span>

<span data-ttu-id="49bcd-104">Recupera una lista de objetos de dominio.</span><span class="sxs-lookup"><span data-stu-id="49bcd-104">Retrieve a list of domain objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="49bcd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="49bcd-105">Permissions</span></span>
<span data-ttu-id="49bcd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="49bcd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="49bcd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="49bcd-108">Permission type</span></span>      | <span data-ttu-id="49bcd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="49bcd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="49bcd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="49bcd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="49bcd-111">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="49bcd-111">Directory.Read.All</span></span>    |
|<span data-ttu-id="49bcd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="49bcd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="49bcd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49bcd-113">Not supported.</span></span>    |
|<span data-ttu-id="49bcd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="49bcd-114">Application</span></span> | <span data-ttu-id="49bcd-115">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="49bcd-115">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="49bcd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains
```
## <a name="optional-query-parameters"></a><span data-ttu-id="49bcd-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="49bcd-117">Optional query parameters</span></span>
<span data-ttu-id="49bcd-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49bcd-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="49bcd-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="49bcd-119">Request headers</span></span>
| <span data-ttu-id="49bcd-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="49bcd-120">Name</span></span>      |<span data-ttu-id="49bcd-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="49bcd-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="49bcd-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="49bcd-122">Authorization</span></span>  | <span data-ttu-id="49bcd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="49bcd-p102">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="49bcd-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="49bcd-125">Accept</span></span>         | <span data-ttu-id="49bcd-126">application/json;</span><span class="sxs-lookup"><span data-stu-id="49bcd-126">application/json;</span></span> |

## <a name="request-body"></a><span data-ttu-id="49bcd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="49bcd-127">Request body</span></span>
<span data-ttu-id="49bcd-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="49bcd-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="49bcd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49bcd-129">Response</span></span>

<span data-ttu-id="49bcd-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49bcd-130">If successful, this method returns a `200 OK` response code and collection of [domain](../resources/domain.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="49bcd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49bcd-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="49bcd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49bcd-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domains"
}-->
```http
GET https://graph.microsoft.com/v1.0/domains
```
##### <a name="response"></a><span data-ttu-id="49bcd-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49bcd-133">Response</span></span>
<span data-ttu-id="49bcd-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="49bcd-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 245

{
  "value": [
    {
      "authenticationType": "authenticationType-value",
      "availabilityStatus": "availabilityStatus-value",
      "isAdminManaged": true,
      "isDefault": true,
      "isInitial": true,
      "isRoot": true,
      "id": "contoso.com",
      "supportedServices": [
        "Email",
        "OfficeCommunicationsOnline"
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List domains",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->