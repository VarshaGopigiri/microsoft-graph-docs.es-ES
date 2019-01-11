---
title: Lista de las aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams
description: 'Aplicaciones de lista desde el catálogo de aplicaciones de Microsoft Teams. '
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 4cd3d8d66caa384a064711987f4fcd7473083089
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863458"
---
# <a name="list-the-published-apps-from-the-microsoft-teams-app-catalog"></a><span data-ttu-id="b0b1a-103">Lista de las aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b0b1a-103">List the published apps from the Microsoft Teams app catalog</span></span>

> <span data-ttu-id="b0b1a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b0b1a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b0b1a-106">Lista de [aplicaciones](../resources/teamsapp.md) desde el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-106">List [apps](../resources/teamsapp.md) from the Microsoft Teams app catalog.</span></span> <span data-ttu-id="b0b1a-107">Esto incluye aplicaciones de la tienda de Microsoft Teams, así como aplicaciones de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino).</span><span class="sxs-lookup"><span data-stu-id="b0b1a-107">This includes apps from the Microsoft Teams store, as well as apps from your organization's app catalog (the tenant app catalog).</span></span> <span data-ttu-id="b0b1a-108">Para obtener aplicaciones desde el catálogo de aplicaciones de la organización sólo, especifique `Organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b1a-108">To get apps from your organization's app catalog only, specify `Organization` as the **distributionMethod** in the [teamsCatalogApp](../resources/teamsapp.md) resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="b0b1a-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="b0b1a-109">Permissions</span></span>

<span data-ttu-id="b0b1a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="b0b1a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="b0b1a-112">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-112">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="b0b1a-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b0b1a-113">Permission Type</span></span>                        | <span data-ttu-id="b0b1a-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b0b1a-114">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="b0b1a-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b0b1a-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="b0b1a-116">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b0b1a-116">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="b0b1a-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b0b1a-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b0b1a-118">No admitido</span><span class="sxs-lookup"><span data-stu-id="b0b1a-118">Not supported</span></span>|
| <span data-ttu-id="b0b1a-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b0b1a-119">Application</span></span>                            | <span data-ttu-id="b0b1a-120">No se admite</span><span class="sxs-lookup"><span data-stu-id="b0b1a-120">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="b0b1a-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b0b1a-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /appCatalogs/teamsApps
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b0b1a-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b0b1a-122">Optional query parameters</span></span>
<span data-ttu-id="b0b1a-123">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-123">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b0b1a-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b0b1a-124">Request headers</span></span>

| <span data-ttu-id="b0b1a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0b1a-125">Header</span></span>        | <span data-ttu-id="b0b1a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b0b1a-126">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="b0b1a-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="b0b1a-127">Authorization</span></span> | <span data-ttu-id="b0b1a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b0b1a-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b0b1a-130">Request body</span></span>
<span data-ttu-id="b0b1a-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-131">None.</span></span>

><span data-ttu-id="b0b1a-132">**Nota:** Puede filtrar en cualquiera de los campos del objeto [teamsCatalogApp](../resources/teamsapp.md) para reducir la lista de resultados.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-132">**Note:** You can filter on any of the fields of the [teamsCatalogApp](../resources/teamsapp.md) object to shorten the list of results.</span></span> <span data-ttu-id="b0b1a-133">Puede usar cualquiera de las siguientes operaciones de filtro: igual, no igual y, o bien y no.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-133">You can use any of the following filter operations: Equal, not-equal, and, or, and not.</span></span>

## <a name="response"></a><span data-ttu-id="b0b1a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b0b1a-134">Response</span></span>
<span data-ttu-id="b0b1a-135">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de objetos de [teamsCatalogApp](../resources/teamsapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-135">If successful, this method returns a `200 OK` response code and a list of [teamsCatalogApp](../resources/teamsapp.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="b0b1a-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b0b1a-136">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="b0b1a-137">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="b0b1a-137">Example 1</span></span>
<span data-ttu-id="b0b1a-138">En el ejemplo siguiente se enumeran todas las aplicaciones que son específicas de su inquilino.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-138">The following example lists all applications that are specific to your tenant.</span></span>

#### <a name="request"></a><span data-ttu-id="b0b1a-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b0b1a-139">Request</span></span>
```
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps?$filter=distributionMethod eq 'organization'
```

#### <a name="response"></a><span data-ttu-id="b0b1a-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b0b1a-140">Response</span></span>
```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "b1c5353a-7aca-41b3-830f-27d5218fe0e5",
      "externalId": "f31b1263-ba99-435a-a679-911d24850d7c",
      "name": "Test App",
      "version": "1.0.1",
      "distributionMethod":"Organization"
    }
  ]
}
```

### <a name="example-2"></a><span data-ttu-id="b0b1a-141">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="b0b1a-141">Example 2</span></span>

<span data-ttu-id="b0b1a-142">En el ejemplo siguiente se enumeran las aplicaciones con un identificador determinado.</span><span class="sxs-lookup"><span data-stu-id="b0b1a-142">The following example lists applications with a given ID.</span></span>

#### <a name="request"></a><span data-ttu-id="b0b1a-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b0b1a-143">Request</span></span>
```
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps?$filter=id%20eq%20'b1c5353a-7aca-41b3-830f-27d5218fe0e5'
```

#### <a name="response"></a><span data-ttu-id="b0b1a-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b0b1a-144">Response</span></span>
```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "b1c5353a-7aca-41b3-830f-27d5218fe0e5",
      "externalId": "f31b1263-ba99-435a-a679-911d24850d7c",
      "name": "Test App",
      "version": "1.0.1",
      "distributionMethod":"Organization"
    }
  ]
}
```

