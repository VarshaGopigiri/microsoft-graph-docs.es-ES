---
title: Tipo de recurso iosLobAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de línea de negocio para iOS.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7f2e0c9ca5b2628343b79ff972e50c3684651c23
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990519"
---
# <a name="ioslobappassignmentsettings-resource-type"></a><span data-ttu-id="fb98b-103">Tipo de recurso iosLobAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="fb98b-103">iosLobAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="fb98b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fb98b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fb98b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fb98b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fb98b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fb98b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fb98b-107">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de línea de negocio para iOS.</span><span class="sxs-lookup"><span data-stu-id="fb98b-107">Contains properties used to assign an iOS LOB mobile app to a group.</span></span>

<span data-ttu-id="fb98b-108">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="fb98b-108">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="fb98b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb98b-109">Properties</span></span>
|<span data-ttu-id="fb98b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb98b-110">Property</span></span>|<span data-ttu-id="fb98b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb98b-111">Type</span></span>|<span data-ttu-id="fb98b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb98b-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fb98b-113">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fb98b-113">vpnConfigurationId</span></span>|<span data-ttu-id="fb98b-114">cadena</span><span class="sxs-lookup"><span data-stu-id="fb98b-114">String</span></span>|<span data-ttu-id="fb98b-115">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb98b-115">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fb98b-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fb98b-116">Relationships</span></span>
<span data-ttu-id="fb98b-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fb98b-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fb98b-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fb98b-118">JSON Representation</span></span>
<span data-ttu-id="fb98b-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fb98b-119">Here is a JSON representation of the resource.</span></span>
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





