---
title: Crear un educationSynchronizationProfile
description: 'Crear una solicitud de un nuevo perfil de sincronización de datos de school en el inquilino. Consultar el estado para obtener el estado de los perfiles. '
author: mmast-msft
ms.openlocfilehash: 20c4a7f4dd1512a52bed4a12d1642b8d1138d0e3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345314"
---
# <a name="create-an-educationsynchronizationprofile"></a><span data-ttu-id="80b4c-104">Crear un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="80b4c-104">Create an educationSynchronizationProfile</span></span>

> <span data-ttu-id="80b4c-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="80b4c-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="80b4c-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="80b4c-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="80b4c-107">Crear una solicitud para un nuevo de datos de school [perfil de sincronización](../resources/educationsynchronizationprofile.md) en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="80b4c-107">Create a request for a new school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span> <span data-ttu-id="80b4c-108">[El estado de la consulta](educationsynchronizationprofilestatus-get.md) para obtener el estado de los perfiles.</span><span class="sxs-lookup"><span data-stu-id="80b4c-108">[Query the status](educationsynchronizationprofilestatus-get.md) to get the status of the profile.</span></span> 

## <a name="permissions"></a><span data-ttu-id="80b4c-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="80b4c-109">Permissions</span></span>
<span data-ttu-id="80b4c-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="80b4c-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="80b4c-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="80b4c-112">Permission type</span></span> | <span data-ttu-id="80b4c-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="80b4c-113">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="80b4c-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="80b4c-114">Delegated (work or school account)</span></span> | <span data-ttu-id="80b4c-115">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="80b4c-115">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="80b4c-116">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="80b4c-116">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="80b4c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="80b4c-117">Not supported.</span></span>|
|<span data-ttu-id="80b4c-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="80b4c-118">Application</span></span>|<span data-ttu-id="80b4c-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="80b4c-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="80b4c-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="80b4c-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /synchronizationProfiles
```

## <a name="request-headers"></a><span data-ttu-id="80b4c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="80b4c-121">Request headers</span></span>
| <span data-ttu-id="80b4c-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="80b4c-122">Name</span></span>       | <span data-ttu-id="80b4c-123">Type</span><span class="sxs-lookup"><span data-stu-id="80b4c-123">Type</span></span> | <span data-ttu-id="80b4c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="80b4c-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="80b4c-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="80b4c-125">Authorization</span></span>  | <span data-ttu-id="80b4c-126">string</span><span class="sxs-lookup"><span data-stu-id="80b4c-126">string</span></span>  | <span data-ttu-id="80b4c-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="80b4c-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="80b4c-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="80b4c-129">Content-Type</span></span> | <span data-ttu-id="80b4c-130">string</span><span class="sxs-lookup"><span data-stu-id="80b4c-130">string</span></span> | <span data-ttu-id="80b4c-131">Application/json.</span><span class="sxs-lookup"><span data-stu-id="80b4c-131">Application/json.</span></span> <span data-ttu-id="80b4c-132">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="80b4c-132">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="80b4c-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="80b4c-133">Request body</span></span>
<span data-ttu-id="80b4c-134">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="80b4c-134">In the request body, supply a JSON representation of the [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="80b4c-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80b4c-135">Response</span></span>
<span data-ttu-id="80b4c-136">Si tiene éxito, este método devuelve una `202, Accepted` código de respuesta y un objeto [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80b4c-136">If successful, this method returns a `202, Accepted` response code and an [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="80b4c-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="80b4c-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="80b4c-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="80b4c-138">Request</span></span>
<span data-ttu-id="80b4c-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80b4c-139">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "create_educationSynchronizationProfile"
}-->
```http
POST https://graph.microsoft.com/beta/education/synchronizationProfiles
Content-type: application/json

{
    "displayName": "Test Profile",
    "dataProvider": {
        "@odata.type": "#microsoft.graph.educationcsvdataprovider",
        "customizations": {
            "student": {
                "optionalPropertiesToSync": [
                    "State ID",
                    "Middle Name"
                ]
            }
        }
    },
    "identitySynchronizationConfiguration": {
        "@odata.type": "#microsoft.graph.educationidentitycreationconfiguration",
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
    "licensesToAssign": [
        {
            "appliesTo": "teacher",
            "skuIds": [
                "6fd2c87f-b296-42f0-b197-1e91e994b900"
            ]
        },
        {
            "appliesTo": "student",
            "skuIds": [
                "6fd2c87f-b296-42f0-b197-1e91e994b900"
            ]
        }
    ]
}
```

##### <a name="response"></a><span data-ttu-id="80b4c-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80b4c-140">Response</span></span>
<span data-ttu-id="80b4c-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80b4c-141">The following is an example of the response.</span></span> 

><span data-ttu-id="80b4c-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="80b4c-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "#microsoft.graph.educationSynchronizationProfile",
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "displayName": "Test Profile",
    "state": "provisioning",
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
    "licensesToAssign": [
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