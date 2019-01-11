---
title: Lista secureScores
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 6bf0a1e1964c93043bad4a81ab812786627ea737
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831818"
---
# <a name="list-securescores"></a><span data-ttu-id="1cd90-104">Lista secureScores</span><span class="sxs-lookup"><span data-stu-id="1cd90-104">List secureScores</span></span>

 > <span data-ttu-id="1cd90-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1cd90-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1cd90-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1cd90-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1cd90-107">Recuperar las propiedades y relaciones de un objeto [secureScores](../resources/securescores.md) .</span><span class="sxs-lookup"><span data-stu-id="1cd90-107">Retrieve the properties and relationships of a [secureScores](../resources/securescores.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="1cd90-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="1cd90-108">Permissions</span></span>

<span data-ttu-id="1cd90-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1cd90-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1cd90-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1cd90-111">Permission type</span></span>      | <span data-ttu-id="1cd90-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1cd90-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1cd90-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1cd90-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="1cd90-114">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="1cd90-114">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All.</span></span>   |
|<span data-ttu-id="1cd90-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1cd90-115">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="1cd90-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1cd90-116">Not supported.</span></span>  |
|<span data-ttu-id="1cd90-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1cd90-117">Application</span></span> | <span data-ttu-id="1cd90-118">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="1cd90-118">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1cd90-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1cd90-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /security/secureScores
```

## <a name="request-headers"></a><span data-ttu-id="1cd90-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1cd90-120">Request headers</span></span>

| <span data-ttu-id="1cd90-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="1cd90-121">Name</span></span>      |<span data-ttu-id="1cd90-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cd90-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="1cd90-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1cd90-123">Authorization</span></span>  | <span data-ttu-id="1cd90-p104">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="1cd90-p104">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1cd90-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1cd90-126">Request body</span></span>

<span data-ttu-id="1cd90-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1cd90-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1cd90-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1cd90-128">Response</span></span>

<span data-ttu-id="1cd90-129">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **secureScores** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1cd90-129">If successful, this method returns a `200 OK` response code and a **secureScores** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1cd90-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1cd90-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="1cd90-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1cd90-131">Request</span></span>

<span data-ttu-id="1cd90-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1cd90-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "securescores_list"
}-->

```http
GET https://graph.microsoft.com/beta/security/secureScores?$top=1
```

### <a name="response"></a><span data-ttu-id="1cd90-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1cd90-133">Response</span></span>

<span data-ttu-id="1cd90-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1cd90-134">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.secureScores"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json


{
    "value": [
        {
            "activeUserCount": "activeUserCount.value",
            "createdDateTime": "createdDateTime.value",
            "currentScore": "currentScore.value",
            "enabledServices": "enabledServices.value",
            "licensedUserCount": "licensedUserCount.value",
            "maxScore": "maxScore.value",
            "id": "id.value",
            "azureTenantId": "azureTenantId.value",
            "averageComparativeScores": [
                {
                    "basis": "AllTenants",
                    "averageScore": "averageScore.value",
                    "deviceScore": "deviceScore.value",
                    "dataScore": "dataScore.value",
                    "identityScore": "identityScore.value"
                },
                {
                    "basis": "TotalSeats",
                    "averageScore": "averageScore.value",
                    "deviceScore": "deviceScore.value",
                    "dataScore": "dataScore.value",
                    "identityScore": "identityScore.value",
                    "seatSizeRangeUpperValue": "seatSizeRangeUpperValue.value",
                    "categoryValue": "categoryValue.value",
                    "seatSizeRangeLowerValue": "seatSizeRangeLowerValue.value"
                },
                {
                    "basis": "IndustryTypes",
                    "averageScore": "averageScore.value",
                    "deviceScore": "deviceScore.value",
                    "dataScore": "dataScore.value",
                    "identityScore": "identityScore.value",
                    "categoryValue": "categoryValue.value"
                }
            ],
            "controlScores": [
                {
                    "controlCategory": "controlCategory.value",
                    "controlName": "controlName.value",
                    "description": "description.value",
                    "score": "score.value",
                    "total": "total.value",
                    "count": "count.value"
                }
            ]
        }
    ]            
}

```


<!-- {
  "type": "#page.annotation",
  "description": "List secureScores",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
