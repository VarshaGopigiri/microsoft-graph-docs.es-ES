---
title: Obtener educationSynchronizationErrors
description: 'Obtenga los errores generados durante la validación o durante una sincronización de un perfil de sincronización de datos de school específicos en el inquilino. '
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 1b0504ae8ef7c463afb4041a89bfb4229833b63e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854008"
---
# <a name="get-educationsynchronizationerrors"></a><span data-ttu-id="3cf7e-103">Obtener educationSynchronizationErrors</span><span class="sxs-lookup"><span data-stu-id="3cf7e-103">Get educationSynchronizationErrors</span></span>

<span data-ttu-id="3cf7e-104">Obtenga los errores generados durante la validación o durante una sincronización de escuela específico datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino.</span><span class="sxs-lookup"><span data-stu-id="3cf7e-104">Get the errors generated during validation and/or during a sync of a specific school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span> 

## <a name="permissions"></a><span data-ttu-id="3cf7e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3cf7e-105">Permissions</span></span>
<span data-ttu-id="3cf7e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3cf7e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="3cf7e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3cf7e-108">Permission type</span></span> | <span data-ttu-id="3cf7e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3cf7e-109">Permissions (from least to most privileged)</span></span> |
|:-----------|:------|
| <span data-ttu-id="3cf7e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3cf7e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="3cf7e-111">EduAdministration.Read, EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3cf7e-111">EduAdministration.Read, EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="3cf7e-112">Delegado (cuenta Microsoft personal</span><span class="sxs-lookup"><span data-stu-id="3cf7e-112">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="3cf7e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3cf7e-113">Not supported.</span></span>|
|<span data-ttu-id="3cf7e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3cf7e-114">Application</span></span>| <span data-ttu-id="3cf7e-115">EduAdministration.Read.All, EduAdministration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3cf7e-115">EduAdministration.Read.All, EduAdministration.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3cf7e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3cf7e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /synchronizationProfiles/{id}/errors
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3cf7e-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3cf7e-117">Optional query parameters</span></span>
<span data-ttu-id="3cf7e-118">Este método admite los siguientes [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta: $filter, $orderby, $top, $skip y $count.</span><span class="sxs-lookup"><span data-stu-id="3cf7e-118">This method supports the following [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response: $filter, $orderby, $top, $skip, and $count.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3cf7e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3cf7e-119">Request headers</span></span>
| <span data-ttu-id="3cf7e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3cf7e-120">Name</span></span>       | <span data-ttu-id="3cf7e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="3cf7e-121">Type</span></span> | <span data-ttu-id="3cf7e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cf7e-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="3cf7e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3cf7e-123">Authorization</span></span>  | <span data-ttu-id="3cf7e-124">string</span><span class="sxs-lookup"><span data-stu-id="3cf7e-124">string</span></span>  | <span data-ttu-id="3cf7e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3cf7e-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3cf7e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3cf7e-127">Request body</span></span>
<span data-ttu-id="3cf7e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3cf7e-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="3cf7e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3cf7e-129">Response</span></span>
<span data-ttu-id="3cf7e-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [error de sincronización](../resources/educationsynchronizationerror.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3cf7e-130">If successful, this method returns a `200 OK` response code and a collection of [synchronization error](../resources/educationsynchronizationerror.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3cf7e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3cf7e-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3cf7e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3cf7e-132">Request</span></span>
<span data-ttu-id="3cf7e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3cf7e-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationSynchronizationProfile_error"
}-->
```http
GET https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/errors
```

##### <a name="response"></a><span data-ttu-id="3cf7e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3cf7e-134">Response</span></span>
<span data-ttu-id="3cf7e-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3cf7e-135">The following is an example of the response.</span></span> 

><span data-ttu-id="3cf7e-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3cf7e-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "@odata.type": "#microsoft.graph.educationSynchronizationError",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1568

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/synchronizationProfiles('{id}')/errors",
    "@odata.count": 14,
    "value": [
        {
            "entryType": "Student",
            "errorCode": "UnsynchronizableChange",
            "errorMessage": "Student cannot be updated as no matching entry in Active Directory was found for Student.  Verify the identity matching criteria for the profile.",
            "joiningValue": "richard.2wilson@testschool.edu",
            "recordedDateTime": "2017-07-05T00:52:45Z",
            "reportableIdentifier": "richard.2wilson"
        },
        {
            "entryType": "Teacher",
            "errorCode": "UnsynchronizableChange",
            "errorMessage": "Teacher cannot be updated as no matching entry in Active Directory was found for Teacher.  Verify the identity matching criteria for the profile.",
            "joiningValue": "alberto2.dorsey@testschool.edu",
            "recordedDateTime": "2017-07-05T00:52:57Z",
            "reportableIdentifier": "alberto2.dorsey"
        },
        {
            "entryType": "Teacher",
            "errorCode": "UnsynchronizableChange",
            "errorMessage": "Teacher cannot be updated as no matching entry in Active Directory was found for Teacher.  Verify the identity matching criteria for the profile.",
            "joiningValue": "madeline2.bullock@testschool.edu",
            "recordedDateTime": "2017-07-05T00:52:57Z",
            "reportableIdentifier": "madeline2.bullock"
        }
    ]
}
```
