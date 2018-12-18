---
title: Tipo de recurso iosVppAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.
author: tfitzmac
ms.openlocfilehash: 65a143c1f6cc9eed4dfdc6dabeb6f9379517277c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310251"
---
# <a name="iosvppappassignmentsettings-resource-type"></a><span data-ttu-id="73746-103">Tipo de recurso iosVppAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="73746-103">iosVppAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="73746-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="73746-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="73746-105">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.</span><span class="sxs-lookup"><span data-stu-id="73746-105">Contains properties used to assign an iOS VPP mobile app to a group.</span></span>

<span data-ttu-id="73746-106">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="73746-106">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="73746-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73746-107">Properties</span></span>
|<span data-ttu-id="73746-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73746-108">Property</span></span>|<span data-ttu-id="73746-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="73746-109">Type</span></span>|<span data-ttu-id="73746-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="73746-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="73746-111">useDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="73746-111">useDeviceLicensing</span></span>|<span data-ttu-id="73746-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="73746-112">Boolean</span></span>|<span data-ttu-id="73746-113">Si se deben usar o no las licencias de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73746-113">Whether or not to use device licensing.</span></span>|
|<span data-ttu-id="73746-114">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="73746-114">vpnConfigurationId</span></span>|<span data-ttu-id="73746-115">cadena</span><span class="sxs-lookup"><span data-stu-id="73746-115">String</span></span>|<span data-ttu-id="73746-116">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="73746-116">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="73746-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="73746-117">Relationships</span></span>
<span data-ttu-id="73746-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="73746-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="73746-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="73746-119">JSON Representation</span></span>
<span data-ttu-id="73746-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="73746-120">Here is a JSON representation of the resource.</span></span>
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



