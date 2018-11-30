---
title: Tipo de recurso omaSetting
description: Definición de la configuración de OMA.
ms.openlocfilehash: 7ef8617ca4ce10ebeabf0d7a4655688e58925646
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029984"
---
# <a name="omasetting-resource-type"></a><span data-ttu-id="11313-103">Tipo de recurso omaSetting</span><span class="sxs-lookup"><span data-stu-id="11313-103">omaSetting resource type</span></span>

> <span data-ttu-id="11313-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11313-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11313-105">Definición de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="11313-105">OMA Settings definition.</span></span>
## <a name="properties"></a><span data-ttu-id="11313-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11313-106">Properties</span></span>
|<span data-ttu-id="11313-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11313-107">Property</span></span>|<span data-ttu-id="11313-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="11313-108">Type</span></span>|<span data-ttu-id="11313-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="11313-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11313-110">displayName</span><span class="sxs-lookup"><span data-stu-id="11313-110">displayName</span></span>|<span data-ttu-id="11313-111">cadena</span><span class="sxs-lookup"><span data-stu-id="11313-111">String</span></span>|<span data-ttu-id="11313-112">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="11313-112">Display Name.</span></span>|
|<span data-ttu-id="11313-113">description</span><span class="sxs-lookup"><span data-stu-id="11313-113">description</span></span>|<span data-ttu-id="11313-114">String</span><span class="sxs-lookup"><span data-stu-id="11313-114">String</span></span>|<span data-ttu-id="11313-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="11313-115">Description.</span></span>|
|<span data-ttu-id="11313-116">omaUri</span><span class="sxs-lookup"><span data-stu-id="11313-116">omaUri</span></span>|<span data-ttu-id="11313-117">cadena</span><span class="sxs-lookup"><span data-stu-id="11313-117">String</span></span>|<span data-ttu-id="11313-118">OMA.</span><span class="sxs-lookup"><span data-stu-id="11313-118">OMA.</span></span>|

## <a name="relationships"></a><span data-ttu-id="11313-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11313-119">Relationships</span></span>
<span data-ttu-id="11313-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="11313-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="11313-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11313-121">JSON Representation</span></span>
<span data-ttu-id="11313-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="11313-122">Here is a JSON representation of the resource.</span></span>
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



