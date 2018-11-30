---
title: Lista educationSynchronizationProfiles
description: Recupere la colección de perfiles de sincronización de datos de school en el inquilino.
ms.openlocfilehash: a303178a930f207aa92e7a49c769afbc06a7e1e0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084004"
---
# <a name="list-educationsynchronizationprofiles"></a><span data-ttu-id="b562c-103">Lista educationSynchronizationProfiles</span><span class="sxs-lookup"><span data-stu-id="b562c-103">List educationSynchronizationProfiles</span></span>

> <span data-ttu-id="b562c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b562c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b562c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b562c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b562c-106">Recupere la colección school datos de [perfiles de sincronización](../resources/educationsynchronizationprofile.md) en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="b562c-106">Retrieve the collection of school data [synchronization profiles](../resources/educationsynchronizationprofile.md) in the tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="b562c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b562c-107">Permissions</span></span>
<span data-ttu-id="b562c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b562c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b562c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b562c-110">Permission type</span></span> | <span data-ttu-id="b562c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b562c-111">Permissions (from least to most privileged)</span></span> |
|:-----------|:----------|
| <span data-ttu-id="b562c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b562c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b562c-113">EduAdministration.Read, EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b562c-113">EduAdministration.Read, EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="b562c-114">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="b562c-114">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="b562c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b562c-115">Not supported.</span></span>|
|<span data-ttu-id="b562c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b562c-116">Application</span></span>|<span data-ttu-id="b562c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b562c-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b562c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b562c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /synchronizationProfiles
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b562c-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b562c-119">Optional query parameters</span></span>
<span data-ttu-id="b562c-120">Este método admite los siguientes [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta: $filter, $orderby, $top, $skip y $count.</span><span class="sxs-lookup"><span data-stu-id="b562c-120">This method supports the following [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response: $filter, $orderby, $top, $skip, and $count.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b562c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b562c-121">Request headers</span></span>
| <span data-ttu-id="b562c-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b562c-122">Name</span></span>       | <span data-ttu-id="b562c-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="b562c-123">Type</span></span> | <span data-ttu-id="b562c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b562c-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b562c-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="b562c-125">Authorization</span></span>  | <span data-ttu-id="b562c-126">string</span><span class="sxs-lookup"><span data-stu-id="b562c-126">string</span></span>  | <span data-ttu-id="b562c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b562c-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b562c-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b562c-129">Request body</span></span>
<span data-ttu-id="b562c-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b562c-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="b562c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b562c-131">Response</span></span>
<span data-ttu-id="b562c-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b562c-132">If successful, this method returns a `200 OK` response code and a collection of [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b562c-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b562c-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b562c-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b562c-134">Request</span></span>
<span data-ttu-id="b562c-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b562c-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "list_synchronizationProfile"
}-->
```http
GET https://graph.microsoft.com/beta/education/synchronizationProfiles
```

##### <a name="response"></a><span data-ttu-id="b562c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b562c-136">Response</span></span>
<span data-ttu-id="b562c-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b562c-137">The following is an example of the response.</span></span> 

><span data-ttu-id="b562c-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b562c-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "#microsoft.graph.educationSynchronizationProfile",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 3296

{
    "value": [
    {
        "displayName": "Test Profile",
        "state": "provisioned",
        "id": "15e9b9fa-de85-492e-aa44-550c40de626e",
        "dataProvider": {
            "@odata.type": "#microsoft.graph.educationCsvDataProvider",
            "customizations": {
                "school": {
                    "optionalPropertiesToSync": [
                        "School NCES_ID",
                        "State ID",
                        "GradeLow",
                        "GradeHigh",
                        "Principal Name"
                    ],
                    "synchronizationStartDate": "0001-01-01T00:00:00Z",
                    "isSyncDeferred": false,
                    "allowDisplayNameUpdate": false
                },
                "section": {
                    "optionalPropertiesToSync": [],
                    "synchronizationStartDate": "0001-01-01T00:00:00Z",
                    "isSyncDeferred": false,
                    "allowDisplayNameUpdate": false
                },
                "student": {
                    "optionalPropertiesToSync": [
                        "State ID",
                        "Email",
                        "Middle Name"
                    ],
                    "synchronizationStartDate": "0001-01-01T00:00:00Z",
                    "isSyncDeferred": false,
                    "allowDisplayNameUpdate": false
                },
                "teacher": {
                    "optionalPropertiesToSync": [
                        "Teacher Number",
                        "Middle Name"
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
  ]
}
```