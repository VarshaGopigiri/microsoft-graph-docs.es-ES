---
title: Tipo de recurso iosVppAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2dd3f8816aaa4e08066e329e4a9f4630e3f27f1d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867770"
---
# <a name="iosvppappassignmentsettings-resource-type"></a><span data-ttu-id="3784b-103">Tipo de recurso iosVppAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="3784b-103">iosVppAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="3784b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3784b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3784b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3784b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3784b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3784b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3784b-107">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.</span><span class="sxs-lookup"><span data-stu-id="3784b-107">Contains properties used to assign an iOS VPP mobile app to a group.</span></span>

<span data-ttu-id="3784b-108">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="3784b-108">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="3784b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3784b-109">Properties</span></span>
|<span data-ttu-id="3784b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3784b-110">Property</span></span>|<span data-ttu-id="3784b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="3784b-111">Type</span></span>|<span data-ttu-id="3784b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3784b-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3784b-113">useDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="3784b-113">useDeviceLicensing</span></span>|<span data-ttu-id="3784b-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="3784b-114">Boolean</span></span>|<span data-ttu-id="3784b-115">Si se deben usar o no las licencias de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3784b-115">Whether or not to use device licensing.</span></span>|
|<span data-ttu-id="3784b-116">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3784b-116">vpnConfigurationId</span></span>|<span data-ttu-id="3784b-117">cadena</span><span class="sxs-lookup"><span data-stu-id="3784b-117">String</span></span>|<span data-ttu-id="3784b-118">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="3784b-118">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3784b-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3784b-119">Relationships</span></span>
<span data-ttu-id="3784b-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3784b-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3784b-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3784b-121">JSON Representation</span></span>
<span data-ttu-id="3784b-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3784b-122">Here is a JSON representation of the resource.</span></span>
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





