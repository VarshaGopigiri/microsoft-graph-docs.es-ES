---
title: Obtener el estado de un educationSynchronizationProfile
description: Obtener el estado de un perfil de sincronización de datos de school específicos en el inquilino. La respuesta indicará el estado de la sincronización.
ms.openlocfilehash: 87ced84dc0960eb6d5808fb8d21bc40d9d9e64e2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084006"
---
# <a name="get-the-status-of-an-educationsynchronizationprofile"></a><span data-ttu-id="411ed-104">Obtener el estado de un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="411ed-104">Get the status of an educationSynchronizationProfile</span></span>

> <span data-ttu-id="411ed-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="411ed-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="411ed-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="411ed-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="411ed-107">Obtener el estado de de datos específicos de escuela [perfil de sincronización](../resources/educationsynchronizationprofile.md) en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="411ed-107">Get the status of a specific school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span> <span data-ttu-id="411ed-108">La respuesta indicará el estado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="411ed-108">The response will indicate the status of the sync.</span></span>

## <a name="permissions"></a><span data-ttu-id="411ed-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="411ed-109">Permissions</span></span>
<span data-ttu-id="411ed-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="411ed-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="411ed-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="411ed-112">Permission type</span></span> | <span data-ttu-id="411ed-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="411ed-113">Permissions (from least to most privileged)</span></span> |
|:-----------|:----------|
| <span data-ttu-id="411ed-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="411ed-114">Delegated (work or school account)</span></span> | <span data-ttu-id="411ed-115">EduAdministration.Read, EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="411ed-115">EduAdministration.Read, EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="411ed-116">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="411ed-116">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="411ed-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="411ed-117">Not supported.</span></span>|
|<span data-ttu-id="411ed-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="411ed-118">Application</span></span>| <span data-ttu-id="411ed-119">EduAdministration.Read.All, EduAdministration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="411ed-119">EduAdministration.Read.All, EduAdministration.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="411ed-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="411ed-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /synchronizationProfiles/{id}/profileStatus
```

## <a name="request-headers"></a><span data-ttu-id="411ed-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="411ed-121">Request headers</span></span>
| <span data-ttu-id="411ed-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="411ed-122">Name</span></span>       | <span data-ttu-id="411ed-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="411ed-123">Type</span></span> | <span data-ttu-id="411ed-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="411ed-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="411ed-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="411ed-125">Authorization</span></span>  | <span data-ttu-id="411ed-126">string</span><span class="sxs-lookup"><span data-stu-id="411ed-126">string</span></span>  | <span data-ttu-id="411ed-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="411ed-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="411ed-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="411ed-129">Request body</span></span>
<span data-ttu-id="411ed-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="411ed-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="411ed-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="411ed-131">Response</span></span>
<span data-ttu-id="411ed-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [educationsynchronizationprofilestatus](../resources/educationsynchronizationprofilestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="411ed-132">If successful, this method returns a `200 OK` response code and an [educationsynchronizationprofilestatus](../resources/educationsynchronizationprofilestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="411ed-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="411ed-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="411ed-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="411ed-134">Request</span></span>
<span data-ttu-id="411ed-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="411ed-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationSynchronizationProfile_status"
}-->
```http
GET https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/profileStatus
```

##### <a name="response"></a><span data-ttu-id="411ed-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="411ed-136">Response</span></span>
<span data-ttu-id="411ed-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="411ed-137">The following is an example of the response.</span></span> 

><span data-ttu-id="411ed-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="411ed-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "@odata.type": "#microsoft.graph.educationSynchronizationProfileStatus",
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 232

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/synchronizationProfiles('{id}')/profileStatus/$entity",
    "status": "inProgress",
    "lastSynchronizationDateTime": "2017-07-04T22:06:37.6472621Z"
}
```
