---
title: Tipo de recurso managedAppPolicyDeploymentSummaryPerApp
description: Representa el resumen de implementación de directivas por aplicación.
ms.openlocfilehash: 56b7952049c6ad41ee46f6b77c821aa32b1c4de8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031558"
---
# <a name="managedapppolicydeploymentsummaryperapp-resource-type"></a><span data-ttu-id="3d54e-103">Tipo de recurso managedAppPolicyDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="3d54e-103">managedAppPolicyDeploymentSummaryPerApp resource type</span></span>

> <span data-ttu-id="3d54e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3d54e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3d54e-105">Representa el resumen de implementación de directivas por aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d54e-105">Represents policy deployment summary per app.</span></span>
## <a name="properties"></a><span data-ttu-id="3d54e-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d54e-106">Properties</span></span>
|<span data-ttu-id="3d54e-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3d54e-107">Property</span></span>|<span data-ttu-id="3d54e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d54e-108">Type</span></span>|<span data-ttu-id="3d54e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d54e-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3d54e-110">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="3d54e-110">mobileAppIdentifier</span></span>|[<span data-ttu-id="3d54e-111">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="3d54e-111">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="3d54e-112">Implementación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d54e-112">Deployment of an app.</span></span>|
|<span data-ttu-id="3d54e-113">configurationAppliedUserCount</span><span class="sxs-lookup"><span data-stu-id="3d54e-113">configurationAppliedUserCount</span></span>|<span data-ttu-id="3d54e-114">Int32</span><span class="sxs-lookup"><span data-stu-id="3d54e-114">Int32</span></span>|<span data-ttu-id="3d54e-115">Número de usuarios a los que se aplica la directiva.</span><span class="sxs-lookup"><span data-stu-id="3d54e-115">Number of users the policy is applied.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3d54e-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3d54e-116">Relationships</span></span>
<span data-ttu-id="3d54e-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3d54e-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3d54e-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3d54e-118">JSON Representation</span></span>
<span data-ttu-id="3d54e-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3d54e-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "configurationAppliedUserCount": 1024
}
```



