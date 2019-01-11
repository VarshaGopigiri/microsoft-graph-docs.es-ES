---
title: Iniciar sincronización después de cargar archivos en un educationSynchronizationProfile
description: Compruebe los archivos cargan en un perfil de sincronización de datos de school específicos en el inquilino. Si la comprobación se realiza correctamente, se iniciará la sincronización en el perfil. De lo contrario, la respuesta contendrá errores y advertencias. Si la respuesta contiene errores, no se iniciará la sincronización. Si la respuesta contiene sólo las advertencias, se iniciará la sincronización.
localization_priority: Normal
ms.openlocfilehash: 465ab6a807fc6af10067d048459c440c7c567361
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866741"
---
# <a name="start-sync-after-uploading-files-to-an-educationsynchronizationprofile"></a><span data-ttu-id="115d4-107">Iniciar sincronización después de cargar archivos en un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="115d4-107">Start sync after uploading files to an educationSynchronizationProfile</span></span>

> <span data-ttu-id="115d4-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="115d4-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="115d4-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="115d4-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="115d4-110">Compruebe los archivos cargan en school específico datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino.</span><span class="sxs-lookup"><span data-stu-id="115d4-110">Verify the files uploaded to a specific school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span> <span data-ttu-id="115d4-111">Si la comprobación se realiza correctamente, se iniciará la sincronización en el perfil.</span><span class="sxs-lookup"><span data-stu-id="115d4-111">If the verification is successful, synchronization will start on the profile.</span></span> <span data-ttu-id="115d4-112">De lo contrario, la respuesta contendrá errores y advertencias.</span><span class="sxs-lookup"><span data-stu-id="115d4-112">Otherwise, the response will contain errors and warnings.</span></span> <span data-ttu-id="115d4-113">Si la respuesta contiene errores, no se iniciará la sincronización.</span><span class="sxs-lookup"><span data-stu-id="115d4-113">If the response contains errors, the synchronization will not start.</span></span> <span data-ttu-id="115d4-114">Si la respuesta contiene sólo las advertencias, se iniciará la sincronización.</span><span class="sxs-lookup"><span data-stu-id="115d4-114">If the response contains only warnings, synchronization will start.</span></span>

> <span data-ttu-id="115d4-115">**Nota:** Use este método sólo cuando el proveedor de datos es del tipo [educationcsvdataprovider](../resources/educationcsvdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="115d4-115">**Note:** Use this method only when the data provider is of type [educationcsvdataprovider](../resources/educationcsvdataprovider.md).</span></span> <span data-ttu-id="115d4-116">Además, debe aprovisionarse antes de poder iniciar propiedad de estado del perfil.</span><span class="sxs-lookup"><span data-stu-id="115d4-116">Also, the profile's state property needs to be provisioned before it can be started.</span></span> <span data-ttu-id="115d4-117">Sondee el objeto de perfil para comprobar su propiedad state.</span><span class="sxs-lookup"><span data-stu-id="115d4-117">Poll the profile object to check its state property.</span></span>

## <a name="permissions"></a><span data-ttu-id="115d4-118">Permisos</span><span class="sxs-lookup"><span data-stu-id="115d4-118">Permissions</span></span>
<span data-ttu-id="115d4-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="115d4-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="115d4-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="115d4-121">Permission type</span></span> | <span data-ttu-id="115d4-122">Permisos</span><span class="sxs-lookup"><span data-stu-id="115d4-122">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="115d4-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="115d4-123">Delegated (work or school account)</span></span> | <span data-ttu-id="115d4-124">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="115d4-124">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="115d4-125">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="115d4-125">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="115d4-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="115d4-126">Not supported.</span></span>|
|<span data-ttu-id="115d4-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="115d4-127">Application</span></span>|<span data-ttu-id="115d4-128">No admitida.</span><span class="sxs-lookup"><span data-stu-id="115d4-128">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="115d4-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="115d4-129">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /synchronizationProfiles/{id}/start
```

## <a name="request-headers"></a><span data-ttu-id="115d4-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="115d4-130">Request headers</span></span>
| <span data-ttu-id="115d4-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="115d4-131">Name</span></span>       | <span data-ttu-id="115d4-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="115d4-132">Type</span></span> | <span data-ttu-id="115d4-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="115d4-133">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="115d4-134">Autorización</span><span class="sxs-lookup"><span data-stu-id="115d4-134">Authorization</span></span>  | <span data-ttu-id="115d4-135">string</span><span class="sxs-lookup"><span data-stu-id="115d4-135">string</span></span>  | <span data-ttu-id="115d4-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="115d4-p106">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="115d4-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="115d4-138">Request body</span></span>
<span data-ttu-id="115d4-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="115d4-139">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="115d4-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="115d4-140">Response</span></span>
<span data-ttu-id="115d4-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="115d4-141">If successful, this method returns a `200 OK` response code.</span></span> <span data-ttu-id="115d4-142">Si no lo consigue, devuelve un `400 Bad Request`.</span><span class="sxs-lookup"><span data-stu-id="115d4-142">If unsuccessful, it returns a `400 Bad Request`.</span></span> <span data-ttu-id="115d4-143">La respuesta contiene una colección de objetos de [educationFileSynchronizationVerificationMessage](../resources/educationfilesynchronizationverificationmessage.md) como parte del cuerpo de la respuesta si se han encontrado los errores o advertencias.</span><span class="sxs-lookup"><span data-stu-id="115d4-143">The response contains a collection of [educationFileSynchronizationVerificationMessage](../resources/educationfilesynchronizationverificationmessage.md) objects as part of the response body if any errors or warnings were found.</span></span>

## <a name="example"></a><span data-ttu-id="115d4-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="115d4-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="115d4-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="115d4-145">Request</span></span>
<span data-ttu-id="115d4-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="115d4-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_educationSynchronizationProfile_start"
}-->
```http
POST https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/start
```

##### <a name="response"></a><span data-ttu-id="115d4-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="115d4-147">Response</span></span>
<span data-ttu-id="115d4-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="115d4-148">Here is an example of the response.</span></span> 

><span data-ttu-id="115d4-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="115d4-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationFileSynchronizationVerificationMessage",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 2105

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/Collection(microsoft.graph.verificationMessage)",
    "value": [
        {
            "type": "Error",
            "fileName": "section.csv",
            "description": "5 row(s) have missing data for the field - SIS ID"
        },
        {
            "type": "Error",
            "fileName": "section.csv",
            "description": "5 row(s) have an invalid format for the field - SIS ID"
        },
        {
            "type": "Warning",
            "fileName": "student.csv",
            "description": "3 duplicates found in column SIS ID which requires values to be Unique."
        },
        {
            "type": "Warning",
            "fileName": "student.csv",
            "description": "3 duplicates found in column Username which requires values to be Unique."
        },
        {
            "type": "Error",
            "fileName": "studentenrollment.csv",
            "description": "125 row(s) have referenced data not found in source. Field - Section SIS ID"
        },
        {
            "type": "Error",
            "fileName": "studentenrollment.csv",
            "description": "35 row(s) have referenced data not found in source. Field - SIS ID"
        },
        {
            "type": "Warning",
            "fileName": "teacher.csv",
            "description": "3 duplicates found in column SIS ID which requires values to be Unique."
        },
        {
            "type": "Warning",
            "fileName": "teacher.csv",
            "description": "3 duplicates found in column Username which requires values to be Unique."
        },
        {
            "type": "Error",
            "fileName": "teacherroster.csv",
            "description": "10 row(s) have referenced data not found in source. Field - Section SIS ID"
        },
        {
            "type": "Error",
            "fileName": "teacherroster.csv",
            "description": "91 row(s) have referenced data not found in source. Field - SIS ID"
        }
    ]
}
```
