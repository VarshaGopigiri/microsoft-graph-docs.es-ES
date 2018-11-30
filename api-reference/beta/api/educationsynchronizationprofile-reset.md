---
title: Restablecer la sincronización en un educationSynchronizationProfile
description: Restablecer la sincronización de un perfil de sincronización de datos de school específicos en el inquilino.
ms.openlocfilehash: 4be91b7d6229148c51dc8fb1279a9078fb5cad7b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087717"
---
# <a name="reset-sync-on-an-educationsynchronizationprofile"></a><span data-ttu-id="7dcb4-103">Restablecer la sincronización en un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="7dcb4-103">Reset sync on an educationSynchronizationProfile</span></span>

> <span data-ttu-id="7dcb4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7dcb4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7dcb4-106">Restablecer la sincronización de escuela específico datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-106">Reset the sync of a specific school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span>

> <span data-ttu-id="7dcb4-107">**Nota:** Esta operación hará que la sincronización para reiniciar.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-107">**Note:** This operation will cause synchronization to restart.</span></span> <span data-ttu-id="7dcb4-108">Se eliminarán todos los errores detectados.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-108">Any errors encountered will be deleted.</span></span> <span data-ttu-id="7dcb4-109">Datos no se eliminarán de Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="7dcb4-109">No data will be deleted from Azure Active Directory (Azure AD).</span></span> 

## <a name="permissions"></a><span data-ttu-id="7dcb4-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="7dcb4-110">Permissions</span></span>
<span data-ttu-id="7dcb4-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7dcb4-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7dcb4-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7dcb4-113">Permission type</span></span> | <span data-ttu-id="7dcb4-114">Permissions</span><span class="sxs-lookup"><span data-stu-id="7dcb4-114">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="7dcb4-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7dcb4-115">Delegated (work or school account)</span></span> | <span data-ttu-id="7dcb4-116">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7dcb4-116">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="7dcb4-117">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="7dcb4-117">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="7dcb4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-118">Not supported.</span></span>|
|<span data-ttu-id="7dcb4-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7dcb4-119">Application</span></span>|<span data-ttu-id="7dcb4-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-120">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7dcb4-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7dcb4-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /synchronizationProfiles/{id}/reset
```

## <a name="request-headers"></a><span data-ttu-id="7dcb4-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7dcb4-122">Request headers</span></span>
| <span data-ttu-id="7dcb4-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="7dcb4-123">Name</span></span>       | <span data-ttu-id="7dcb4-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="7dcb4-124">Type</span></span> | <span data-ttu-id="7dcb4-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dcb4-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7dcb4-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="7dcb4-126">Authorization</span></span>  | <span data-ttu-id="7dcb4-127">string</span><span class="sxs-lookup"><span data-stu-id="7dcb4-127">string</span></span>  | <span data-ttu-id="7dcb4-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7dcb4-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7dcb4-130">Request body</span></span>
<span data-ttu-id="7dcb4-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-131">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="7dcb4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7dcb4-132">Response</span></span>
<span data-ttu-id="7dcb4-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-133">If successful, this method returns a `200 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="7dcb4-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7dcb4-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7dcb4-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7dcb4-135">Request</span></span>
<span data-ttu-id="7dcb4-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_educationSynchronizationProfile_reset"
}-->
```http
POST https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/reset
```

##### <a name="response"></a><span data-ttu-id="7dcb4-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7dcb4-137">Response</span></span>

<span data-ttu-id="7dcb4-138">No hay ningún cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-138">There is no response body.</span></span>

<!-- {
  "blockType": "response",
  "name": "post_educationSynchronizationProfile_reset"
}-->
```
HTTP/1.1 200 OK
```