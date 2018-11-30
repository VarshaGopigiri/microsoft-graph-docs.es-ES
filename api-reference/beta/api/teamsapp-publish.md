---
title: Permissions
description: 'Publicar una aplicación en el catálogo de aplicaciones de Microsoft Teams. '
ms.openlocfilehash: ae8dcf5e20da2ac18bb036ad40916496d91136f1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089569"
---
# <a name="publish-apps-to-your-organizations-app-catalog"></a><span data-ttu-id="c8ca8-103">Publicar aplicaciones en el catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="c8ca8-103">Publish apps to your organization's app catalog</span></span>

> <span data-ttu-id="c8ca8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c8ca8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c8ca8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c8ca8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c8ca8-106">Publicar una [aplicación](../resources/teamsapp.md) en el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c8ca8-106">Publish an [app](../resources/teamsapp.md) to the Microsoft Teams apps catalog.</span></span> <span data-ttu-id="c8ca8-107">En concreto, esta API publica la aplicación al catálogo de su organización (el catálogo de aplicaciones de inquilino); el recurso creado tendrá `distributionMethod`  =  `organization`.</span><span class="sxs-lookup"><span data-stu-id="c8ca8-107">Specifically, this API publishes the app to your organization's catalog (the tenant app catalog); the created resource will have `distributionMethod` = `organization`.</span></span>

## <a name="permissions"></a><span data-ttu-id="c8ca8-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="c8ca8-108">Permissions</span></span>

<span data-ttu-id="c8ca8-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="c8ca8-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="c8ca8-111">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c8ca8-111">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="c8ca8-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c8ca8-112">Permission Type</span></span>                        | <span data-ttu-id="c8ca8-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c8ca8-113">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="c8ca8-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c8ca8-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="c8ca8-115">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c8ca8-115">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="c8ca8-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c8ca8-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c8ca8-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="c8ca8-117">Not supported</span></span>|
| <span data-ttu-id="c8ca8-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c8ca8-118">Application</span></span>                            | <span data-ttu-id="c8ca8-119">No se admite</span><span class="sxs-lookup"><span data-stu-id="c8ca8-119">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="c8ca8-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c8ca8-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /appCatalogs/teamsApps
```

## <a name="request-headers"></a><span data-ttu-id="c8ca8-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c8ca8-121">Request headers</span></span>

| <span data-ttu-id="c8ca8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8ca8-122">Header</span></span>        | <span data-ttu-id="c8ca8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c8ca8-123">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="c8ca8-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="c8ca8-124">Authorization</span></span> | <span data-ttu-id="c8ca8-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c8ca8-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c8ca8-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c8ca8-127">Content-Type</span></span>  | <span data-ttu-id="c8ca8-128">aplicación/zip</span><span class="sxs-lookup"><span data-stu-id="c8ca8-128">application/zip</span></span> |

## <a name="request-body"></a><span data-ttu-id="c8ca8-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c8ca8-129">Request body</span></span>

<span data-ttu-id="c8ca8-130">Carga de manifiesto Zip de los equipos.</span><span class="sxs-lookup"><span data-stu-id="c8ca8-130">Teams Zip Manifest Payload.</span></span> <span data-ttu-id="c8ca8-131">Para la aplicación de los equipos zip de archivo, [vea Crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="c8ca8-131">For Teams application zip file [see Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> <span data-ttu-id="c8ca8-132">No se puede crear una aplicación para una organización que tiene el mismo identificador de manifiesto que otra aplicación en esa organización.</span><span class="sxs-lookup"><span data-stu-id="c8ca8-132">You can't create an app for an organization that has the same manifest ID as another app in that organization.</span></span>

## <a name="response"></a><span data-ttu-id="c8ca8-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8ca8-133">Response</span></span>

<span data-ttu-id="c8ca8-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="c8ca8-134">If successful, this method returns a `200 OK` response code and a [teamsCatalogApp](../resources/teamsapp.md) object.</span></span>

## <a name="example"></a><span data-ttu-id="c8ca8-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8ca8-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="c8ca8-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c8ca8-136">Request</span></span>

```http
POST https://graph.microsoft.com/beta/appCatalogs/teamsApps
Content-type: application/zip
Content-length: 244

[Zip file containing a Teams app package]
```

<span data-ttu-id="c8ca8-137">Para obtener información acerca de cómo crear un archivo zip de aplicación de Microsoft Teams, consulte [crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="c8ca8-137">For information about how to create a Microsoft Teams application zip file, see [Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> 

### <a name="response"></a><span data-ttu-id="c8ca8-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8ca8-138">Response</span></span>

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
