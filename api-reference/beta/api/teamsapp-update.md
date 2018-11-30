---
title: Permissions
description: 'Actualizar una aplicación que se publicaron anteriormente en el catálogo de aplicaciones de Microsoft Teams. '
ms.openlocfilehash: f63b75fe3373ad89148b2901b828dcc0ae1f95a3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090021"
---
# <a name="update-apps-published-to-your-organizations-app-catalog"></a><span data-ttu-id="2f458-103">Actualizar aplicaciones publicadas en catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="2f458-103">Update apps published to your organization's app catalog</span></span>

> <span data-ttu-id="2f458-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2f458-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2f458-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2f458-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2f458-106">Actualización de una [aplicación](../resources/teamsapp.md) se publicaron anteriormente en el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2f458-106">Update an [app](../resources/teamsapp.md) previously published to the Microsoft Teams app catalog.</span></span> <span data-ttu-id="2f458-107">Esta API específicamente actualiza una aplicación publicada en catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino).</span><span class="sxs-lookup"><span data-stu-id="2f458-107">This API specifically updates an app published to your organization's app catalog (the tenant app catalog).</span></span> <span data-ttu-id="2f458-108">Para publicar en el catálogo de aplicaciones de la organización, especifique `organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="2f458-108">To publish to your organization's app catalog, specify `organization` as the **distributionMethod** in the [teamsCatalogApp](../resources/teamsapp.md) resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="2f458-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="2f458-109">Permissions</span></span>

<span data-ttu-id="2f458-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="2f458-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="2f458-112">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2f458-112">**Note:** Only global administrators can call this API.</span></span>

| <span data-ttu-id="2f458-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2f458-113">Permission Type</span></span>                        | <span data-ttu-id="2f458-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2f458-114">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="2f458-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2f458-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="2f458-116">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2f458-116">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="2f458-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2f458-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2f458-118">No admitido</span><span class="sxs-lookup"><span data-stu-id="2f458-118">Not supported</span></span>|
| <span data-ttu-id="2f458-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2f458-119">Application</span></span>                            | <span data-ttu-id="2f458-120">No se admite</span><span class="sxs-lookup"><span data-stu-id="2f458-120">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="2f458-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2f458-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /appCatalogs/teamsApps/{id}
```

## <a name="request-headers"></a><span data-ttu-id="2f458-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2f458-122">Request headers</span></span>

| <span data-ttu-id="2f458-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f458-123">Header</span></span>        | <span data-ttu-id="2f458-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2f458-124">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="2f458-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="2f458-125">Authorization</span></span> | <span data-ttu-id="2f458-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2f458-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="2f458-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2f458-128">Content-Type</span></span>  | <span data-ttu-id="2f458-129">aplicación/zip</span><span class="sxs-lookup"><span data-stu-id="2f458-129">application/zip</span></span> |

## <a name="request-body"></a><span data-ttu-id="2f458-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2f458-130">Request body</span></span>

<span data-ttu-id="2f458-131">Carga de los equipos Zip manifiesto: Para la aplicación de los equipos zip archivo [consulte Creación de un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span><span class="sxs-lookup"><span data-stu-id="2f458-131">Teams Zip Manifest Payload: For Teams application zip file [see Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span></span>

><span data-ttu-id="2f458-132">**Nota:** Use el identificador devuelto de la llamada [lista publica aplicaciones](./teamsapp-list.md) para hacer referencia a la aplicación que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="2f458-132">**Note:** Use the ID returned from the [List published apps](./teamsapp-list.md) call for to reference the app you'd like to update.</span></span> <span data-ttu-id="2f458-133">No use el identificador del manifiesto del paquete de la aplicación de zip.</span><span class="sxs-lookup"><span data-stu-id="2f458-133">Do not use the ID from the manifest of the zip app package.</span></span>

## <a name="response"></a><span data-ttu-id="2f458-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f458-134">Response</span></span>

```
HTTP/1.1 204 No Content
```

## <a name="example"></a><span data-ttu-id="2f458-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f458-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="2f458-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2f458-136">Request</span></span>

```
PUT https://graph.microsoft.com/beta/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8
Content-type: application/zip
Content-length: 244

[Zip file containing a Teams app package]
```

<span data-ttu-id="2f458-137">Para la aplicación de los equipos zip archivo [vea Crear paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span><span class="sxs-lookup"><span data-stu-id="2f458-137">For Teams application zip file [see Create app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span></span>

### <a name="response"></a><span data-ttu-id="2f458-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f458-138">Response</span></span>

```
HTTP/1.1 204 No Content
```
