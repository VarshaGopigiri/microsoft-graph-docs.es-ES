---
title: Tipo de recurso windows10NetworkProxyServer
description: Directiva del servidor proxy de red
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c193c5b5d1ba61626bb348f52caf39ded58a77c8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951918"
---
# <a name="windows10networkproxyserver-resource-type"></a><span data-ttu-id="85fd6-103">Tipo de recurso windows10NetworkProxyServer</span><span class="sxs-lookup"><span data-stu-id="85fd6-103">windows10NetworkProxyServer resource type</span></span>

> <span data-ttu-id="85fd6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="85fd6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="85fd6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="85fd6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="85fd6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="85fd6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="85fd6-107">Directiva del servidor proxy de red</span><span class="sxs-lookup"><span data-stu-id="85fd6-107">Network Proxy Server Policy.</span></span>
## <a name="properties"></a><span data-ttu-id="85fd6-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85fd6-108">Properties</span></span>
|<span data-ttu-id="85fd6-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85fd6-109">Property</span></span>|<span data-ttu-id="85fd6-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="85fd6-110">Type</span></span>|<span data-ttu-id="85fd6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="85fd6-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="85fd6-112">address</span><span class="sxs-lookup"><span data-stu-id="85fd6-112">address</span></span>|<span data-ttu-id="85fd6-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="85fd6-113">String</span></span>|<span data-ttu-id="85fd6-114">Dirección del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="85fd6-114">Address to the proxy server.</span></span> <span data-ttu-id="85fd6-115">Especifique una dirección en formato <server>\[":"<port>\]</span><span class="sxs-lookup"><span data-stu-id="85fd6-115">Specify an address in the format <server>\[“:”<port>\]</span></span>|
|<span data-ttu-id="85fd6-116">excepciones</span><span class="sxs-lookup"><span data-stu-id="85fd6-116">exceptions</span></span>|<span data-ttu-id="85fd6-117">Colección string</span><span class="sxs-lookup"><span data-stu-id="85fd6-117">String collection</span></span>|<span data-ttu-id="85fd6-118">Direcciones que el servidor proxy no debe usar.</span><span class="sxs-lookup"><span data-stu-id="85fd6-118">Addresses that should not use the proxy server.</span></span> <span data-ttu-id="85fd6-119">El sistema no usará el servidor proxy para las direcciones que empiecen por lo que se especifica en este nodo.</span><span class="sxs-lookup"><span data-stu-id="85fd6-119">The system will not use the proxy server for addresses beginning with what is specified in this node.</span></span>|
|<span data-ttu-id="85fd6-120">useForLocalAddresses</span><span class="sxs-lookup"><span data-stu-id="85fd6-120">useForLocalAddresses</span></span>|<span data-ttu-id="85fd6-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="85fd6-121">Boolean</span></span>|<span data-ttu-id="85fd6-122">Especifica si el servidor proxy se debe usar para direcciones locales (intranet).</span><span class="sxs-lookup"><span data-stu-id="85fd6-122">Specifies whether the proxy server should be used for local (intranet) addresses.</span></span>|

## <a name="relationships"></a><span data-ttu-id="85fd6-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="85fd6-123">Relationships</span></span>
<span data-ttu-id="85fd6-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="85fd6-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="85fd6-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="85fd6-125">JSON Representation</span></span>
<span data-ttu-id="85fd6-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="85fd6-126">Here is a JSON representation of the resource.</span></span>
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





