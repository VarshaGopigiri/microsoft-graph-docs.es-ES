---
title: Permisos
description: 'Publicar una aplicación en el catálogo de aplicaciones de Microsoft Teams. '
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 7faf5847b78d6221b5167c775def75ae9a2ce629
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911878"
---
# <a name="publish-apps-to-your-organizations-app-catalog"></a><span data-ttu-id="ff0a0-103">Publicar aplicaciones en el catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="ff0a0-103">Publish apps to your organization's app catalog</span></span>



<span data-ttu-id="ff0a0-104">Publicar una [aplicación](../resources/teamsapp.md) en el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ff0a0-104">Publish an [app](../resources/teamsapp.md) to the Microsoft Teams apps catalog.</span></span> <span data-ttu-id="ff0a0-105">En concreto, esta API publica la aplicación al catálogo de su organización (el catálogo de aplicaciones de inquilino); el recurso creado tendrá `distributionMethod`  =  `organization`.</span><span class="sxs-lookup"><span data-stu-id="ff0a0-105">Specifically, this API publishes the app to your organization's catalog (the tenant app catalog); the created resource will have `distributionMethod` = `organization`.</span></span>

## <a name="permissions"></a><span data-ttu-id="ff0a0-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="ff0a0-106">Permissions</span></span>

<span data-ttu-id="ff0a0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="ff0a0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="ff0a0-109">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ff0a0-109">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="ff0a0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ff0a0-110">Permission Type</span></span>                        | <span data-ttu-id="ff0a0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ff0a0-111">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="ff0a0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ff0a0-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="ff0a0-113">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ff0a0-113">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="ff0a0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ff0a0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ff0a0-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="ff0a0-115">Not supported</span></span>|
| <span data-ttu-id="ff0a0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ff0a0-116">Application</span></span>                            | <span data-ttu-id="ff0a0-117">No se admite</span><span class="sxs-lookup"><span data-stu-id="ff0a0-117">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="ff0a0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ff0a0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /appCatalogs/teamsApps
```

## <a name="request-headers"></a><span data-ttu-id="ff0a0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ff0a0-119">Request headers</span></span>

| <span data-ttu-id="ff0a0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff0a0-120">Header</span></span>        | <span data-ttu-id="ff0a0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ff0a0-121">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="ff0a0-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ff0a0-122">Authorization</span></span> | <span data-ttu-id="ff0a0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ff0a0-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ff0a0-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ff0a0-125">Content-Type</span></span>  | <span data-ttu-id="ff0a0-126">aplicación/zip</span><span class="sxs-lookup"><span data-stu-id="ff0a0-126">application/zip</span></span> |

## <a name="request-body"></a><span data-ttu-id="ff0a0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ff0a0-127">Request body</span></span>

<span data-ttu-id="ff0a0-128">Carga de manifiesto Zip de los equipos.</span><span class="sxs-lookup"><span data-stu-id="ff0a0-128">Teams Zip Manifest Payload.</span></span> <span data-ttu-id="ff0a0-129">Para la aplicación de los equipos zip de archivo, [vea Crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="ff0a0-129">For Teams application zip file [see Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> <span data-ttu-id="ff0a0-130">No se puede crear una aplicación para una organización que tiene el mismo identificador de manifiesto que otra aplicación en esa organización.</span><span class="sxs-lookup"><span data-stu-id="ff0a0-130">You can't create an app for an organization that has the same manifest ID as another app in that organization.</span></span>

## <a name="response"></a><span data-ttu-id="ff0a0-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff0a0-131">Response</span></span>

<span data-ttu-id="ff0a0-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0a0-132">If successful, this method returns a `200 OK` response code and a [teamsCatalogApp](../resources/teamsapp.md) object.</span></span>

## <a name="example"></a><span data-ttu-id="ff0a0-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff0a0-133">Example</span></span>

### <a name="request"></a><span data-ttu-id="ff0a0-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ff0a0-134">Request</span></span>

```http
POST https://graph.microsoft.com/beta/appCatalogs/teamsApps
Content-type: application/zip
Content-length: 244

[Zip file containing a Teams app package]
```

<span data-ttu-id="ff0a0-135">Para obtener información acerca de cómo crear un archivo zip de aplicación de Microsoft Teams, consulte [crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="ff0a0-135">For information about how to create a Microsoft Teams application zip file, see [Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> 

### <a name="response"></a><span data-ttu-id="ff0a0-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff0a0-136">Response</span></span>

```
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "e3e29acb-8c79-412b-b746-e6c39ff4cd22",
  "externalId": "b5561ec9-8cab-4aa3-8aa2-d8d7172e4311",
  "name": "Test App",
  "version": "1.0.0",
  "distributionMethod": "organization"
}
```
