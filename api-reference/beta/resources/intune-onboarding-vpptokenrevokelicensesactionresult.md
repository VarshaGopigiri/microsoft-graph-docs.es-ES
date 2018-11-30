---
title: tipo de recurso vppTokenRevokeLicensesActionResult
description: El estado de la acción de licencias revoke se realiza en el símbolo (token) de programa de compra de volumen de Apple.
ms.openlocfilehash: 89baf69ba89ac11c52b8e05b35f38aca422cc1b2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086518"
---
# <a name="vpptokenrevokelicensesactionresult-resource-type"></a><span data-ttu-id="50dae-103">tipo de recurso vppTokenRevokeLicensesActionResult</span><span class="sxs-lookup"><span data-stu-id="50dae-103">vppTokenRevokeLicensesActionResult resource type</span></span>

> <span data-ttu-id="50dae-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="50dae-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="50dae-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="50dae-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="50dae-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="50dae-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="50dae-107">El estado de la acción de licencias revoke se realiza en el símbolo (token) de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="50dae-107">The status of the revoke licenses action performed on the Apple Volume Purchase Program token.</span></span>

<span data-ttu-id="50dae-108">Hereda de [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="50dae-108">Inherits from [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="50dae-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50dae-109">Properties</span></span>
|<span data-ttu-id="50dae-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50dae-110">Property</span></span>|<span data-ttu-id="50dae-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="50dae-111">Type</span></span>|<span data-ttu-id="50dae-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="50dae-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="50dae-113">actionName</span><span class="sxs-lookup"><span data-stu-id="50dae-113">actionName</span></span>|<span data-ttu-id="50dae-114">String</span><span class="sxs-lookup"><span data-stu-id="50dae-114">String</span></span>|<span data-ttu-id="50dae-115">Nombre de la acción Inherited desde [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="50dae-115">Action name Inherited from [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)</span></span>|
|<span data-ttu-id="50dae-116">actionState</span><span class="sxs-lookup"><span data-stu-id="50dae-116">actionState</span></span>|[<span data-ttu-id="50dae-117">actionState</span><span class="sxs-lookup"><span data-stu-id="50dae-117">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="50dae-118">Estado de la acción Inherited desde [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="50dae-118">State of the action Inherited from [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md).</span></span> <span data-ttu-id="50dae-119">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="50dae-119">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="50dae-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="50dae-120">startDateTime</span></span>|<span data-ttu-id="50dae-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="50dae-121">DateTimeOffset</span></span>|<span data-ttu-id="50dae-122">Tiempo que se inició la acción se hereda de [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="50dae-122">Time the action was initiated Inherited from [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)</span></span>|
|<span data-ttu-id="50dae-123">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="50dae-123">lastUpdatedDateTime</span></span>|<span data-ttu-id="50dae-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="50dae-124">DateTimeOffset</span></span>|<span data-ttu-id="50dae-125">Tiempo por última vez el estado de acción actualizó Inherited desde [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="50dae-125">Time the action state was last updated Inherited from [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)</span></span>|
|<span data-ttu-id="50dae-126">totalLicensesCount</span><span class="sxs-lookup"><span data-stu-id="50dae-126">totalLicensesCount</span></span>|<span data-ttu-id="50dae-127">Int32</span><span class="sxs-lookup"><span data-stu-id="50dae-127">Int32</span></span>|<span data-ttu-id="50dae-128">Un recuento del número de licencias que se han intentado se va a revocar.</span><span class="sxs-lookup"><span data-stu-id="50dae-128">A count of the number of licenses that were attempted to revoke.</span></span>|
|<span data-ttu-id="50dae-129">failedLicensesCount</span><span class="sxs-lookup"><span data-stu-id="50dae-129">failedLicensesCount</span></span>|<span data-ttu-id="50dae-130">Int32</span><span class="sxs-lookup"><span data-stu-id="50dae-130">Int32</span></span>|<span data-ttu-id="50dae-131">Un recuento del número de licencias que no se pudo revocar.</span><span class="sxs-lookup"><span data-stu-id="50dae-131">A count of the number of licenses that failed to revoke.</span></span>|
|<span data-ttu-id="50dae-132">actionFailureReason</span><span class="sxs-lookup"><span data-stu-id="50dae-132">actionFailureReason</span></span>|[<span data-ttu-id="50dae-133">vppTokenActionFailureReason</span><span class="sxs-lookup"><span data-stu-id="50dae-133">vppTokenActionFailureReason</span></span>](../resources/intune-shared-vpptokenactionfailurereason.md)|<span data-ttu-id="50dae-134">El motivo del error de acción de licencias revoke.</span><span class="sxs-lookup"><span data-stu-id="50dae-134">The reason for the revoke licenses action failure.</span></span> <span data-ttu-id="50dae-135">Los valores posibles son: `none`, `appleFailure`, `internalError`, `expiredVppToken` y `expiredApplePushNotificationCertificate`.</span><span class="sxs-lookup"><span data-stu-id="50dae-135">Possible values are: `none`, `appleFailure`, `internalError`, `expiredVppToken`, `expiredApplePushNotificationCertificate`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="50dae-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="50dae-136">Relationships</span></span>
<span data-ttu-id="50dae-137">Ninguna</span><span class="sxs-lookup"><span data-stu-id="50dae-137">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="50dae-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="50dae-138">JSON Representation</span></span>
<span data-ttu-id="50dae-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="50dae-139">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vppTokenRevokeLicensesActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vppTokenRevokeLicensesActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "totalLicensesCount": 1024,
  "failedLicensesCount": 1024,
  "actionFailureReason": "String"
}
```





