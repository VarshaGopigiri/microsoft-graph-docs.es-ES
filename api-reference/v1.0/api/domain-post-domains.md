---
title: Crear dominio
description: Agregue un dominio al inquilino.
author: lleonard-msft
ms.openlocfilehash: c7b64f2d6df2279f248fe41ad23e3bfc0d9636de
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324832"
---
# <a name="create-domain"></a><span data-ttu-id="8fc20-103">Crear dominio</span><span class="sxs-lookup"><span data-stu-id="8fc20-103">Create domain</span></span>

<span data-ttu-id="8fc20-104">Agregue un dominio al inquilino.</span><span class="sxs-lookup"><span data-stu-id="8fc20-104">Adds a domain to the tenant.</span></span>

<span data-ttu-id="8fc20-p101">**Importante**: No puede utilizar un dominio asociado con su inquilino de Azure AD hasta que se verifique la propiedad. Consulte [Enumerar verificationDnsRecords](domain-list-verificationdnsrecords.md) para obtener más información. Los dominios raíz requieren comprobación. Por ejemplo, contoso.com requiere comprobación. Si se comprueba un dominio raíz, los subdominios de este también se comprueban de forma automática. Por ejemplo, subdominio.contoso.com se comprueba de forma automática si se ha comprobado contoso.com.</span><span class="sxs-lookup"><span data-stu-id="8fc20-p101">**Important**: You cannot use an associated domain with your Azure AD tenant until ownership is verified. See [List verificationDnsRecords](domain-list-verificationdnsrecords.md) for details. Root domains require verification. For example, contoso.com requires verification. If a root domain is verified, subdomains of the root domain are automatically verified. For example, subdomain.contoso.com is automatically be verified if contoso.com has been verified.</span></span>

## <a name="permissions"></a><span data-ttu-id="8fc20-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="8fc20-111">Permissions</span></span>

<span data-ttu-id="8fc20-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8fc20-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="8fc20-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8fc20-114">Permission type</span></span>      | <span data-ttu-id="8fc20-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8fc20-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8fc20-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8fc20-116">Delegated (work or school account)</span></span> | <span data-ttu-id="8fc20-117">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="8fc20-117">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="8fc20-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8fc20-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8fc20-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8fc20-119">Not supported.</span></span>    |
|<span data-ttu-id="8fc20-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8fc20-120">Application</span></span> | <span data-ttu-id="8fc20-121">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8fc20-121">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8fc20-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8fc20-122">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /domains
```
## <a name="request-headers"></a><span data-ttu-id="8fc20-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8fc20-123">Request headers</span></span>
| <span data-ttu-id="8fc20-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="8fc20-124">Name</span></span>       | <span data-ttu-id="8fc20-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fc20-125">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="8fc20-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="8fc20-126">Authorization</span></span>  | <span data-ttu-id="8fc20-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8fc20-p103">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="8fc20-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8fc20-129">Content-Type</span></span>  | <span data-ttu-id="8fc20-130">application/json</span><span class="sxs-lookup"><span data-stu-id="8fc20-130">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="8fc20-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8fc20-131">Request body</span></span>
<span data-ttu-id="8fc20-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [domain](../resources/domain.md).</span><span class="sxs-lookup"><span data-stu-id="8fc20-132">In the request body, supply a JSON representation of [domain](../resources/domain.md) object.</span></span>

> <span data-ttu-id="8fc20-p104">El cuerpo de la solicitud contiene la propiedad de id. del dominio nuevo. Id. es la única propiedad que se puede especificar y que es necesaria. El valor de la propiedad de id. es el nombre de dominio completo que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="8fc20-p104">The request body contains the id property for the new domain. Id is the only property that can be specified and it is required. The id property value is the fully qualified domain name to create.</span></span>

## <a name="response"></a><span data-ttu-id="8fc20-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fc20-136">Response</span></span>

<span data-ttu-id="8fc20-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8fc20-137">If successful, this method returns `201 Created` response code and [domain](../resources/domain.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8fc20-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8fc20-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8fc20-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8fc20-139">Request</span></span>

<span data-ttu-id="8fc20-140">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [domain](../resources/domain.md).</span><span class="sxs-lookup"><span data-stu-id="8fc20-140">In the request body, supply a JSON representation of [domain](../resources/domain.md) object.</span></span>

<!-- {
  "blockType": "request",
  "id": "create_domain_from_domains"
}-->
```http
POST https://graph.microsoft.com/v1.0/domains
Content-type: application/json
Content-length: 192

{
  "id": "contoso.com"
}
```

##### <a name="response"></a><span data-ttu-id="8fc20-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fc20-141">Response</span></span>
<span data-ttu-id="8fc20-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8fc20-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 192

{
  "authenticationType": "authenticationType-value",
  "availabilityStatus": "availabilityStatus-value",
  "id": "contoso.com",
  "isAdminManaged": true,
  "isDefault": true,
  "isInitial": true,
  "isRoot": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->