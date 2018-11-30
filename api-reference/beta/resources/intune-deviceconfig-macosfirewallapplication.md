---
title: tipo de recurso macOSFirewallApplication
description: Representa una aplicación en la lista de aplicaciones de servidor de seguridad de Mac OS
ms.openlocfilehash: 6e016f2191fd9b366bbdf5dbaef5562284a6b5ae
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084828"
---
# <a name="macosfirewallapplication-resource-type"></a><span data-ttu-id="ec409-103">tipo de recurso macOSFirewallApplication</span><span class="sxs-lookup"><span data-stu-id="ec409-103">macOSFirewallApplication resource type</span></span>

> <span data-ttu-id="ec409-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ec409-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ec409-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ec409-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ec409-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ec409-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ec409-107">Representa una aplicación en la lista de aplicaciones de servidor de seguridad de Mac OS</span><span class="sxs-lookup"><span data-stu-id="ec409-107">Represents an app in the list of macOS firewall applications</span></span>
## <a name="properties"></a><span data-ttu-id="ec409-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec409-108">Properties</span></span>
|<span data-ttu-id="ec409-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec409-109">Property</span></span>|<span data-ttu-id="ec409-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec409-110">Type</span></span>|<span data-ttu-id="ec409-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec409-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ec409-112">bundleId</span><span class="sxs-lookup"><span data-stu-id="ec409-112">bundleId</span></span>|<span data-ttu-id="ec409-113">String</span><span class="sxs-lookup"><span data-stu-id="ec409-113">String</span></span>|<span data-ttu-id="ec409-114">BundleId de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ec409-114">BundleId of the application.</span></span>|
|<span data-ttu-id="ec409-115">allowsIncomingConnections</span><span class="sxs-lookup"><span data-stu-id="ec409-115">allowsIncomingConnections</span></span>|<span data-ttu-id="ec409-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="ec409-116">Boolean</span></span>|<span data-ttu-id="ec409-117">Si se permiten las conexiones entrantes.</span><span class="sxs-lookup"><span data-stu-id="ec409-117">Whether or not incoming connections are allowed.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ec409-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ec409-118">Relationships</span></span>
<span data-ttu-id="ec409-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ec409-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ec409-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ec409-120">JSON Representation</span></span>
<span data-ttu-id="ec409-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ec409-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSFirewallApplication"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSFirewallApplication",
  "bundleId": "String",
  "allowsIncomingConnections": true
}
```





