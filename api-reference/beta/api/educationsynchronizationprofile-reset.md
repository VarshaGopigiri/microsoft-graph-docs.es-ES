---
title: Restablecer la sincronización en un educationSynchronizationProfile
description: Restablecer la sincronización de un perfil de sincronización de datos de school específicos en el inquilino.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 54352d29280d671aaddc152307d8669f64c11bdc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808543"
---
# <a name="reset-sync-on-an-educationsynchronizationprofile"></a><span data-ttu-id="49aa2-103">Restablecer la sincronización en un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="49aa2-103">Reset sync on an educationSynchronizationProfile</span></span>

> <span data-ttu-id="49aa2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="49aa2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="49aa2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="49aa2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="49aa2-106">Restablecer la sincronización de escuela específico datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino.</span><span class="sxs-lookup"><span data-stu-id="49aa2-106">Reset the sync of a specific school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span>

> <span data-ttu-id="49aa2-107">**Nota:** Esta operación hará que la sincronización para reiniciar.</span><span class="sxs-lookup"><span data-stu-id="49aa2-107">**Note:** This operation will cause synchronization to restart.</span></span> <span data-ttu-id="49aa2-108">Se eliminarán todos los errores detectados.</span><span class="sxs-lookup"><span data-stu-id="49aa2-108">Any errors encountered will be deleted.</span></span> <span data-ttu-id="49aa2-109">Datos no se eliminarán de Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="49aa2-109">No data will be deleted from Azure Active Directory (Azure AD).</span></span> 

## <a name="permissions"></a><span data-ttu-id="49aa2-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="49aa2-110">Permissions</span></span>
<span data-ttu-id="49aa2-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="49aa2-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="49aa2-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="49aa2-113">Permission type</span></span> | <span data-ttu-id="49aa2-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="49aa2-114">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="49aa2-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="49aa2-115">Delegated (work or school account)</span></span> | <span data-ttu-id="49aa2-116">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="49aa2-116">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="49aa2-117">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="49aa2-117">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="49aa2-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49aa2-118">Not supported.</span></span>|
|<span data-ttu-id="49aa2-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="49aa2-119">Application</span></span>|<span data-ttu-id="49aa2-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49aa2-120">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="49aa2-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49aa2-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /synchronizationProfiles/{id}/reset
```

## <a name="request-headers"></a><span data-ttu-id="49aa2-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="49aa2-122">Request headers</span></span>
| <span data-ttu-id="49aa2-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="49aa2-123">Name</span></span>       | <span data-ttu-id="49aa2-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="49aa2-124">Type</span></span> | <span data-ttu-id="49aa2-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="49aa2-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="49aa2-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="49aa2-126">Authorization</span></span>  | <span data-ttu-id="49aa2-127">string</span><span class="sxs-lookup"><span data-stu-id="49aa2-127">string</span></span>  | <span data-ttu-id="49aa2-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="49aa2-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="49aa2-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="49aa2-130">Request body</span></span>
<span data-ttu-id="49aa2-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="49aa2-131">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="49aa2-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49aa2-132">Response</span></span>
<span data-ttu-id="49aa2-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="49aa2-133">If successful, this method returns a `200 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="49aa2-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49aa2-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="49aa2-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49aa2-135">Request</span></span>
<span data-ttu-id="49aa2-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49aa2-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_educationSynchronizationProfile_reset"
}-->
```http
POST https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/reset
```

##### <a name="response"></a><span data-ttu-id="49aa2-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49aa2-137">Response</span></span>

<span data-ttu-id="49aa2-138">No hay ningún cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49aa2-138">There is no response body.</span></span>

<!-- {
  "blockType": "response",
  "name": "post_educationSynchronizationProfile_reset"
}-->
```
HTTP/1.1 200 OK
```
