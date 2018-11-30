---
title: Tipo de recurso iosVppAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.
ms.openlocfilehash: c7ae6221aa978cc1412de25521dd8b08ff72c0c3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088723"
---
# <a name="iosvppappassignmentsettings-resource-type"></a><span data-ttu-id="c2e02-103">Tipo de recurso iosVppAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="c2e02-103">iosVppAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="c2e02-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c2e02-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2e02-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c2e02-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c2e02-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c2e02-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c2e02-107">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.</span><span class="sxs-lookup"><span data-stu-id="c2e02-107">Contains properties used to assign an iOS VPP mobile app to a group.</span></span>

<span data-ttu-id="c2e02-108">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="c2e02-108">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="c2e02-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2e02-109">Properties</span></span>
|<span data-ttu-id="c2e02-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2e02-110">Property</span></span>|<span data-ttu-id="c2e02-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2e02-111">Type</span></span>|<span data-ttu-id="c2e02-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2e02-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c2e02-113">useDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="c2e02-113">useDeviceLicensing</span></span>|<span data-ttu-id="c2e02-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="c2e02-114">Boolean</span></span>|<span data-ttu-id="c2e02-115">Si se deben usar o no las licencias de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2e02-115">Whether or not to use device licensing.</span></span>|
|<span data-ttu-id="c2e02-116">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c2e02-116">vpnConfigurationId</span></span>|<span data-ttu-id="c2e02-117">cadena</span><span class="sxs-lookup"><span data-stu-id="c2e02-117">String</span></span>|<span data-ttu-id="c2e02-118">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2e02-118">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c2e02-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c2e02-119">Relationships</span></span>
<span data-ttu-id="c2e02-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c2e02-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c2e02-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c2e02-121">JSON Representation</span></span>
<span data-ttu-id="c2e02-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c2e02-122">Here is a JSON representation of the resource.</span></span>
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





