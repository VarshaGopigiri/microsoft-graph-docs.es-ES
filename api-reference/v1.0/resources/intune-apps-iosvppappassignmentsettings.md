---
title: Tipo de recurso iosVppAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4c9a5196be760204af682c1a7318318920284a40
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886117"
---
# <a name="iosvppappassignmentsettings-resource-type"></a><span data-ttu-id="301f2-103">Tipo de recurso iosVppAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="301f2-103">iosVppAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="301f2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="301f2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="301f2-105">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.</span><span class="sxs-lookup"><span data-stu-id="301f2-105">Contains properties used to assign an iOS VPP mobile app to a group.</span></span>

<span data-ttu-id="301f2-106">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="301f2-106">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="301f2-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="301f2-107">Properties</span></span>
|<span data-ttu-id="301f2-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="301f2-108">Property</span></span>|<span data-ttu-id="301f2-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="301f2-109">Type</span></span>|<span data-ttu-id="301f2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="301f2-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="301f2-111">useDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="301f2-111">useDeviceLicensing</span></span>|<span data-ttu-id="301f2-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="301f2-112">Boolean</span></span>|<span data-ttu-id="301f2-113">Si se deben usar o no las licencias de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="301f2-113">Whether or not to use device licensing.</span></span>|
|<span data-ttu-id="301f2-114">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="301f2-114">vpnConfigurationId</span></span>|<span data-ttu-id="301f2-115">cadena</span><span class="sxs-lookup"><span data-stu-id="301f2-115">String</span></span>|<span data-ttu-id="301f2-116">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="301f2-116">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="301f2-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="301f2-117">Relationships</span></span>
<span data-ttu-id="301f2-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="301f2-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="301f2-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="301f2-119">JSON Representation</span></span>
<span data-ttu-id="301f2-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="301f2-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosVppAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppAppAssignmentSettings",
  "useDeviceLicensing": true,
  "vpnConfigurationId": "String"
}
```



