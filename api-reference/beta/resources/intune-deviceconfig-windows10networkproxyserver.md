---
title: Tipo de recurso windows10NetworkProxyServer
description: Directiva del servidor proxy de red
ms.openlocfilehash: 4e2e995c8d66249e5c742343f74e18e87337bfaa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088659"
---
# <a name="windows10networkproxyserver-resource-type"></a><span data-ttu-id="371ce-103">Tipo de recurso windows10NetworkProxyServer</span><span class="sxs-lookup"><span data-stu-id="371ce-103">windows10NetworkProxyServer resource type</span></span>

> <span data-ttu-id="371ce-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="371ce-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="371ce-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="371ce-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="371ce-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="371ce-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="371ce-107">Directiva del servidor proxy de red</span><span class="sxs-lookup"><span data-stu-id="371ce-107">Network Proxy Server Policy.</span></span>
## <a name="properties"></a><span data-ttu-id="371ce-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="371ce-108">Properties</span></span>
|<span data-ttu-id="371ce-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="371ce-109">Property</span></span>|<span data-ttu-id="371ce-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="371ce-110">Type</span></span>|<span data-ttu-id="371ce-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="371ce-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="371ce-112">address</span><span class="sxs-lookup"><span data-stu-id="371ce-112">address</span></span>|<span data-ttu-id="371ce-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="371ce-113">String</span></span>|<span data-ttu-id="371ce-114">Dirección del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="371ce-114">Address to the proxy server.</span></span> <span data-ttu-id="371ce-115">Especifique una dirección en formato <server>\[":"<port>\]</span><span class="sxs-lookup"><span data-stu-id="371ce-115">Specify an address in the format <server>\[“:”<port>\]</span></span>|
|<span data-ttu-id="371ce-116">excepciones</span><span class="sxs-lookup"><span data-stu-id="371ce-116">exceptions</span></span>|<span data-ttu-id="371ce-117">Colección string</span><span class="sxs-lookup"><span data-stu-id="371ce-117">String collection</span></span>|<span data-ttu-id="371ce-118">Direcciones que el servidor proxy no debe usar.</span><span class="sxs-lookup"><span data-stu-id="371ce-118">Addresses that should not use the proxy server.</span></span> <span data-ttu-id="371ce-119">El sistema no usará el servidor proxy para las direcciones que empiecen por lo que se especifica en este nodo.</span><span class="sxs-lookup"><span data-stu-id="371ce-119">The system will not use the proxy server for addresses beginning with what is specified in this node.</span></span>|
|<span data-ttu-id="371ce-120">useForLocalAddresses</span><span class="sxs-lookup"><span data-stu-id="371ce-120">useForLocalAddresses</span></span>|<span data-ttu-id="371ce-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="371ce-121">Boolean</span></span>|<span data-ttu-id="371ce-122">Especifica si el servidor proxy se debe usar para direcciones locales (intranet).</span><span class="sxs-lookup"><span data-stu-id="371ce-122">Specifies whether the proxy server should be used for local (intranet) addresses.</span></span>|

## <a name="relationships"></a><span data-ttu-id="371ce-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="371ce-123">Relationships</span></span>
<span data-ttu-id="371ce-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="371ce-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="371ce-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="371ce-125">JSON Representation</span></span>
<span data-ttu-id="371ce-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="371ce-126">Here is a JSON representation of the resource.</span></span>
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





