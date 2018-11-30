---
title: Tipo de recurso proxiedDomain
description: Dominio con proxy
ms.openlocfilehash: 310ccb1420ed450c9e7c53d534181720f9051ff4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084179"
---
# <a name="proxieddomain-resource-type"></a><span data-ttu-id="34c8d-103">Tipo de recurso proxiedDomain</span><span class="sxs-lookup"><span data-stu-id="34c8d-103">proxiedDomain resource type</span></span>

> <span data-ttu-id="34c8d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="34c8d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="34c8d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="34c8d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="34c8d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="34c8d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="34c8d-107">Dominio con proxy</span><span class="sxs-lookup"><span data-stu-id="34c8d-107">Proxied Domain</span></span>

## <a name="properties"></a><span data-ttu-id="34c8d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34c8d-108">Properties</span></span>
|<span data-ttu-id="34c8d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34c8d-109">Property</span></span>|<span data-ttu-id="34c8d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c8d-110">Type</span></span>|<span data-ttu-id="34c8d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="34c8d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="34c8d-112">ipAddressOrFQDN</span><span class="sxs-lookup"><span data-stu-id="34c8d-112">ipAddressOrFQDN</span></span>|<span data-ttu-id="34c8d-113">cadena</span><span class="sxs-lookup"><span data-stu-id="34c8d-113">String</span></span>|<span data-ttu-id="34c8d-114">La dirección IP o el nombre de dominio completo (FQDN).</span><span class="sxs-lookup"><span data-stu-id="34c8d-114">The IP address or fully qualified domain name (FQDN).</span></span>|
|<span data-ttu-id="34c8d-115">proxy</span><span class="sxs-lookup"><span data-stu-id="34c8d-115">proxy</span></span>|<span data-ttu-id="34c8d-116">cadena</span><span class="sxs-lookup"><span data-stu-id="34c8d-116">String</span></span>|<span data-ttu-id="34c8d-117">Dirección IP del proxy o el FQDN.</span><span class="sxs-lookup"><span data-stu-id="34c8d-117">Proxy IP address or FQDN.</span></span>|

## <a name="relationships"></a><span data-ttu-id="34c8d-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="34c8d-118">Relationships</span></span>
<span data-ttu-id="34c8d-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="34c8d-119">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="34c8d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="34c8d-120">JSON Representation</span></span>
<span data-ttu-id="34c8d-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="34c8d-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.proxiedDomain"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.proxiedDomain",
  "ipAddressOrFQDN": "String",
  "proxy": "String"
}
```



