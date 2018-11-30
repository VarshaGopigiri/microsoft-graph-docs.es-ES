---
title: Actualizar un educationSynchronizationProfile
description: Actualizar las propiedades de un perfil de sincronización de datos de escuela existente en el inquilino.
ms.openlocfilehash: 9f670a04dfb3c5465683883eeaf4eeed543e830a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086202"
---
# <a name="update-an-educationsynchronizationprofile"></a><span data-ttu-id="fc26a-103">Actualizar un educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="fc26a-103">Update an educationSynchronizationProfile</span></span>

> <span data-ttu-id="fc26a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fc26a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fc26a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fc26a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fc26a-106">Actualizar las propiedades de una existente de datos school [perfil de sincronización](../resources/educationsynchronizationprofile.md) en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="fc26a-106">Update properties for an existing school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="fc26a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="fc26a-107">Permissions</span></span>
<span data-ttu-id="fc26a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc26a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="fc26a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc26a-110">Permission type</span></span> | <span data-ttu-id="fc26a-111">Permissions</span><span class="sxs-lookup"><span data-stu-id="fc26a-111">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="fc26a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc26a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="fc26a-113">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fc26a-113">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="fc26a-114">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="fc26a-114">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="fc26a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc26a-115">Not supported.</span></span>|
|<span data-ttu-id="fc26a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc26a-116">Application</span></span>|<span data-ttu-id="fc26a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc26a-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fc26a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc26a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /synchronizationProfiles
```

## <a name="request-headers"></a><span data-ttu-id="fc26a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc26a-119">Request headers</span></span>
| <span data-ttu-id="fc26a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc26a-120">Name</span></span>       | <span data-ttu-id="fc26a-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc26a-121">Type</span></span> | <span data-ttu-id="fc26a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc26a-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="fc26a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="fc26a-123">Authorization</span></span>  | <span data-ttu-id="fc26a-124">string</span><span class="sxs-lookup"><span data-stu-id="fc26a-124">string</span></span>  | <span data-ttu-id="fc26a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fc26a-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="fc26a-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fc26a-127">Content-Type</span></span> | <span data-ttu-id="fc26a-128">string</span><span class="sxs-lookup"><span data-stu-id="fc26a-128">string</span></span> | <span data-ttu-id="fc26a-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fc26a-p104">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fc26a-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc26a-131">Request body</span></span>
<span data-ttu-id="fc26a-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [synchronizationProfile](../resources/educationsynchronizationprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="fc26a-132">In the request body, supply a JSON representation of the [synchronizationProfile](../resources/educationsynchronizationprofile.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="fc26a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc26a-133">Response</span></span>
<span data-ttu-id="fc26a-134">Si tiene éxito, este método devuelve una `202, Accepted` código de respuesta y un objeto [synchronizationProfile](../resources/educationsynchronizationprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc26a-134">If successful, this method returns a `202, Accepted` response code and a [synchronizationProfile](../resources/educationsynchronizationprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fc26a-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc26a-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fc26a-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc26a-136">Request</span></span>
<span data-ttu-id="fc26a-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc26a-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "update_synchronizationProfile"
}-->
```http
PUT https://graph.microsoft.com/beta/education/synchronizationProfiles
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

##### <a name="response"></a><span data-ttu-id="fc26a-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc26a-138">Response</span></span>
<span data-ttu-id="fc26a-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc26a-139">Here is an example of the response.</span></span> 

><span data-ttu-id="fc26a-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc26a-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "#microsoft.graph.educationSynchronizationProfile",
} -->
```http
HTTP/1.1 202 Accepted
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