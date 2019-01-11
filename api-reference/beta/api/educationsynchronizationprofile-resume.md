---
title: Reanudar la sincronización en un educationSynchronizationProfile
description: Reanudar la sincronización de un perfil de sincronización de datos de school específicos en el inquilino.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: c68fb6d042d92fd0f1334dc498b175c27cbc4ced
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894211"
---
# <a name="resume-sync-on-an-educationsynchronizationprofile"></a><span data-ttu-id="21811-103">Reanudar la sincronización en un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="21811-103">Resume sync on an educationSynchronizationProfile</span></span>

> <span data-ttu-id="21811-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="21811-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="21811-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="21811-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="21811-106">Reanudar la sincronización de escuela específico datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino.</span><span class="sxs-lookup"><span data-stu-id="21811-106">Resume the sync of a specific school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="21811-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="21811-107">Permissions</span></span>
<span data-ttu-id="21811-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21811-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="21811-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21811-110">Permission type</span></span> | <span data-ttu-id="21811-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="21811-111">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="21811-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21811-112">Delegated (work or school account)</span></span> | <span data-ttu-id="21811-113">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="21811-113">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="21811-114">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="21811-114">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="21811-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21811-115">Not supported.</span></span>|
|<span data-ttu-id="21811-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21811-116">Application</span></span>|<span data-ttu-id="21811-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21811-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="21811-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21811-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /synchronizationProfiles/{id}/resume
```

## <a name="request-headers"></a><span data-ttu-id="21811-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21811-119">Request headers</span></span>
| <span data-ttu-id="21811-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="21811-120">Name</span></span>       | <span data-ttu-id="21811-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="21811-121">Type</span></span> | <span data-ttu-id="21811-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="21811-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="21811-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="21811-123">Authorization</span></span>  | <span data-ttu-id="21811-124">string</span><span class="sxs-lookup"><span data-stu-id="21811-124">string</span></span>  | <span data-ttu-id="21811-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="21811-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="21811-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21811-127">Request body</span></span>
<span data-ttu-id="21811-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="21811-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="21811-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21811-129">Response</span></span>
<span data-ttu-id="21811-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="21811-130">If successful, this method returns a `200 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="21811-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21811-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="21811-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21811-132">Request</span></span>
<span data-ttu-id="21811-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21811-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_educationSynchronizationProfile_resume"
}-->
```http
POST https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/resume
```

##### <a name="response"></a><span data-ttu-id="21811-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21811-134">Response</span></span>

<span data-ttu-id="21811-135">No hay ningún cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21811-135">There is no response body.</span></span>

<!-- {
  "blockType": "response",
  "name": "post_educationSynchronizationProfile_resume"
}-->
```
HTTP/1.1 200 OK
```
