---
title: Tipo de recurso iosStoreAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de la tienda iOS.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ca558a4c4be65a7ab8bd3aa880d39689a25863d2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943533"
---
# <a name="iosstoreappassignmentsettings-resource-type"></a><span data-ttu-id="1737e-103">Tipo de recurso iosStoreAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="1737e-103">iosStoreAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="1737e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1737e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1737e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1737e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1737e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1737e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1737e-107">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de la tienda iOS.</span><span class="sxs-lookup"><span data-stu-id="1737e-107">Contains properties used to assign an iOS Store mobile app to a group.</span></span>

<span data-ttu-id="1737e-108">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="1737e-108">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="1737e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1737e-109">Properties</span></span>
|<span data-ttu-id="1737e-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1737e-110">Property</span></span>|<span data-ttu-id="1737e-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1737e-111">Type</span></span>|<span data-ttu-id="1737e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1737e-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1737e-113">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1737e-113">vpnConfigurationId</span></span>|<span data-ttu-id="1737e-114">cadena</span><span class="sxs-lookup"><span data-stu-id="1737e-114">String</span></span>|<span data-ttu-id="1737e-115">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="1737e-115">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="1737e-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1737e-116">Relationships</span></span>
<span data-ttu-id="1737e-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1737e-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1737e-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1737e-118">JSON Representation</span></span>
<span data-ttu-id="1737e-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1737e-119">Here is a JSON representation of the resource.</span></span>
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





