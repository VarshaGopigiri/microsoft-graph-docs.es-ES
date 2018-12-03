---
title: Obtener un educationSynchronizationProfile
description: Recuperar un perfil de sincronización de datos de school en el inquilino según el identificador.
ms.openlocfilehash: a62b938f3177f06a02a8a5ad1190d72b3f27dfd9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083016"
---
# <a name="get-an-educationsynchronizationprofile"></a><span data-ttu-id="98298-103">Obtener un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="98298-103">Get an educationSynchronizationProfile</span></span>

> <span data-ttu-id="98298-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="98298-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="98298-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="98298-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="98298-106">Recuperar school datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino según el identificador.</span><span class="sxs-lookup"><span data-stu-id="98298-106">Retrieve a school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant based on the identifier.</span></span>

## <a name="permissions"></a><span data-ttu-id="98298-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="98298-107">Permissions</span></span>
<span data-ttu-id="98298-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="98298-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="98298-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98298-110">Permission type</span></span> | <span data-ttu-id="98298-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98298-111">Permissions (from least to most privileged)</span></span> |
|:-----------|:----------|
| <span data-ttu-id="98298-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98298-112">Delegated (work or school account)</span></span> | <span data-ttu-id="98298-113">EduAdministration.Read, EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="98298-113">EduAdministration.Read, EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="98298-114">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="98298-114">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="98298-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98298-115">Not supported.</span></span>|
|<span data-ttu-id="98298-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98298-116">Application</span></span>| <span data-ttu-id="98298-117">EduAdministration.Read.All, EduAdministration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98298-117">EduAdministration.Read.All, EduAdministration.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="98298-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98298-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /synchronizationProfiles/{id}
```

## <a name="request-headers"></a><span data-ttu-id="98298-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98298-119">Request headers</span></span>
| <span data-ttu-id="98298-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="98298-120">Name</span></span>       | <span data-ttu-id="98298-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="98298-121">Type</span></span> | <span data-ttu-id="98298-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="98298-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="98298-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="98298-123">Authorization</span></span>  | <span data-ttu-id="98298-124">string</span><span class="sxs-lookup"><span data-stu-id="98298-124">string</span></span>  | <span data-ttu-id="98298-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98298-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="98298-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98298-127">Request body</span></span>
<span data-ttu-id="98298-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="98298-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="98298-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98298-129">Response</span></span>
<span data-ttu-id="98298-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98298-130">If successful, this method returns a `200 OK` response code and an [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="98298-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98298-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="98298-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98298-132">Request</span></span>
<span data-ttu-id="98298-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98298-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_educationSynchronizationProfile"
}-->
```http
GET https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}
```

##### <a name="response"></a><span data-ttu-id="98298-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98298-134">Response</span></span>
<span data-ttu-id="98298-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98298-135">The following is an example of the response.</span></span> 

><span data-ttu-id="98298-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98298-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "#microsoft.graph.educationSynchronizationProfile",
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 2487

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/synchronizationProfiles/$entity",
    "displayName": "Test Profile",
    "state": "provisioned",
    "id": "86904b1e-c7d0-4ead-b13a-98f11fc400ee",
    "dataProvider": {
        "@odata.type": "#microsoft.graph.educationCsvDataProvider",
        "customizations": {
            "student": {
                "optionalPropertiesToSync": [
                    "State ID",
                    "Middle Name"
                ],
                "synchronizationStartDate": "0001-01-01T00:00:00Z",
                "isSyncDeferred": false,
                "allowDisplayNameUpdate": false
            },
            "teacher": {
                "optionalPropertiesToSync": [
                    "State ID",
                    "Teacher Number",
                    "Status",
                    "Middle Name",
                    "Secondary Email",
                    "Title",
                    "Qualification"
                ],
                "synchronizationStartDate": "0001-01-01T00:00:00Z",
                "isSyncDeferred": false,
                "allowDisplayNameUpdate": false
            },
            "studentEnrollment": {
                "optionalPropertiesToSync": [],
                "synchronizationStartDate": "0001-01-01T00:00:00Z",
                "isSyncDeferred": false,
                "allowDisplayNameUpdate": false
            },
            "teacherRoster": {
                "optionalPropertiesToSync": [],
                "synchronizationStartDate": "0001-01-01T00:00:00Z",
                "isSyncDeferred": false,
                "allowDisplayNameUpdate": false
            }
        }
    },
    "identitySynchronizationConfiguration": {
        "@odata.type": "#microsoft.graph.educationIdentityCreationConfiguration",
        "userDomains": [
            {
                "appliesTo": "student",
                "name": "testschool.edu"
            },
            {
                "appliesTo": "teacher",
                "name": "testschool.edu"
            }
        ]
    },
    "licensesToAssign": 
         [
            {
                "@odata.type": "#microsoft.graph.educationSynchronizationLicenseAssignment",
                "appliesTo": "teacher",
                "skuIds": [
                    "6fd2c87f-b296-42f0-b197-1e91e994b900"
                ]
            },
            {
                "@odata.type": "#microsoft.graph.educationSynchronizationLicenseAssignment",
                "appliesTo": "student",
                "skuIds": [
                    "6fd2c87f-b296-42f0-b197-1e91e994b900"
                ]
            }
        ]
}
```