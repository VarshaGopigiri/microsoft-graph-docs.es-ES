---
title: 'educationSynchronizationProfile: uploadUrl'
description: Recuperar una firma acceso compartido (SAS) para cargar archivos de origen para el almacenamiento de Azure blob para un perfil de sincronización de datos de school específicos en el inquilino. El token de SAS tiene una validez de una hora.
ms.openlocfilehash: cf685b56718664ca68e0fde697872fe624c7e7b1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088927"
---
# <a name="educationsynchronizationprofile-uploadurl"></a><span data-ttu-id="d7057-104">educationSynchronizationProfile: uploadUrl</span><span class="sxs-lookup"><span data-stu-id="d7057-104">educationSynchronizationProfile: uploadUrl</span></span>

> <span data-ttu-id="d7057-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7057-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7057-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7057-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d7057-107">Recuperar una firma acceso compartido (SAS) para cargar archivos de origen al almacenamiento de blobs Azure para school específico datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino.</span><span class="sxs-lookup"><span data-stu-id="d7057-107">Retrieve a shared access signature (SAS) for uploading source files to Azure blob storage for a specific school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span> <span data-ttu-id="d7057-108">El token de SAS tiene una validez de una hora.</span><span class="sxs-lookup"><span data-stu-id="d7057-108">The SAS token has a validity of one hour.</span></span>

<span data-ttu-id="d7057-109">La carga se proporciona la dirección URL sólo para el [proveedor de datos CSV](../resources/educationcsvdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="d7057-109">The upload URL is provided only for the [CSV data provider](../resources/educationcsvdataprovider.md).</span></span>

> <span data-ttu-id="d7057-110">**Nota:** Para tener acceso el almacenamiento de blobs con el token de SAS, use el [almacenamiento de Azure SDK](https://github.com/search?q=org%3AAzure+azure-storage) o [AzCopy](https://docs.microsoft.com/en-us/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="d7057-110">**Note:** To access the blob storage with the SAS token, use the [Azure storage SDKs](https://github.com/search?q=org%3AAzure+azure-storage) or [AzCopy](https://docs.microsoft.com/en-us/azure/storage/storage-use-azcopy).</span></span>

## <a name="permissions"></a><span data-ttu-id="d7057-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="d7057-111">Permissions</span></span>
<span data-ttu-id="d7057-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d7057-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="d7057-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7057-114">Permission type</span></span> | <span data-ttu-id="d7057-115">Permissions</span><span class="sxs-lookup"><span data-stu-id="d7057-115">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="d7057-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7057-116">Delegated (work or school account)</span></span> | <span data-ttu-id="d7057-117">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d7057-117">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="d7057-118">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="d7057-118">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="d7057-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7057-119">Not supported.</span></span>|
|<span data-ttu-id="d7057-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7057-120">Application</span></span>|<span data-ttu-id="d7057-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7057-121">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d7057-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7057-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /synchronizationProfiles/{id}/uploadUrl
```

## <a name="request-headers"></a><span data-ttu-id="d7057-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7057-123">Request headers</span></span>
| <span data-ttu-id="d7057-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="d7057-124">Name</span></span>       | <span data-ttu-id="d7057-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7057-125">Type</span></span> | <span data-ttu-id="d7057-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7057-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d7057-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="d7057-127">Authorization</span></span>  | <span data-ttu-id="d7057-128">string</span><span class="sxs-lookup"><span data-stu-id="d7057-128">string</span></span>  | <span data-ttu-id="d7057-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7057-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d7057-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7057-131">Request body</span></span>
<span data-ttu-id="d7057-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d7057-132">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="d7057-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7057-133">Response</span></span>
<span data-ttu-id="d7057-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una dirección URL de SAS para el [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7057-134">If successful, this method returns a `200 OK` response code and a SAS URL for the [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) in the response body.</span></span>

<span data-ttu-id="d7057-135">Si aún se está procesando una solicitud anterior, este método devuelve una `409 Conflict` que indica que la carga está bloqueada actualmente para la [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md).</span><span class="sxs-lookup"><span data-stu-id="d7057-135">If a previous request is still being processed, this method returns a `409 Conflict` indicating that the upload is presently blocked for the [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md).</span></span>

## <a name="example"></a><span data-ttu-id="d7057-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7057-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d7057-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7057-137">Request</span></span>
<span data-ttu-id="d7057-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7057-138">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationSynchronizationProfile_uploadurl"
}-->
```http
GET https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/uploadUrl
```

##### <a name="response"></a><span data-ttu-id="d7057-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7057-139">Response</span></span>
<span data-ttu-id="d7057-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7057-140">The following is an example of the response.</span></span> 

><span data-ttu-id="d7057-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d7057-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "@odata.type": "String",
} -->
```http
HTTP/1.1 201 OK
Content-type: application/json
Content-length: 314

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#String",
    "value": "https://sdsstorage.blob.core.windows.net/86904b1e-c7d0-4ead-b13a-98f11fc400ee?sv=2015-07-08&sr=c&si=SharedAccessPolicy_20170704044441&sig=CH65vxxqXETCkQNH0Lfsu31cUo0s0XcEEo0OE2YiL6Q%3D&se=2017-07-04T08%3A43%3A01Z&sp=w"
}
```