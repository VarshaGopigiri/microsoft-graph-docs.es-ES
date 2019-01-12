---
title: tipo de recurso ExtendeKeyUsage
description: Definición de uso de clave extendida personalizada
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: bb08bf086ce8386e424ebd6355a4920e87be59a0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928447"
---
# <a name="extendedkeyusage-resource-type"></a><span data-ttu-id="593c1-103">tipo de recurso ExtendeKeyUsage</span><span class="sxs-lookup"><span data-stu-id="593c1-103">extendedKeyUsage resource type</span></span>

> <span data-ttu-id="593c1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="593c1-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="593c1-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="593c1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="593c1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="593c1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="593c1-107">Definición de uso de clave extendida personalizada</span><span class="sxs-lookup"><span data-stu-id="593c1-107">Custom Extended Key Usage definition</span></span>
## <a name="properties"></a><span data-ttu-id="593c1-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="593c1-108">Properties</span></span>
|<span data-ttu-id="593c1-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="593c1-109">Property</span></span>|<span data-ttu-id="593c1-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="593c1-110">Type</span></span>|<span data-ttu-id="593c1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="593c1-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="593c1-112">name</span><span class="sxs-lookup"><span data-stu-id="593c1-112">name</span></span>|<span data-ttu-id="593c1-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="593c1-113">String</span></span>|<span data-ttu-id="593c1-114">Nombre de uso de clave extendida</span><span class="sxs-lookup"><span data-stu-id="593c1-114">Extended Key Usage Name</span></span>|
|<span data-ttu-id="593c1-115">objectIdentifier</span><span class="sxs-lookup"><span data-stu-id="593c1-115">objectIdentifier</span></span>|<span data-ttu-id="593c1-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="593c1-116">String</span></span>|<span data-ttu-id="593c1-117">Identificador de objeto de uso de la clave de extendido</span><span class="sxs-lookup"><span data-stu-id="593c1-117">Extended Key Usage Object Identifier</span></span>|

## <a name="relationships"></a><span data-ttu-id="593c1-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="593c1-118">Relationships</span></span>
<span data-ttu-id="593c1-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="593c1-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="593c1-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="593c1-120">JSON Representation</span></span>
<span data-ttu-id="593c1-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="593c1-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.extendedKeyUsage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.extendedKeyUsage",
  "name": "String",
  "objectIdentifier": "String"
}
```





