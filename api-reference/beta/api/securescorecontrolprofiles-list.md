---
title: Lista secureScoreControlProfiles
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 33d0f6059d66350c9fa763097277f83c041e96ee
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086336"
---
# <a name="list-securescorecontrolprofiles"></a><span data-ttu-id="bd62a-104">Lista secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="bd62a-104">List secureScoreControlProfiles</span></span>

 > <span data-ttu-id="bd62a-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bd62a-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bd62a-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bd62a-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bd62a-107">Recuperar las propiedades y relaciones de un objeto [secureScoreControlProfiles](../resources/securescorecontrolprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="bd62a-107">Retrieve the properties and relationships of a [secureScoreControlProfiles](../resources/securescorecontrolprofiles.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="bd62a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="bd62a-108">Permissions</span></span>

<span data-ttu-id="bd62a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bd62a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bd62a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd62a-111">Permission type</span></span>      | <span data-ttu-id="bd62a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd62a-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bd62a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd62a-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="bd62a-114">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="bd62a-114">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All.</span></span>   |
|<span data-ttu-id="bd62a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd62a-115">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="bd62a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd62a-116">Not supported.</span></span>  |
|<span data-ttu-id="bd62a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd62a-117">Application</span></span> | <span data-ttu-id="bd62a-118">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="bd62a-118">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bd62a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd62a-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /security/secureScoreControlProfiles
```

## <a name="request-headers"></a><span data-ttu-id="bd62a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd62a-120">Request headers</span></span>

| <span data-ttu-id="bd62a-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd62a-121">Name</span></span>      |<span data-ttu-id="bd62a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd62a-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="bd62a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bd62a-123">Authorization</span></span>  | <span data-ttu-id="bd62a-p104">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="bd62a-p104">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="bd62a-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bd62a-126">Request body</span></span>

<span data-ttu-id="bd62a-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bd62a-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bd62a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd62a-128">Response</span></span>

<span data-ttu-id="bd62a-129">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **secureScoreControlProfiles** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd62a-129">If successful, this method returns a `200 OK` response code and a **secureScoreControlProfiles** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bd62a-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd62a-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="bd62a-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd62a-131">Request</span></span>

<span data-ttu-id="bd62a-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd62a-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "securescorecontrolprofiles_list"
}-->

```http
GET https://graph.microsoft.com/beta/security/secureScoreControlProfiles
```

### <a name="response"></a><span data-ttu-id="bd62a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd62a-133">Response</span></span>

<span data-ttu-id="bd62a-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd62a-134">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.secureScoreControlProfiles"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json


{
    "value": [
        {
            "actionType": "actionType.value",
            "actionUrl": "actionUrl.value",
            "controlCategory": "controlCategory.value",
            "title": "title.value",
            "deprecated": "deprecated.value",
            "implementationCost": "implementationCost.value",
            "lastModifiedDateTime": "lastModifiedDateTime.value",
            "maxScore": "maxScore.value",
            "rank": "rank.value",
            "remediation": "remediation.value",
            "remediationImpact": "remediationImpact.value",
            "service": "service.value",
            "threats": [
                "threats.value"
            ],
            "tier": "tier.value",
            "userImpact": "userImpact.value",
            "id": "id.value",
            "azureTenantId": "azureTenantId.value",
            "controlStateUpdates": [
                {
                    "assignedTo": "assignedTo.value",
                    "comment": "comment.value",
                    "state": "state.value",
                    "updatedBy": "updatedBy.value",
                    "updatedDateTime": "updatedDateTime.value"
                }
            ],
            "vendorInformation": {
                "provider": "SecureScore",
                "providerVersion": null,
                "subProvider": null,
                "vendor": "Microsoft"
            }
         }
     ]
}
```


<!-- {
  "type": "#page.annotation",
  "description": "List secureScoreControlProfiles",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
