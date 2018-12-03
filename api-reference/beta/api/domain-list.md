---
title: Enumerar dominios
description: Recupera una lista de objetos de dominio.
ms.openlocfilehash: 8038f2456c2eafdd74688d7f0815fd3cd264b3c0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083343"
---
# <a name="list-domains"></a><span data-ttu-id="0bb6f-103">Enumerar dominios</span><span class="sxs-lookup"><span data-stu-id="0bb6f-103">List domains</span></span>

> <span data-ttu-id="0bb6f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0bb6f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0bb6f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0bb6f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0bb6f-106">Recupera una lista de objetos de dominio.</span><span class="sxs-lookup"><span data-stu-id="0bb6f-106">Retrieve a list of domain objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="0bb6f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0bb6f-107">Permissions</span></span>
<span data-ttu-id="0bb6f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0bb6f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0bb6f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0bb6f-110">Permission type</span></span>      | <span data-ttu-id="0bb6f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0bb6f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0bb6f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0bb6f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0bb6f-113">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="0bb6f-113">Directory.Read.All</span></span>    |
|<span data-ttu-id="0bb6f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0bb6f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0bb6f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0bb6f-115">Not supported.</span></span>    |
|<span data-ttu-id="0bb6f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0bb6f-116">Application</span></span> | <span data-ttu-id="0bb6f-117">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0bb6f-117">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0bb6f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0bb6f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains
```
## <a name="optional-query-parameters"></a><span data-ttu-id="0bb6f-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0bb6f-119">Optional query parameters</span></span>
<span data-ttu-id="0bb6f-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0bb6f-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0bb6f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0bb6f-121">Request headers</span></span>
| <span data-ttu-id="0bb6f-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="0bb6f-122">Name</span></span>      |<span data-ttu-id="0bb6f-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="0bb6f-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="0bb6f-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="0bb6f-124">Authorization</span></span>  | <span data-ttu-id="0bb6f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0bb6f-p103">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="0bb6f-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0bb6f-127">Accept</span></span>         | <span data-ttu-id="0bb6f-128">application/json;</span><span class="sxs-lookup"><span data-stu-id="0bb6f-128">application/json;</span></span> |

## <a name="request-body"></a><span data-ttu-id="0bb6f-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0bb6f-129">Request body</span></span>
<span data-ttu-id="0bb6f-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0bb6f-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0bb6f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0bb6f-131">Response</span></span>

<span data-ttu-id="0bb6f-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0bb6f-132">If successful, this method returns a `200 OK` response code and collection of [domain](../resources/domain.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0bb6f-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0bb6f-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0bb6f-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0bb6f-134">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domains"
}-->
```http
GET https://graph.microsoft.com/beta/domains
```
##### <a name="response"></a><span data-ttu-id="0bb6f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0bb6f-135">Response</span></span>
<span data-ttu-id="0bb6f-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0bb6f-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "name": "contoso.com",
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