---
title: tipo de recurso de servidor de VPN
description: Definición del servidor VPN.
ms.openlocfilehash: e89cc562c3fe0f6b353199ca7de639053177ab1f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086602"
---
# <a name="vpnserver-resource-type"></a><span data-ttu-id="78e6b-103">tipo de recurso de servidor de VPN</span><span class="sxs-lookup"><span data-stu-id="78e6b-103">vpnServer resource type</span></span>

> <span data-ttu-id="78e6b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="78e6b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="78e6b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="78e6b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="78e6b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="78e6b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="78e6b-107">Definición del servidor VPN.</span><span class="sxs-lookup"><span data-stu-id="78e6b-107">VPN Server definition.</span></span>
## <a name="properties"></a><span data-ttu-id="78e6b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78e6b-108">Properties</span></span>
|<span data-ttu-id="78e6b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78e6b-109">Property</span></span>|<span data-ttu-id="78e6b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="78e6b-110">Type</span></span>|<span data-ttu-id="78e6b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="78e6b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="78e6b-112">description</span><span class="sxs-lookup"><span data-stu-id="78e6b-112">description</span></span>|<span data-ttu-id="78e6b-113">String</span><span class="sxs-lookup"><span data-stu-id="78e6b-113">String</span></span>|<span data-ttu-id="78e6b-114">Descripción.</span><span class="sxs-lookup"><span data-stu-id="78e6b-114">Description.</span></span>|
|<span data-ttu-id="78e6b-115">address</span><span class="sxs-lookup"><span data-stu-id="78e6b-115">address</span></span>|<span data-ttu-id="78e6b-116">String</span><span class="sxs-lookup"><span data-stu-id="78e6b-116">String</span></span>|<span data-ttu-id="78e6b-117">Dirección (dirección IP, FQDN o dirección URL)</span><span class="sxs-lookup"><span data-stu-id="78e6b-117">Address (IP address, FQDN or URL)</span></span>|
|<span data-ttu-id="78e6b-118">isDefaultServer</span><span class="sxs-lookup"><span data-stu-id="78e6b-118">isDefaultServer</span></span>|<span data-ttu-id="78e6b-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="78e6b-119">Boolean</span></span>|<span data-ttu-id="78e6b-120">Servidor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="78e6b-120">Default server.</span></span>|

## <a name="relationships"></a><span data-ttu-id="78e6b-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="78e6b-121">Relationships</span></span>
<span data-ttu-id="78e6b-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="78e6b-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="78e6b-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="78e6b-123">JSON Representation</span></span>
<span data-ttu-id="78e6b-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="78e6b-124">Here is a JSON representation of the resource.</span></span>
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





