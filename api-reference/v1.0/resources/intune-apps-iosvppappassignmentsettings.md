---
title: Tipo de recurso iosVppAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e221ceb67789f9d96195a31bd7eba8f37a9df6bc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917648"
---
# <a name="iosvppappassignmentsettings-resource-type"></a><span data-ttu-id="3c519-103">Tipo de recurso iosVppAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="3c519-103">iosVppAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="3c519-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3c519-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3c519-105">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.</span><span class="sxs-lookup"><span data-stu-id="3c519-105">Contains properties used to assign an iOS VPP mobile app to a group.</span></span>

<span data-ttu-id="3c519-106">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="3c519-106">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="3c519-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c519-107">Properties</span></span>
|<span data-ttu-id="3c519-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3c519-108">Property</span></span>|<span data-ttu-id="3c519-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c519-109">Type</span></span>|<span data-ttu-id="3c519-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c519-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3c519-111">useDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="3c519-111">useDeviceLicensing</span></span>|<span data-ttu-id="3c519-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="3c519-112">Boolean</span></span>|<span data-ttu-id="3c519-113">Si se deben usar o no las licencias de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c519-113">Whether or not to use device licensing.</span></span>|
|<span data-ttu-id="3c519-114">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3c519-114">vpnConfigurationId</span></span>|<span data-ttu-id="3c519-115">cadena</span><span class="sxs-lookup"><span data-stu-id="3c519-115">String</span></span>|<span data-ttu-id="3c519-116">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="3c519-116">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3c519-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3c519-117">Relationships</span></span>
<span data-ttu-id="3c519-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3c519-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3c519-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3c519-119">JSON Representation</span></span>
<span data-ttu-id="3c519-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3c519-120">Here is a JSON representation of the resource.</span></span>
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



