---
title: Permissions
description: 'Quitar la aplicación de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino). '
ms.openlocfilehash: c3ee6433f38cfd52548af5ac27f3e3c9891af8d1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090825"
---
# <a name="remove-an-app-from-your-organizations-app-catalog"></a><span data-ttu-id="095f3-103">Quitar una aplicación de catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="095f3-103">Remove an app from your organization's app catalog</span></span>

> <span data-ttu-id="095f3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="095f3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="095f3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="095f3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="095f3-106">Quitar la [aplicación](../resources/teamsapp.md) de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino).</span><span class="sxs-lookup"><span data-stu-id="095f3-106">Remove the [app](../resources/teamsapp.md) from your organization's app catalog (the tenant app catalog).</span></span> <span data-ttu-id="095f3-107">Para quitar la aplicación de catálogo de aplicaciones de la organización, especifique `organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="095f3-107">To remove your app from your organization's app catalog, specify `organization` as the **distributionMethod** in the [teamsCatalogApp](../resources/teamsapp.md) resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="095f3-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="095f3-108">Permissions</span></span>

<span data-ttu-id="095f3-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="095f3-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="095f3-111">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="095f3-111">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="095f3-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="095f3-112">Permission Type</span></span>                        | <span data-ttu-id="095f3-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="095f3-113">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="095f3-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="095f3-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="095f3-115">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="095f3-115">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="095f3-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="095f3-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="095f3-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="095f3-117">Not supported</span></span>|
| <span data-ttu-id="095f3-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="095f3-118">Application</span></span>                            | <span data-ttu-id="095f3-119">No se admite</span><span class="sxs-lookup"><span data-stu-id="095f3-119">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="095f3-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="095f3-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /appCatalogs/teamsApps/{id}
```

## <a name="request-headers"></a><span data-ttu-id="095f3-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="095f3-121">Request headers</span></span>

| <span data-ttu-id="095f3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="095f3-122">Header</span></span>        | <span data-ttu-id="095f3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="095f3-123">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="095f3-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="095f3-124">Authorization</span></span> | <span data-ttu-id="095f3-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="095f3-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="095f3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="095f3-127">Request body</span></span>

<span data-ttu-id="095f3-128">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="095f3-128">None.</span></span>

><span data-ttu-id="095f3-129">**Nota:** Use el identificador devuelto de la llamada [lista publica aplicaciones](./teamsapp-list.md) para hacer referencia a la aplicación que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="095f3-129">**Note:** Use the ID returned from the [List published apps](./teamsapp-list.md) call for to reference the app you'd like to update.</span></span> <span data-ttu-id="095f3-130">No use el identificador del manifiesto del paquete de la aplicación de zip.</span><span class="sxs-lookup"><span data-stu-id="095f3-130">Do not use the ID from the manifest of the zip app package.</span></span>

## <a name="response"></a><span data-ttu-id="095f3-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="095f3-131">Response</span></span>

```
HTTP/1.1 204 No Content
```

## <a name="example"></a><span data-ttu-id="095f3-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="095f3-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="095f3-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="095f3-133">Request</span></span>

```http
DELETE https://graph.microsoft.com/beta/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8
```

### <a name="response"></a><span data-ttu-id="095f3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="095f3-134">Response</span></span>

```http
HTTP/1.1 204 No Content
```
