---
title: Registrar governanceResource
description: Registrar un objeto governanceResource no administrado en PIM.
ms.openlocfilehash: 53452202b58c2d2187b6876eabfaae1ae646710d
ms.sourcegitcommit: 82f9d0d10388572a3073b2dde8ca0a7b409135b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/07/2018
ms.locfileid: "27195309"
---
# <a name="register-governanceresource"></a><span data-ttu-id="49346-103">Registrar governanceResource</span><span class="sxs-lookup"><span data-stu-id="49346-103">Register governanceResource</span></span>

> <span data-ttu-id="49346-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="49346-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="49346-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="49346-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="49346-106">Registrar un objeto no administrado [governanceResource](../resources/governanceresource.md) en la administración de identidades con privilegios.</span><span class="sxs-lookup"><span data-stu-id="49346-106">Register an unmanaged [governanceResource](../resources/governanceresource.md) object in Privileged Identity Management.</span></span>

## <a name="permissions"></a><span data-ttu-id="49346-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="49346-107">Permissions</span></span>
<span data-ttu-id="49346-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="49346-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

><span data-ttu-id="49346-110">**Nota:** Esta API también requiere que el solicitante tiene al menos una asignación de rol activo en el recurso.</span><span class="sxs-lookup"><span data-stu-id="49346-110">**Note:** This API also requires that the requester have at least one active role assignment on the resource.</span></span>

|<span data-ttu-id="49346-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="49346-111">Permission type</span></span>      | <span data-ttu-id="49346-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="49346-112">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="49346-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="49346-113">Delegated (work or school account)</span></span> | <span data-ttu-id="49346-114">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="49346-114">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="49346-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="49346-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="49346-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49346-116">Not supported.</span></span>    |
|<span data-ttu-id="49346-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="49346-117">Application</span></span> | <span data-ttu-id="49346-118">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="49346-118">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="http-request"></a><span data-ttu-id="49346-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49346-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/resources/register
```

### <a name="optional-query-parameters"></a><span data-ttu-id="49346-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="49346-120">Optional query parameters</span></span>
<span data-ttu-id="49346-121">Este método **sólo** es compatible con la `$select` y `$expand` de [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49346-121">This method **only** supports the `$select` and `$expand` [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

### <a name="request-headers"></a><span data-ttu-id="49346-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="49346-122">Request headers</span></span>
| <span data-ttu-id="49346-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="49346-123">Name</span></span>      |<span data-ttu-id="49346-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="49346-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="49346-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="49346-125">Authorization</span></span>  | <span data-ttu-id="49346-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="49346-126">Bearer {code}</span></span>|
| <span data-ttu-id="49346-127">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="49346-127">Content-type</span></span>  | <span data-ttu-id="49346-128">application/json</span><span class="sxs-lookup"><span data-stu-id="49346-128">application/json</span></span>|

### <a name="request-body"></a><span data-ttu-id="49346-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="49346-129">Request body</span></span>

|<span data-ttu-id="49346-130">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49346-130">Parameters</span></span>      |<span data-ttu-id="49346-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="49346-131">Type</span></span>                 |<span data-ttu-id="49346-132">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="49346-132">Required</span></span> |<span data-ttu-id="49346-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="49346-133">Description</span></span>|
|:-------------|:----------------------|:--------|:----------|
|<span data-ttu-id="49346-134">externalId</span><span class="sxs-lookup"><span data-stu-id="49346-134">externalId</span></span>    |<span data-ttu-id="49346-135">String</span><span class="sxs-lookup"><span data-stu-id="49346-135">String</span></span>                 |<span data-ttu-id="49346-136">✓</span><span class="sxs-lookup"><span data-stu-id="49346-136">✓</span></span>        |<span data-ttu-id="49346-137">ExternalId del recurso para poder registrarlas en PIM.</span><span class="sxs-lookup"><span data-stu-id="49346-137">The externalId of the resource to be registered in PIM.</span></span>|

### <a name="response"></a><span data-ttu-id="49346-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49346-138">Response</span></span>
<span data-ttu-id="49346-139">Si tiene éxito, este método devuelve una `200 OK` respuesta.</span><span class="sxs-lookup"><span data-stu-id="49346-139">If successful, this method returns a `200 OK` response.</span></span>

### <a name="example"></a><span data-ttu-id="49346-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49346-140">Example</span></span>
<span data-ttu-id="49346-141">En este ejemplo se muestra cómo registrar una suscripción de Azure Wingtip Toys - Prod.</span><span class="sxs-lookup"><span data-stu-id="49346-141">This example shows how to register an Azure subscription Wingtip Toys - Prod.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceresource"
}-->
##### <a name="request"></a><span data-ttu-id="49346-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49346-142">Request</span></span>
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/resources/register
```
##### <a name="response"></a><span data-ttu-id="49346-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49346-143">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceResource"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Register governanceResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
