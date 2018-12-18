---
title: Lista de las aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams
description: 'Aplicaciones de lista desde el catálogo de aplicaciones de Microsoft Teams. '
author: nkramer
ms.openlocfilehash: 9f292312b0e65a37d9d66b67009b49cf81db1c85
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326029"
---
# <a name="list-the-published-apps-from-the-microsoft-teams-app-catalog"></a><span data-ttu-id="0ce2c-103">Lista de las aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0ce2c-103">List the published apps from the Microsoft Teams app catalog</span></span>



<span data-ttu-id="0ce2c-104">Lista de [aplicaciones](../resources/teamsapp.md) desde el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-104">List [apps](../resources/teamsapp.md) from the Microsoft Teams app catalog.</span></span> <span data-ttu-id="0ce2c-105">Esto incluye aplicaciones de la tienda de Microsoft Teams, así como aplicaciones de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino).</span><span class="sxs-lookup"><span data-stu-id="0ce2c-105">This includes apps from the Microsoft Teams store, as well as apps from your organization's app catalog (the tenant app catalog).</span></span> <span data-ttu-id="0ce2c-106">Para obtener aplicaciones desde el catálogo de aplicaciones de la organización sólo, especifique `Organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="0ce2c-106">To get apps from your organization's app catalog only, specify `Organization` as the **distributionMethod** in the [teamsCatalogApp](../resources/teamsapp.md) resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="0ce2c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0ce2c-107">Permissions</span></span>

<span data-ttu-id="0ce2c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="0ce2c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="0ce2c-110">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-110">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="0ce2c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0ce2c-111">Permission Type</span></span>                        | <span data-ttu-id="0ce2c-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0ce2c-112">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="0ce2c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0ce2c-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="0ce2c-114">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0ce2c-114">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="0ce2c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0ce2c-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0ce2c-116">No admitido</span><span class="sxs-lookup"><span data-stu-id="0ce2c-116">Not supported</span></span>|
| <span data-ttu-id="0ce2c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0ce2c-117">Application</span></span>                            | <span data-ttu-id="0ce2c-118">No se admite</span><span class="sxs-lookup"><span data-stu-id="0ce2c-118">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="0ce2c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0ce2c-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /appCatalogs/teamsApps
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0ce2c-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0ce2c-120">Optional query parameters</span></span>
<span data-ttu-id="0ce2c-121">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-121">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0ce2c-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0ce2c-122">Request headers</span></span>

| <span data-ttu-id="0ce2c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ce2c-123">Header</span></span>        | <span data-ttu-id="0ce2c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0ce2c-124">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="0ce2c-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="0ce2c-125">Authorization</span></span> | <span data-ttu-id="0ce2c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0ce2c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0ce2c-128">Request body</span></span>
<span data-ttu-id="0ce2c-129">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-129">None.</span></span>

><span data-ttu-id="0ce2c-130">**Nota:** Puede filtrar en cualquiera de los campos del objeto [teamsCatalogApp](../resources/teamsapp.md) para reducir la lista de resultados.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-130">**Note:** You can filter on any of the fields of the [teamsCatalogApp](../resources/teamsapp.md) object to shorten the list of results.</span></span> <span data-ttu-id="0ce2c-131">Puede usar cualquiera de las siguientes operaciones de filtro: igual, no igual y, o bien y no.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-131">You can use any of the following filter operations: Equal, not-equal, and, or, and not.</span></span>

## <a name="response"></a><span data-ttu-id="0ce2c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ce2c-132">Response</span></span>
<span data-ttu-id="0ce2c-133">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de objetos de [teamsCatalogApp](../resources/teamsapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-133">If successful, this method returns a `200 OK` response code and a list of [teamsCatalogApp](../resources/teamsapp.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="0ce2c-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0ce2c-134">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="0ce2c-135">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ce2c-135">Example 1</span></span>
<span data-ttu-id="0ce2c-136">En el ejemplo siguiente se enumeran todas las aplicaciones que son específicas de su inquilino.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-136">The following example lists all applications that are specific to your tenant.</span></span>

#### <a name="request"></a><span data-ttu-id="0ce2c-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0ce2c-137">Request</span></span>
```
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps?$filter=distributionMethod eq 'organization'
```

#### <a name="response"></a><span data-ttu-id="0ce2c-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ce2c-138">Response</span></span>
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

### <a name="example-2"></a><span data-ttu-id="0ce2c-139">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="0ce2c-139">Example 2</span></span>

<span data-ttu-id="0ce2c-140">En el ejemplo siguiente se enumeran las aplicaciones con un identificador determinado.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-140">The following example lists applications with a given ID.</span></span>

#### <a name="request"></a><span data-ttu-id="0ce2c-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0ce2c-141">Request</span></span>
```
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps?$filter=id%20eq%20'b1c5353a-7aca-41b3-830f-27d5218fe0e5'
```

#### <a name="response"></a><span data-ttu-id="0ce2c-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ce2c-142">Response</span></span>
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

