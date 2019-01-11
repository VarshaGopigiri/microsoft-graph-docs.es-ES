---
title: Tipo de recurso iosStoreAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de la tienda iOS.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 34776d6002926486baa05d0720ce1c7eeecee927
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822235"
---
# <a name="iosstoreappassignmentsettings-resource-type"></a><span data-ttu-id="8ce59-103">Tipo de recurso iosStoreAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="8ce59-103">iosStoreAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="8ce59-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8ce59-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8ce59-105">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de la tienda iOS.</span><span class="sxs-lookup"><span data-stu-id="8ce59-105">Contains properties used to assign an iOS Store mobile app to a group.</span></span>

<span data-ttu-id="8ce59-106">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="8ce59-106">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8ce59-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ce59-107">Properties</span></span>
|<span data-ttu-id="8ce59-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ce59-108">Property</span></span>|<span data-ttu-id="8ce59-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ce59-109">Type</span></span>|<span data-ttu-id="8ce59-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ce59-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8ce59-111">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8ce59-111">vpnConfigurationId</span></span>|<span data-ttu-id="8ce59-112">cadena</span><span class="sxs-lookup"><span data-stu-id="8ce59-112">String</span></span>|<span data-ttu-id="8ce59-113">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="8ce59-113">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8ce59-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8ce59-114">Relationships</span></span>
<span data-ttu-id="8ce59-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8ce59-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8ce59-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8ce59-116">JSON Representation</span></span>
<span data-ttu-id="8ce59-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8ce59-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosStoreAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosStoreAppAssignmentSettings",
  "vpnConfigurationId": "String"
}
```



