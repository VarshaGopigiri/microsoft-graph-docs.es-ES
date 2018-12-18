---
title: Enumerar serviceConfigurationRecords
description: Recupera una lista de los objetos domainDnsRecord necesarios para habilitar los servicios para el dominio.
author: lleonard-msft
ms.openlocfilehash: d61c3d1fc877b7e4902f79d1b8f92cc1ca9ad1c8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336620"
---
# <a name="list-serviceconfigurationrecords"></a><span data-ttu-id="9f57c-103">Enumerar serviceConfigurationRecords</span><span class="sxs-lookup"><span data-stu-id="9f57c-103">List serviceConfigurationRecords</span></span>

> <span data-ttu-id="9f57c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9f57c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9f57c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9f57c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9f57c-106">Recupera una lista de los objetos [domainDnsRecord](../resources/domaindnsrecord.md) necesarios para habilitar los servicios para el dominio.</span><span class="sxs-lookup"><span data-stu-id="9f57c-106">Retrieves a list of [domainDnsRecord](../resources/domaindnsrecord.md) objects needed to enable services for the domain.</span></span>

<span data-ttu-id="9f57c-p102">Utilice la lista devuelta para agregar registros en el archivo de zona del dominio. Esto puede hacerse a través del registrador de dominios o de la configuración del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="9f57c-p102">Use the returned list to add records to the zone file of the domain. This can be done through the domain registrar or DNS server configuration.</span></span>

## <a name="permissions"></a><span data-ttu-id="9f57c-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="9f57c-109">Permissions</span></span>

<span data-ttu-id="9f57c-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9f57c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="9f57c-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9f57c-112">Permission type</span></span>      | <span data-ttu-id="9f57c-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9f57c-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9f57c-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9f57c-114">Delegated (work or school account)</span></span> | <span data-ttu-id="9f57c-115">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="9f57c-115">Directory.Read.All</span></span>    |
|<span data-ttu-id="9f57c-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9f57c-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9f57c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f57c-117">Not supported.</span></span>    |
|<span data-ttu-id="9f57c-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9f57c-118">Application</span></span> | <span data-ttu-id="9f57c-119">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9f57c-119">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9f57c-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9f57c-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/contoso.com/serviceConfigurationRecords
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9f57c-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9f57c-121">Optional query parameters</span></span>

<span data-ttu-id="9f57c-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f57c-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9f57c-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f57c-123">Request headers</span></span>

| <span data-ttu-id="9f57c-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="9f57c-124">Name</span></span>      |<span data-ttu-id="9f57c-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f57c-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9f57c-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="9f57c-126">Authorization</span></span>  | <span data-ttu-id="9f57c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9f57c-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9f57c-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9f57c-129">Content-Type</span></span>  | <span data-ttu-id="9f57c-130">application/json</span><span class="sxs-lookup"><span data-stu-id="9f57c-130">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="9f57c-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9f57c-131">Request body</span></span>

<span data-ttu-id="9f57c-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9f57c-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9f57c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f57c-133">Response</span></span>

<span data-ttu-id="9f57c-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domainDnsRecord](../resources/domaindnsrecord.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f57c-134">If successful, this method returns a `200 OK` response code and collection of [domainDnsRecord](../resources/domaindnsrecord.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9f57c-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f57c-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9f57c-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9f57c-136">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_serviceconfigurationrecords"
}-->
```http
GET https://graph.microsoft.com/beta/domains/contoso.com/serviceConfigurationRecords
```
##### <a name="response"></a><span data-ttu-id="9f57c-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f57c-137">Response</span></span>
<span data-ttu-id="9f57c-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9f57c-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "isOptional": false,
      "label": "contoso.com",
      "recordType": "Mx",
      "supportedService": "Email",
      "ttl": 3600,
      "mailExchange": "contoso-com.mail.protection.outlook.com",
      "preference": 0
    },
    {
      "isOptional": false,
      "label": "contoso.com",
      "recordType": "Txt",
      "supportedServices": "Email",
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