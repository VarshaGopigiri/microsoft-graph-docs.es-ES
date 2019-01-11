---
title: tipo de recurso de servidor de VPN
description: Definición del servidor VPN.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b48daa95cc2227f6d1691902a75614446c93a10a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889876"
---
# <a name="vpnserver-resource-type"></a><span data-ttu-id="feb19-103">tipo de recurso de servidor de VPN</span><span class="sxs-lookup"><span data-stu-id="feb19-103">vpnServer resource type</span></span>

> <span data-ttu-id="feb19-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="feb19-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="feb19-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="feb19-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="feb19-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="feb19-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="feb19-107">Definición del servidor VPN.</span><span class="sxs-lookup"><span data-stu-id="feb19-107">VPN Server definition.</span></span>
## <a name="properties"></a><span data-ttu-id="feb19-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="feb19-108">Properties</span></span>
|<span data-ttu-id="feb19-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="feb19-109">Property</span></span>|<span data-ttu-id="feb19-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="feb19-110">Type</span></span>|<span data-ttu-id="feb19-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="feb19-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="feb19-112">description</span><span class="sxs-lookup"><span data-stu-id="feb19-112">description</span></span>|<span data-ttu-id="feb19-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="feb19-113">String</span></span>|<span data-ttu-id="feb19-114">Descripción.</span><span class="sxs-lookup"><span data-stu-id="feb19-114">Description.</span></span>|
|<span data-ttu-id="feb19-115">address</span><span class="sxs-lookup"><span data-stu-id="feb19-115">address</span></span>|<span data-ttu-id="feb19-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="feb19-116">String</span></span>|<span data-ttu-id="feb19-117">Dirección (dirección IP, FQDN o dirección URL)</span><span class="sxs-lookup"><span data-stu-id="feb19-117">Address (IP address, FQDN or URL)</span></span>|
|<span data-ttu-id="feb19-118">isDefaultServer</span><span class="sxs-lookup"><span data-stu-id="feb19-118">isDefaultServer</span></span>|<span data-ttu-id="feb19-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="feb19-119">Boolean</span></span>|<span data-ttu-id="feb19-120">Servidor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="feb19-120">Default server.</span></span>|

## <a name="relationships"></a><span data-ttu-id="feb19-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="feb19-121">Relationships</span></span>
<span data-ttu-id="feb19-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="feb19-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="feb19-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="feb19-123">JSON Representation</span></span>
<span data-ttu-id="feb19-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="feb19-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnServer"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnServer",
  "description": "String",
  "address": "String",
  "isDefaultServer": true
}
```





