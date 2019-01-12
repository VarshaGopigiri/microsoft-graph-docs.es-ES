---
title: Permisos
description: 'Actualizar una aplicación que se publicaron anteriormente en el catálogo de aplicaciones de Microsoft Teams. '
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 44ca5870fd585ef7cd5aa0c0282eac42d41c1a18
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948525"
---
# <a name="update-apps-published-to-your-organizations-app-catalog"></a><span data-ttu-id="00b97-103">Actualizar aplicaciones publicadas en catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="00b97-103">Update apps published to your organization's app catalog</span></span>



<span data-ttu-id="00b97-104">Actualización de una [aplicación](../resources/teamsapp.md) se publicaron anteriormente en el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="00b97-104">Update an [app](../resources/teamsapp.md) previously published to the Microsoft Teams app catalog.</span></span> <span data-ttu-id="00b97-105">Esta API específicamente actualiza una aplicación publicada en catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino).</span><span class="sxs-lookup"><span data-stu-id="00b97-105">This API specifically updates an app published to your organization's app catalog (the tenant app catalog).</span></span> <span data-ttu-id="00b97-106">Para publicar en el catálogo de aplicaciones de la organización, especifique `organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="00b97-106">To publish to your organization's app catalog, specify `organization` as the **distributionMethod** in the [teamsCatalogApp](../resources/teamsapp.md) resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="00b97-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="00b97-107">Permissions</span></span>

<span data-ttu-id="00b97-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="00b97-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="00b97-110">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="00b97-110">**Note:** Only global administrators can call this API.</span></span>

| <span data-ttu-id="00b97-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="00b97-111">Permission Type</span></span>                        | <span data-ttu-id="00b97-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="00b97-112">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="00b97-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="00b97-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="00b97-114">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00b97-114">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="00b97-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="00b97-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="00b97-116">No admitido</span><span class="sxs-lookup"><span data-stu-id="00b97-116">Not supported</span></span>|
| <span data-ttu-id="00b97-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="00b97-117">Application</span></span>                            | <span data-ttu-id="00b97-118">No se admite</span><span class="sxs-lookup"><span data-stu-id="00b97-118">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="00b97-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00b97-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /appCatalogs/teamsApps/{id}
```

## <a name="request-headers"></a><span data-ttu-id="00b97-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="00b97-120">Request headers</span></span>

| <span data-ttu-id="00b97-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00b97-121">Header</span></span>        | <span data-ttu-id="00b97-122">Valor</span><span class="sxs-lookup"><span data-stu-id="00b97-122">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="00b97-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="00b97-123">Authorization</span></span> | <span data-ttu-id="00b97-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00b97-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="00b97-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="00b97-126">Content-Type</span></span>  | <span data-ttu-id="00b97-127">aplicación/zip</span><span class="sxs-lookup"><span data-stu-id="00b97-127">application/zip</span></span> |

## <a name="request-body"></a><span data-ttu-id="00b97-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="00b97-128">Request body</span></span>

<span data-ttu-id="00b97-129">Carga de los equipos Zip manifiesto: Para la aplicación de los equipos zip archivo [consulte Creación de un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span><span class="sxs-lookup"><span data-stu-id="00b97-129">Teams Zip Manifest Payload: For Teams application zip file [see Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span></span>

><span data-ttu-id="00b97-130">**Nota:** Use el identificador devuelto de la llamada [lista publica aplicaciones](./teamsapp-list.md) para hacer referencia a la aplicación que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="00b97-130">**Note:** Use the ID returned from the [List published apps](./teamsapp-list.md) call for to reference the app you'd like to update.</span></span> <span data-ttu-id="00b97-131">No use el identificador del manifiesto del paquete de la aplicación de zip.</span><span class="sxs-lookup"><span data-stu-id="00b97-131">Do not use the ID from the manifest of the zip app package.</span></span>

## <a name="response"></a><span data-ttu-id="00b97-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00b97-132">Response</span></span>

```
HTTP/1.1 204 No Content
```

## <a name="example"></a><span data-ttu-id="00b97-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00b97-133">Example</span></span>

### <a name="request"></a><span data-ttu-id="00b97-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="00b97-134">Request</span></span>

```
PUT https://graph.microsoft.com/beta/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8
Content-type: application/zip
Content-length: 244

[Zip file containing a Teams app package]
```

<span data-ttu-id="00b97-135">Para la aplicación de los equipos zip archivo [vea Crear paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span><span class="sxs-lookup"><span data-stu-id="00b97-135">For Teams application zip file [see Create app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span></span>

### <a name="response"></a><span data-ttu-id="00b97-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00b97-136">Response</span></span>

```
HTTP/1.1 204 No Content
```
