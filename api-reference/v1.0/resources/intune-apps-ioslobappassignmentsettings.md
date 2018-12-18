---
title: Tipo de recurso iosLobAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de línea de negocio para iOS.
author: tfitzmac
ms.openlocfilehash: 78de511bdbdf2e4a8b16d9ce32a790329d2eb3c9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306093"
---
# <a name="ioslobappassignmentsettings-resource-type"></a><span data-ttu-id="3cd5d-103">Tipo de recurso iosLobAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="3cd5d-103">iosLobAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="3cd5d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3cd5d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3cd5d-105">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de línea de negocio para iOS.</span><span class="sxs-lookup"><span data-stu-id="3cd5d-105">Contains properties used to assign an iOS LOB mobile app to a group.</span></span>

<span data-ttu-id="3cd5d-106">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="3cd5d-106">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="3cd5d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3cd5d-107">Properties</span></span>
|<span data-ttu-id="3cd5d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3cd5d-108">Property</span></span>|<span data-ttu-id="3cd5d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3cd5d-109">Type</span></span>|<span data-ttu-id="3cd5d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cd5d-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3cd5d-111">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3cd5d-111">vpnConfigurationId</span></span>|<span data-ttu-id="3cd5d-112">cadena</span><span class="sxs-lookup"><span data-stu-id="3cd5d-112">String</span></span>|<span data-ttu-id="3cd5d-113">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="3cd5d-113">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3cd5d-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3cd5d-114">Relationships</span></span>
<span data-ttu-id="3cd5d-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3cd5d-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3cd5d-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3cd5d-116">JSON Representation</span></span>
<span data-ttu-id="3cd5d-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3cd5d-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosLobAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosLobAppAssignmentSettings",
  "vpnConfigurationId": "String"
}
```



