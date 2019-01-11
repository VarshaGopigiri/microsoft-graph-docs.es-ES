---
title: Enumerar serviceConfigurationRecords
description: Recupera una lista de los objetos domainDnsRecord necesarios para habilitar los servicios para el dominio.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 958115620d9cf1e8a108c08004bfb124328f15b9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825336"
---
# <a name="list-serviceconfigurationrecords"></a><span data-ttu-id="a3c01-103">Enumerar serviceConfigurationRecords</span><span class="sxs-lookup"><span data-stu-id="a3c01-103">List serviceConfigurationRecords</span></span>

<span data-ttu-id="a3c01-104">Recupera una lista de los objetos [domainDnsRecord](../resources/domaindnsrecord.md) necesarios para habilitar los servicios para el dominio.</span><span class="sxs-lookup"><span data-stu-id="a3c01-104">Retrieves a list of [domainDnsRecord](../resources/domaindnsrecord.md) objects needed to enable services for the domain.</span></span>

<span data-ttu-id="a3c01-p101">Utilice la lista devuelta para agregar registros en el archivo de zona del dominio. Esto puede hacerse a través del registrador de dominios o de la configuración del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="a3c01-p101">Use the returned list to add records to the zone file of the domain. This can be done through the domain registrar or DNS server configuration.</span></span>

## <a name="permissions"></a><span data-ttu-id="a3c01-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a3c01-107">Permissions</span></span>

<span data-ttu-id="a3c01-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a3c01-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="a3c01-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a3c01-110">Permission type</span></span>      | <span data-ttu-id="a3c01-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a3c01-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a3c01-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a3c01-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a3c01-113">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="a3c01-113">Directory.Read.All</span></span>    |
|<span data-ttu-id="a3c01-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a3c01-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a3c01-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3c01-115">Not supported.</span></span>    |
|<span data-ttu-id="a3c01-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a3c01-116">Application</span></span> | <span data-ttu-id="a3c01-117">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a3c01-117">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a3c01-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a3c01-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/contoso.com/serviceConfigurationRecords
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a3c01-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a3c01-119">Optional query parameters</span></span>

<span data-ttu-id="a3c01-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3c01-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a3c01-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a3c01-121">Request headers</span></span>

| <span data-ttu-id="a3c01-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="a3c01-122">Name</span></span>      |<span data-ttu-id="a3c01-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3c01-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a3c01-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a3c01-124">Authorization</span></span>  | <span data-ttu-id="a3c01-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3c01-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a3c01-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a3c01-127">Content-Type</span></span>  | <span data-ttu-id="a3c01-128">application/json</span><span class="sxs-lookup"><span data-stu-id="a3c01-128">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="a3c01-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a3c01-129">Request body</span></span>

<span data-ttu-id="a3c01-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a3c01-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a3c01-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3c01-131">Response</span></span>

<span data-ttu-id="a3c01-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domainDnsRecord](../resources/domaindnsrecord.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3c01-132">If successful, this method returns a `200 OK` response code and collection of [domainDnsRecord](../resources/domaindnsrecord.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a3c01-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3c01-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a3c01-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a3c01-134">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_serviceconfigurationrecords"
}-->
```http
GET https://graph.microsoft.com/v1.0/domains/{domain-name}/serviceConfigurationRecords
```
##### <a name="response"></a><span data-ttu-id="a3c01-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3c01-135">Response</span></span>
<span data-ttu-id="a3c01-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a3c01-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domainDnsRecord",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 220

{
  "value": [
    {
      "@odata.type":"microsoft.graph.domainDnsMxRecord",
      "isOptional": false,
      "label": "contoso.com",
      "recordType": "Mx",
      "supportedService": "Email",
      "ttl": 3600,
      "mailExchange": "contoso-com.mail.protection.outlook.com",
      "preference": 0
    },
    {
      "@odata.type":"microsoft.graph.domainDnsTxtRecord",
      "isOptional": false,
      "label": "contoso.com",
      "recordType": "Txt",
      "supportedService": "Email",
      "ttl": 3600,
      "text": "v=spf1 include: spf.protection.outlook.com ~all"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List serviceConfigurationRecords",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
