---
title: Enumerar verificationDnsRecords
description: Recupere una lista de objetos domainDnsRecord.
author: lleonard-msft
ms.openlocfilehash: 4beaac56892a33a5b5dfe46e2739b933d1598c45
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323257"
---
# <a name="list-verificationdnsrecords"></a><span data-ttu-id="7770d-103">Enumerar verificationDnsRecords</span><span class="sxs-lookup"><span data-stu-id="7770d-103">List verificationDnsRecords</span></span>

> <span data-ttu-id="7770d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7770d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7770d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7770d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7770d-106">Recupere una lista de objetos [domainDnsRecord](../resources/domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="7770d-106">Retrieve a list of [domainDnsRecord](../resources/domaindnsrecord.md) objects.</span></span>

<span data-ttu-id="7770d-p102">No puede utilizar un dominio asociado con su inquilino de Azure AD hasta que se verifique la propiedad. Para comprobar la propiedad del dominio, recupere los registros de comprobación del dominio y agregue los detalles al archivo de zona del dominio. Esto puede hacerse a través del registrador de dominios o de la configuración del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="7770d-p102">You cannot use an associated domain with your Azure AD tenant until ownership is verified. To verify the ownership of the domain, retrieve the domain verification records and add the details to the zone file of the domain. This can be done through the domain registrar or DNS server configuration.</span></span>

<span data-ttu-id="7770d-p103">Los dominios raíz requieren comprobación. Por ejemplo, contoso.com requiere comprobación. Si se comprueba un dominio raíz, los subdominios de este también se comprueban de forma automática. Por ejemplo, subdominio.contoso.com se comprueba de forma automática si se ha comprobado contoso.com.</span><span class="sxs-lookup"><span data-stu-id="7770d-p103">Root domains require verification. For example, contoso.com requires verification. If a root domain is verified, subdomains of the root domain are automatically verified. For example, subdomain.contoso.com is automatically be verified if contoso.com has been verified.</span></span>

## <a name="permissions"></a><span data-ttu-id="7770d-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="7770d-114">Permissions</span></span>

<span data-ttu-id="7770d-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7770d-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="7770d-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7770d-117">Permission type</span></span>      | <span data-ttu-id="7770d-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7770d-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7770d-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7770d-119">Delegated (work or school account)</span></span> | <span data-ttu-id="7770d-120">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="7770d-120">Directory.Read.All</span></span>    |
|<span data-ttu-id="7770d-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7770d-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7770d-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7770d-122">Not supported.</span></span>    |
|<span data-ttu-id="7770d-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7770d-123">Application</span></span> | <span data-ttu-id="7770d-124">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7770d-124">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7770d-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7770d-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/verificationDnsRecords
```

> <span data-ttu-id="7770d-126">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="7770d-126">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="7770d-127">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7770d-127">Optional query parameters</span></span>

<span data-ttu-id="7770d-128">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7770d-128">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7770d-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7770d-129">Request headers</span></span>

| <span data-ttu-id="7770d-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="7770d-130">Name</span></span>      |<span data-ttu-id="7770d-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="7770d-131">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="7770d-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="7770d-132">Authorization</span></span>  | <span data-ttu-id="7770d-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7770d-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7770d-135">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7770d-135">Content-Type</span></span>  | <span data-ttu-id="7770d-136">application/json</span><span class="sxs-lookup"><span data-stu-id="7770d-136">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="7770d-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7770d-137">Request body</span></span>

<span data-ttu-id="7770d-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7770d-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7770d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7770d-139">Response</span></span>

<span data-ttu-id="7770d-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domainDnsRecord](../resources/domaindnsrecord.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7770d-140">If successful, this method returns a `200 OK` response code and collection of [domainDnsRecord](../resources/domaindnsrecord.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7770d-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7770d-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7770d-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7770d-142">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_verificationdnsrecords"
}-->
```http
GET https://graph.microsoft.com/beta/domains/contoso.com/verificationDnsRecords
```

##### <a name="response"></a><span data-ttu-id="7770d-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7770d-143">Response</span></span>

<span data-ttu-id="7770d-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7770d-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List verificationDnsRecords",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->