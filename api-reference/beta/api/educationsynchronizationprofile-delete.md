---
title: Eliminar un educationSynchronizationProfile
description: Eliminar un perfil de sincronización de datos de school en el inquilino según el identificador.
author: mmast-msft
ms.openlocfilehash: b0287133d579915279e0f9a02bf49dd981ccf419
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343305"
---
# <a name="delete-a-educationsynchronizationprofile"></a><span data-ttu-id="a6230-103">Eliminar un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="a6230-103">Delete a educationSynchronizationProfile</span></span>

> <span data-ttu-id="a6230-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a6230-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a6230-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a6230-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a6230-106">Eliminar school datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino según el identificador.</span><span class="sxs-lookup"><span data-stu-id="a6230-106">Delete a school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant based on the identifier.</span></span>

## <a name="permissions"></a><span data-ttu-id="a6230-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a6230-107">Permissions</span></span>
<span data-ttu-id="a6230-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a6230-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a6230-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a6230-110">Permission type</span></span> | <span data-ttu-id="a6230-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="a6230-111">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="a6230-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a6230-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a6230-113">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a6230-113">EduAdministration.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a6230-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6230-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /synchronizationProfiles/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a6230-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a6230-115">Request headers</span></span>
| <span data-ttu-id="a6230-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6230-116">Name</span></span>       | <span data-ttu-id="a6230-117">Type</span><span class="sxs-lookup"><span data-stu-id="a6230-117">Type</span></span> | <span data-ttu-id="a6230-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6230-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a6230-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="a6230-119">Authorization</span></span>  | <span data-ttu-id="a6230-120">string</span><span class="sxs-lookup"><span data-stu-id="a6230-120">string</span></span>  | <span data-ttu-id="a6230-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a6230-p103">Bearer {token}. Required.</span></span>  |
|<span data-ttu-id="a6230-123">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="a6230-123">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="a6230-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6230-124">Not supported.</span></span>|
|<span data-ttu-id="a6230-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a6230-125">Application</span></span>|<span data-ttu-id="a6230-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6230-126">Not supported.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a6230-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6230-127">Request body</span></span>
<span data-ttu-id="a6230-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a6230-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="a6230-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6230-129">Response</span></span>
<span data-ttu-id="a6230-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted`, pero no el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6230-130">If successful, this method returns a `202 Accepted` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="a6230-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6230-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a6230-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a6230-132">Request</span></span>
<span data-ttu-id="a6230-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6230-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_synchronizationProfile"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}
```

##### <a name="response"></a><span data-ttu-id="a6230-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6230-134">Response</span></span>
<span data-ttu-id="a6230-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6230-135">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```
