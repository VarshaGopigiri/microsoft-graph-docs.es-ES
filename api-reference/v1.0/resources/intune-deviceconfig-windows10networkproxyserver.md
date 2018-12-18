---
title: Tipo de recurso windows10NetworkProxyServer
description: Directiva del servidor proxy de red
author: tfitzmac
ms.openlocfilehash: c2eaeaa4d89f981e5fa992e7a79a7863f0848a9f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344040"
---
# <a name="windows10networkproxyserver-resource-type"></a><span data-ttu-id="4780f-103">Tipo de recurso windows10NetworkProxyServer</span><span class="sxs-lookup"><span data-stu-id="4780f-103">windows10NetworkProxyServer resource type</span></span>

> <span data-ttu-id="4780f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4780f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4780f-105">Directiva del servidor proxy de red</span><span class="sxs-lookup"><span data-stu-id="4780f-105">Network Proxy Server Policy.</span></span>
## <a name="properties"></a><span data-ttu-id="4780f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4780f-106">Properties</span></span>
|<span data-ttu-id="4780f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4780f-107">Property</span></span>|<span data-ttu-id="4780f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4780f-108">Type</span></span>|<span data-ttu-id="4780f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4780f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4780f-110">address</span><span class="sxs-lookup"><span data-stu-id="4780f-110">address</span></span>|<span data-ttu-id="4780f-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="4780f-111">String</span></span>|<span data-ttu-id="4780f-112">Dirección del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="4780f-112">Address to the proxy server.</span></span> <span data-ttu-id="4780f-113">Especifique una dirección en formato <server>\[":"<port>\]</span><span class="sxs-lookup"><span data-stu-id="4780f-113">Specify an address in the format <server>\[“:”<port>\]</span></span>|
|<span data-ttu-id="4780f-114">excepciones</span><span class="sxs-lookup"><span data-stu-id="4780f-114">exceptions</span></span>|<span data-ttu-id="4780f-115">Colección string</span><span class="sxs-lookup"><span data-stu-id="4780f-115">String collection</span></span>|<span data-ttu-id="4780f-116">Direcciones que el servidor proxy no debe usar.</span><span class="sxs-lookup"><span data-stu-id="4780f-116">Addresses that should not use the proxy server.</span></span> <span data-ttu-id="4780f-117">El sistema no usará el servidor proxy para las direcciones que empiecen por lo que se especifica en este nodo.</span><span class="sxs-lookup"><span data-stu-id="4780f-117">The system will not use the proxy server for addresses beginning with what is specified in this node.</span></span>|
|<span data-ttu-id="4780f-118">useForLocalAddresses</span><span class="sxs-lookup"><span data-stu-id="4780f-118">useForLocalAddresses</span></span>|<span data-ttu-id="4780f-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="4780f-119">Boolean</span></span>|<span data-ttu-id="4780f-120">Especifica si el servidor proxy se debe usar para direcciones locales (intranet).</span><span class="sxs-lookup"><span data-stu-id="4780f-120">Specifies whether the proxy server should be used for local (intranet) addresses.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4780f-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4780f-121">Relationships</span></span>
<span data-ttu-id="4780f-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4780f-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4780f-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4780f-123">JSON Representation</span></span>
<span data-ttu-id="4780f-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4780f-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windows10NetworkProxyServer"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10NetworkProxyServer",
  "address": "String",
  "exceptions": [
    "String"
  ],
  "useForLocalAddresses": true
}
```



