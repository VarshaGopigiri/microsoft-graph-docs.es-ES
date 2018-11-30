---
title: Obtener identityProvider
description: Recuperar las propiedades de un identityProvider existente.
ms.openlocfilehash: 238e222c820e62685fa7c9e7ca50f5efb33693cf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086156"
---
# <a name="get-identityprovider"></a><span data-ttu-id="17b16-103">Obtener identityProvider</span><span class="sxs-lookup"><span data-stu-id="17b16-103">Get identityProvider</span></span>

> <span data-ttu-id="17b16-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="17b16-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="17b16-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="17b16-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="17b16-106">Recuperar las propiedades de una existente [identityProvider](../resources/identityprovider.md).</span><span class="sxs-lookup"><span data-stu-id="17b16-106">Retrieve the properties of an existing [identityProvider](../resources/identityprovider.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="17b16-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="17b16-107">Permissions</span></span>

<span data-ttu-id="17b16-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17b16-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="17b16-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17b16-110">Permission type</span></span>      | <span data-ttu-id="17b16-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17b16-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="17b16-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17b16-112">Delegated (work or school account)</span></span>|<span data-ttu-id="17b16-113">IdentityProvider.Read.All, IdentityProvider.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="17b16-113">IdentityProvider.Read.All, IdentityProvider.ReadWrite.All</span></span>|
|<span data-ttu-id="17b16-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17b16-114">Delegated (personal Microsoft account)</span></span>| <span data-ttu-id="17b16-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17b16-115">Not supported.</span></span>|
|<span data-ttu-id="17b16-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17b16-116">Application</span></span>|<span data-ttu-id="17b16-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17b16-117">Not supported.</span></span>|

<span data-ttu-id="17b16-118">La cuenta de trabajo o escuela debe ser un administrador global del inquilino.</span><span class="sxs-lookup"><span data-stu-id="17b16-118">The work or school account must be a global administrator of the tenant.</span></span>

## <a name="http-request"></a><span data-ttu-id="17b16-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17b16-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /identityProviders/{id}
```

## <a name="request-headers"></a><span data-ttu-id="17b16-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17b16-120">Request headers</span></span>

|<span data-ttu-id="17b16-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="17b16-121">Name</span></span>|<span data-ttu-id="17b16-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="17b16-122">Description</span></span>|
|:---------------|:----------|
|<span data-ttu-id="17b16-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="17b16-123">Authorization</span></span>|<span data-ttu-id="17b16-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="17b16-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="17b16-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17b16-126">Request body</span></span>

<span data-ttu-id="17b16-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="17b16-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="17b16-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17b16-128">Response</span></span>

<span data-ttu-id="17b16-129">Si tiene éxito, este método devuelve `200 OK` código de respuesta y una representación JSON de la [identityProvider](../resources/identityprovider.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17b16-129">If successful, this method returns `200 OK` response code and a JSON representation of the [identityProvider](../resources/identityprovider.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="17b16-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17b16-130">Example</span></span>

<span data-ttu-id="17b16-131">En el ejemplo siguiente se recupera un específico **identityProvider**.</span><span class="sxs-lookup"><span data-stu-id="17b16-131">The following example retrieves a specific **identityProvider**.</span></span>

##### <a name="request"></a><span data-ttu-id="17b16-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17b16-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_identityprovider"
}-->
```http
GET https://graph.microsoft.com/beta/identityProviders/Amazon-OAuth
```

##### <a name="response"></a><span data-ttu-id="17b16-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17b16-133">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.IdentityProvider"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "Amazon-OAUTH",
    "type": "Amazon",
    "name": "Login with Amazon",
    "clientId": "56433757-cadd-4135-8431-2c9e3fd68ae8",
    "clientSecret": "*****"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get identityProvider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->