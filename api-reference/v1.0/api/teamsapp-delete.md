---
title: Permisos
description: 'Quitar la aplicación de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino). '
localization_priority: Normal
ms.openlocfilehash: e19826407a5f809787beffc8211f77ddce21d043
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804931"
---
# <a name="remove-an-app-from-your-organizations-app-catalog"></a><span data-ttu-id="d5977-103">Quitar una aplicación de catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="d5977-103">Remove an app from your organization's app catalog</span></span>



<span data-ttu-id="d5977-104">Quitar la [aplicación](../resources/teamsapp.md) de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino).</span><span class="sxs-lookup"><span data-stu-id="d5977-104">Remove the [app](../resources/teamsapp.md) from your organization's app catalog (the tenant app catalog).</span></span> <span data-ttu-id="d5977-105">Para quitar la aplicación de catálogo de aplicaciones de la organización, especifique `organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="d5977-105">To remove your app from your organization's app catalog, specify `organization` as the **distributionMethod** in the [teamsCatalogApp](../resources/teamsapp.md) resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="d5977-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="d5977-106">Permissions</span></span>

<span data-ttu-id="d5977-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="d5977-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="d5977-109">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d5977-109">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="d5977-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d5977-110">Permission Type</span></span>                        | <span data-ttu-id="d5977-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d5977-111">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="d5977-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d5977-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="d5977-113">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d5977-113">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="d5977-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d5977-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d5977-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="d5977-115">Not supported</span></span>|
| <span data-ttu-id="d5977-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d5977-116">Application</span></span>                            | <span data-ttu-id="d5977-117">No se admite</span><span class="sxs-lookup"><span data-stu-id="d5977-117">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="d5977-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d5977-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /appCatalogs/teamsApps/{id}
```

## <a name="request-headers"></a><span data-ttu-id="d5977-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d5977-119">Request headers</span></span>

| <span data-ttu-id="d5977-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5977-120">Header</span></span>        | <span data-ttu-id="d5977-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d5977-121">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="d5977-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d5977-122">Authorization</span></span> | <span data-ttu-id="d5977-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d5977-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d5977-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d5977-125">Request body</span></span>

<span data-ttu-id="d5977-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d5977-126">None.</span></span>

><span data-ttu-id="d5977-127">**Nota:** Use el identificador devuelto de la llamada [lista publica aplicaciones](./teamsapp-list.md) para hacer referencia a la aplicación que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="d5977-127">**Note:** Use the ID returned from the [List published apps](./teamsapp-list.md) call for to reference the app you'd like to update.</span></span> <span data-ttu-id="d5977-128">No use el identificador del manifiesto del paquete de la aplicación de zip.</span><span class="sxs-lookup"><span data-stu-id="d5977-128">Do not use the ID from the manifest of the zip app package.</span></span>

## <a name="response"></a><span data-ttu-id="d5977-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5977-129">Response</span></span>

```
HTTP/1.1 204 No Content
```

## <a name="example"></a><span data-ttu-id="d5977-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5977-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="d5977-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d5977-131">Request</span></span>

```http
DELETE https://graph.microsoft.com/beta/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8
```

### <a name="response"></a><span data-ttu-id="d5977-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5977-132">Response</span></span>

```http
HTTP/1.1 204 No Content
```
