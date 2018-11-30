---
title: Tipo de recurso omaSetting
description: Definición de la configuración de OMA.
ms.openlocfilehash: 900e3f4d8e24743ed75b15f7a57188b46630c9fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084403"
---
# <a name="omasetting-resource-type"></a><span data-ttu-id="e3472-103">Tipo de recurso omaSetting</span><span class="sxs-lookup"><span data-stu-id="e3472-103">omaSetting resource type</span></span>

> <span data-ttu-id="e3472-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e3472-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e3472-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e3472-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e3472-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e3472-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e3472-107">Definición de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="e3472-107">OMA Settings definition.</span></span>
## <a name="properties"></a><span data-ttu-id="e3472-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3472-108">Properties</span></span>
|<span data-ttu-id="e3472-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3472-109">Property</span></span>|<span data-ttu-id="e3472-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3472-110">Type</span></span>|<span data-ttu-id="e3472-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3472-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e3472-112">displayName</span><span class="sxs-lookup"><span data-stu-id="e3472-112">displayName</span></span>|<span data-ttu-id="e3472-113">cadena</span><span class="sxs-lookup"><span data-stu-id="e3472-113">String</span></span>|<span data-ttu-id="e3472-114">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e3472-114">Display Name.</span></span>|
|<span data-ttu-id="e3472-115">description</span><span class="sxs-lookup"><span data-stu-id="e3472-115">description</span></span>|<span data-ttu-id="e3472-116">String</span><span class="sxs-lookup"><span data-stu-id="e3472-116">String</span></span>|<span data-ttu-id="e3472-117">Descripción.</span><span class="sxs-lookup"><span data-stu-id="e3472-117">Description.</span></span>|
|<span data-ttu-id="e3472-118">omaUri</span><span class="sxs-lookup"><span data-stu-id="e3472-118">omaUri</span></span>|<span data-ttu-id="e3472-119">cadena</span><span class="sxs-lookup"><span data-stu-id="e3472-119">String</span></span>|<span data-ttu-id="e3472-120">OMA.</span><span class="sxs-lookup"><span data-stu-id="e3472-120">OMA.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e3472-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e3472-121">Relationships</span></span>
<span data-ttu-id="e3472-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e3472-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e3472-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e3472-123">JSON Representation</span></span>
<span data-ttu-id="e3472-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e3472-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSetting"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSetting",
  "displayName": "String",
  "description": "String",
  "omaUri": "String"
}
```





