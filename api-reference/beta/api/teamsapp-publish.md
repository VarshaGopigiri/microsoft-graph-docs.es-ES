---
title: Permisos
description: 'Publicar una aplicación en el catálogo de aplicaciones de Microsoft Teams. '
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 656b4a148f1d53cb44e303265af5624ccd1e423b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932927"
---
# <a name="publish-apps-to-your-organizations-app-catalog"></a><span data-ttu-id="00f11-103">Publicar aplicaciones en el catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="00f11-103">Publish apps to your organization's app catalog</span></span>

> <span data-ttu-id="00f11-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="00f11-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="00f11-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="00f11-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="00f11-106">Publicar una [aplicación](../resources/teamsapp.md) en el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="00f11-106">Publish an [app](../resources/teamsapp.md) to the Microsoft Teams apps catalog.</span></span> <span data-ttu-id="00f11-107">En concreto, esta API publica la aplicación al catálogo de su organización (el catálogo de aplicaciones de inquilino); el recurso creado tendrá `distributionMethod`  =  `organization`.</span><span class="sxs-lookup"><span data-stu-id="00f11-107">Specifically, this API publishes the app to your organization's catalog (the tenant app catalog); the created resource will have `distributionMethod` = `organization`.</span></span>

## <a name="permissions"></a><span data-ttu-id="00f11-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="00f11-108">Permissions</span></span>

<span data-ttu-id="00f11-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="00f11-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="00f11-111">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="00f11-111">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="00f11-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="00f11-112">Permission Type</span></span>                        | <span data-ttu-id="00f11-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="00f11-113">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="00f11-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="00f11-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="00f11-115">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00f11-115">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="00f11-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="00f11-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="00f11-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="00f11-117">Not supported</span></span>|
| <span data-ttu-id="00f11-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="00f11-118">Application</span></span>                            | <span data-ttu-id="00f11-119">No se admite</span><span class="sxs-lookup"><span data-stu-id="00f11-119">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="00f11-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00f11-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /appCatalogs/teamsApps
```

## <a name="request-headers"></a><span data-ttu-id="00f11-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="00f11-121">Request headers</span></span>

| <span data-ttu-id="00f11-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00f11-122">Header</span></span>        | <span data-ttu-id="00f11-123">Valor</span><span class="sxs-lookup"><span data-stu-id="00f11-123">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="00f11-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="00f11-124">Authorization</span></span> | <span data-ttu-id="00f11-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00f11-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="00f11-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="00f11-127">Content-Type</span></span>  | <span data-ttu-id="00f11-128">aplicación/zip</span><span class="sxs-lookup"><span data-stu-id="00f11-128">application/zip</span></span> |

## <a name="request-body"></a><span data-ttu-id="00f11-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="00f11-129">Request body</span></span>

<span data-ttu-id="00f11-130">Carga de manifiesto Zip de los equipos.</span><span class="sxs-lookup"><span data-stu-id="00f11-130">Teams Zip Manifest Payload.</span></span> <span data-ttu-id="00f11-131">Para la aplicación de los equipos zip de archivo, [vea Crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="00f11-131">For Teams application zip file [see Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> <span data-ttu-id="00f11-132">No se puede crear una aplicación para una organización que tiene el mismo identificador de manifiesto que otra aplicación en esa organización.</span><span class="sxs-lookup"><span data-stu-id="00f11-132">You can't create an app for an organization that has the same manifest ID as another app in that organization.</span></span>

## <a name="response"></a><span data-ttu-id="00f11-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00f11-133">Response</span></span>

<span data-ttu-id="00f11-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="00f11-134">If successful, this method returns a `200 OK` response code and a [teamsCatalogApp](../resources/teamsapp.md) object.</span></span>

## <a name="example"></a><span data-ttu-id="00f11-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00f11-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="00f11-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="00f11-136">Request</span></span>

```http
POST https://graph.microsoft.com/beta/appCatalogs/teamsApps
Content-type: application/zip
Content-length: 244

[Zip file containing a Teams app package]
```

<span data-ttu-id="00f11-137">Para obtener información acerca de cómo crear un archivo zip de aplicación de Microsoft Teams, consulte [crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="00f11-137">For information about how to create a Microsoft Teams application zip file, see [Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> 

### <a name="response"></a><span data-ttu-id="00f11-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00f11-138">Response</span></span>

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
