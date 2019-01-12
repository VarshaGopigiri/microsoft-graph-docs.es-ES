---
title: Restablecer la sincronización en un educationSynchronizationProfile
description: Restablecer la sincronización de un perfil de sincronización de datos de school específicos en el inquilino.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: e397a5d3a1a49cc827ed6ad72d1fc9fbeca01299
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984580"
---
# <a name="reset-sync-on-an-educationsynchronizationprofile"></a><span data-ttu-id="bdd15-103">Restablecer la sincronización en un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="bdd15-103">Reset sync on an educationSynchronizationProfile</span></span>

> <span data-ttu-id="bdd15-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bdd15-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bdd15-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bdd15-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bdd15-106">Restablecer la sincronización de escuela específico datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino.</span><span class="sxs-lookup"><span data-stu-id="bdd15-106">Reset the sync of a specific school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span>

> <span data-ttu-id="bdd15-107">**Nota:** Esta operación hará que la sincronización para reiniciar.</span><span class="sxs-lookup"><span data-stu-id="bdd15-107">**Note:** This operation will cause synchronization to restart.</span></span> <span data-ttu-id="bdd15-108">Se eliminarán todos los errores detectados.</span><span class="sxs-lookup"><span data-stu-id="bdd15-108">Any errors encountered will be deleted.</span></span> <span data-ttu-id="bdd15-109">Datos no se eliminarán de Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="bdd15-109">No data will be deleted from Azure Active Directory (Azure AD).</span></span> 

## <a name="permissions"></a><span data-ttu-id="bdd15-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="bdd15-110">Permissions</span></span>
<span data-ttu-id="bdd15-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bdd15-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="bdd15-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bdd15-113">Permission type</span></span> | <span data-ttu-id="bdd15-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="bdd15-114">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="bdd15-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bdd15-115">Delegated (work or school account)</span></span> | <span data-ttu-id="bdd15-116">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bdd15-116">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="bdd15-117">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="bdd15-117">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="bdd15-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bdd15-118">Not supported.</span></span>|
|<span data-ttu-id="bdd15-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bdd15-119">Application</span></span>|<span data-ttu-id="bdd15-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bdd15-120">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bdd15-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bdd15-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /synchronizationProfiles/{id}/reset
```

## <a name="request-headers"></a><span data-ttu-id="bdd15-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bdd15-122">Request headers</span></span>
| <span data-ttu-id="bdd15-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="bdd15-123">Name</span></span>       | <span data-ttu-id="bdd15-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="bdd15-124">Type</span></span> | <span data-ttu-id="bdd15-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdd15-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bdd15-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="bdd15-126">Authorization</span></span>  | <span data-ttu-id="bdd15-127">string</span><span class="sxs-lookup"><span data-stu-id="bdd15-127">string</span></span>  | <span data-ttu-id="bdd15-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bdd15-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="bdd15-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bdd15-130">Request body</span></span>
<span data-ttu-id="bdd15-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bdd15-131">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="bdd15-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdd15-132">Response</span></span>
<span data-ttu-id="bdd15-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="bdd15-133">If successful, this method returns a `200 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="bdd15-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bdd15-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bdd15-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bdd15-135">Request</span></span>
<span data-ttu-id="bdd15-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bdd15-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_educationSynchronizationProfile_reset"
}-->
```http
POST https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/reset
```

##### <a name="response"></a><span data-ttu-id="bdd15-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdd15-137">Response</span></span>

<span data-ttu-id="bdd15-138">No hay ningún cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bdd15-138">There is no response body.</span></span>

<!-- {
  "blockType": "response",
  "name": "post_educationSynchronizationProfile_reset"
}-->
```
HTTP/1.1 200 OK
```
