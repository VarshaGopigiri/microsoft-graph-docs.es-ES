---
title: Crear un educationSynchronizationProfile
description: 'Crear una solicitud de un nuevo perfil de sincronización de datos de school en el inquilino. Consultar el estado para obtener el estado de los perfiles. '
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: c5ce12f43af4e32691c34038a9a0c0527d314c06
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853854"
---
# <a name="create-an-educationsynchronizationprofile"></a><span data-ttu-id="f46bf-104">Crear un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="f46bf-104">Create an educationSynchronizationProfile</span></span>

> <span data-ttu-id="f46bf-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f46bf-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f46bf-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f46bf-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f46bf-107">Crear una solicitud para un nuevo de datos de school [perfil de sincronización](../resources/educationsynchronizationprofile.md) en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="f46bf-107">Create a request for a new school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span> <span data-ttu-id="f46bf-108">[El estado de la consulta](educationsynchronizationprofilestatus-get.md) para obtener el estado de los perfiles.</span><span class="sxs-lookup"><span data-stu-id="f46bf-108">[Query the status](educationsynchronizationprofilestatus-get.md) to get the status of the profile.</span></span> 

## <a name="permissions"></a><span data-ttu-id="f46bf-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="f46bf-109">Permissions</span></span>
<span data-ttu-id="f46bf-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f46bf-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f46bf-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f46bf-112">Permission type</span></span> | <span data-ttu-id="f46bf-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="f46bf-113">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="f46bf-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f46bf-114">Delegated (work or school account)</span></span> | <span data-ttu-id="f46bf-115">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f46bf-115">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="f46bf-116">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="f46bf-116">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="f46bf-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f46bf-117">Not supported.</span></span>|
|<span data-ttu-id="f46bf-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f46bf-118">Application</span></span>|<span data-ttu-id="f46bf-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f46bf-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f46bf-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f46bf-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /synchronizationProfiles
```

## <a name="request-headers"></a><span data-ttu-id="f46bf-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f46bf-121">Request headers</span></span>
| <span data-ttu-id="f46bf-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="f46bf-122">Name</span></span>       | <span data-ttu-id="f46bf-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="f46bf-123">Type</span></span> | <span data-ttu-id="f46bf-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f46bf-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="f46bf-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="f46bf-125">Authorization</span></span>  | <span data-ttu-id="f46bf-126">string</span><span class="sxs-lookup"><span data-stu-id="f46bf-126">string</span></span>  | <span data-ttu-id="f46bf-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f46bf-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="f46bf-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f46bf-129">Content-Type</span></span> | <span data-ttu-id="f46bf-130">string</span><span class="sxs-lookup"><span data-stu-id="f46bf-130">string</span></span> | <span data-ttu-id="f46bf-131">Application/json.</span><span class="sxs-lookup"><span data-stu-id="f46bf-131">Application/json.</span></span> <span data-ttu-id="f46bf-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="f46bf-132">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f46bf-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f46bf-133">Request body</span></span>
<span data-ttu-id="f46bf-134">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f46bf-134">In the request body, supply a JSON representation of the [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="f46bf-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f46bf-135">Response</span></span>
<span data-ttu-id="f46bf-136">Si tiene éxito, este método devuelve una `202, Accepted` código de respuesta y un objeto [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f46bf-136">If successful, this method returns a `202, Accepted` response code and an [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f46bf-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f46bf-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f46bf-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f46bf-138">Request</span></span>
<span data-ttu-id="f46bf-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f46bf-139">The following is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="f46bf-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f46bf-140">Response</span></span>
<span data-ttu-id="f46bf-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f46bf-141">The following is an example of the response.</span></span> 

><span data-ttu-id="f46bf-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f46bf-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
