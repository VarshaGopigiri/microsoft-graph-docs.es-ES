---
title: tipo de recurso ExtendeKeyUsage
description: Definición de uso de clave extendida personalizada
author: tfitzmac
ms.openlocfilehash: 2b6155a0fbb234cb0b2081a8a4a226a8d218dbc2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337292"
---
# <a name="extendedkeyusage-resource-type"></a><span data-ttu-id="cf33b-103">tipo de recurso ExtendeKeyUsage</span><span class="sxs-lookup"><span data-stu-id="cf33b-103">extendedKeyUsage resource type</span></span>

> <span data-ttu-id="cf33b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cf33b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cf33b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cf33b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cf33b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf33b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf33b-107">Definición de uso de clave extendida personalizada</span><span class="sxs-lookup"><span data-stu-id="cf33b-107">Custom Extended Key Usage definition</span></span>
## <a name="properties"></a><span data-ttu-id="cf33b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf33b-108">Properties</span></span>
|<span data-ttu-id="cf33b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf33b-109">Property</span></span>|<span data-ttu-id="cf33b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf33b-110">Type</span></span>|<span data-ttu-id="cf33b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf33b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf33b-112">name</span><span class="sxs-lookup"><span data-stu-id="cf33b-112">name</span></span>|<span data-ttu-id="cf33b-113">String</span><span class="sxs-lookup"><span data-stu-id="cf33b-113">String</span></span>|<span data-ttu-id="cf33b-114">Nombre de uso de clave extendida</span><span class="sxs-lookup"><span data-stu-id="cf33b-114">Extended Key Usage Name</span></span>|
|<span data-ttu-id="cf33b-115">objectIdentifier</span><span class="sxs-lookup"><span data-stu-id="cf33b-115">objectIdentifier</span></span>|<span data-ttu-id="cf33b-116">String</span><span class="sxs-lookup"><span data-stu-id="cf33b-116">String</span></span>|<span data-ttu-id="cf33b-117">Identificador de objeto de uso de la clave de extendido</span><span class="sxs-lookup"><span data-stu-id="cf33b-117">Extended Key Usage Object Identifier</span></span>|

## <a name="relationships"></a><span data-ttu-id="cf33b-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cf33b-118">Relationships</span></span>
<span data-ttu-id="cf33b-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cf33b-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cf33b-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cf33b-120">JSON Representation</span></span>
<span data-ttu-id="cf33b-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cf33b-121">Here is a JSON representation of the resource.</span></span>
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





