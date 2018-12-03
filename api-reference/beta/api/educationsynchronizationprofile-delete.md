---
title: Eliminar un educationSynchronizationProfile
description: Eliminar un perfil de sincronización de datos de school en el inquilino según el identificador.
ms.openlocfilehash: 829b723b48eb9a15750bc9d0e00ba50d432e8ab6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087776"
---
# <a name="delete-a-educationsynchronizationprofile"></a><span data-ttu-id="ecf70-103">Eliminar un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="ecf70-103">Delete a educationSynchronizationProfile</span></span>

> <span data-ttu-id="ecf70-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ecf70-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ecf70-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ecf70-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ecf70-106">Eliminar school datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino según el identificador.</span><span class="sxs-lookup"><span data-stu-id="ecf70-106">Delete a school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant based on the identifier.</span></span>

## <a name="permissions"></a><span data-ttu-id="ecf70-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ecf70-107">Permissions</span></span>
<span data-ttu-id="ecf70-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ecf70-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ecf70-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ecf70-110">Permission type</span></span> | <span data-ttu-id="ecf70-111">Permissions</span><span class="sxs-lookup"><span data-stu-id="ecf70-111">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="ecf70-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ecf70-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ecf70-113">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ecf70-113">EduAdministration.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ecf70-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ecf70-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /synchronizationProfiles/{id}
```

## <a name="request-headers"></a><span data-ttu-id="ecf70-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ecf70-115">Request headers</span></span>
| <span data-ttu-id="ecf70-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="ecf70-116">Name</span></span>       | <span data-ttu-id="ecf70-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="ecf70-117">Type</span></span> | <span data-ttu-id="ecf70-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecf70-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ecf70-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ecf70-119">Authorization</span></span>  | <span data-ttu-id="ecf70-120">string</span><span class="sxs-lookup"><span data-stu-id="ecf70-120">string</span></span>  | <span data-ttu-id="ecf70-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ecf70-p103">Bearer {token}. Required.</span></span>  |
|<span data-ttu-id="ecf70-123">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="ecf70-123">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="ecf70-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ecf70-124">Not supported.</span></span>|
|<span data-ttu-id="ecf70-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ecf70-125">Application</span></span>|<span data-ttu-id="ecf70-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ecf70-126">Not supported.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ecf70-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ecf70-127">Request body</span></span>
<span data-ttu-id="ecf70-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ecf70-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="ecf70-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ecf70-129">Response</span></span>
<span data-ttu-id="ecf70-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted`, pero no el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ecf70-130">If successful, this method returns a `202 Accepted` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="ecf70-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ecf70-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ecf70-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ecf70-132">Request</span></span>
<span data-ttu-id="ecf70-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ecf70-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_synchronizationProfile"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}
```

##### <a name="response"></a><span data-ttu-id="ecf70-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ecf70-134">Response</span></span>
<span data-ttu-id="ecf70-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ecf70-135">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```