---
title: tipo de recurso officeUserCheckinSummary
description: Entidad que describe el inquilino protección de estadísticas.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c2470b1e531f1b268d6797fe2692baf0031728b3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834026"
---
# <a name="officeusercheckinsummary-resource-type"></a><span data-ttu-id="35d6b-103">tipo de recurso officeUserCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="35d6b-103">officeUserCheckinSummary resource type</span></span>

> <span data-ttu-id="35d6b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="35d6b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="35d6b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="35d6b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="35d6b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="35d6b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="35d6b-107">Entidad que describe el inquilino protección de estadísticas.</span><span class="sxs-lookup"><span data-stu-id="35d6b-107">Entity that describes  tenant check-in stats.</span></span>
## <a name="properties"></a><span data-ttu-id="35d6b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35d6b-108">Properties</span></span>
|<span data-ttu-id="35d6b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="35d6b-109">Property</span></span>|<span data-ttu-id="35d6b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="35d6b-110">Type</span></span>|<span data-ttu-id="35d6b-111">Description</span><span class="sxs-lookup"><span data-stu-id="35d6b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="35d6b-112">succeededUserCount</span><span class="sxs-lookup"><span data-stu-id="35d6b-112">succeededUserCount</span></span>|<span data-ttu-id="35d6b-113">Int32</span><span class="sxs-lookup"><span data-stu-id="35d6b-113">Int32</span></span>|<span data-ttu-id="35d6b-114">Total de usuario correcta comprobar ins para los últimos 3 meses.</span><span class="sxs-lookup"><span data-stu-id="35d6b-114">Total successful user check ins for the last 3 months.</span></span>|
|<span data-ttu-id="35d6b-115">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="35d6b-115">failedUserCount</span></span>|<span data-ttu-id="35d6b-116">Int32</span><span class="sxs-lookup"><span data-stu-id="35d6b-116">Int32</span></span>|<span data-ttu-id="35d6b-117">Total usuario erróneas comprobar ins para los últimos 3 meses.</span><span class="sxs-lookup"><span data-stu-id="35d6b-117">Total failed user check ins for the last 3 months.</span></span>|

## <a name="relationships"></a><span data-ttu-id="35d6b-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="35d6b-118">Relationships</span></span>
<span data-ttu-id="35d6b-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="35d6b-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="35d6b-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="35d6b-120">JSON Representation</span></span>
<span data-ttu-id="35d6b-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="35d6b-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeUserCheckinSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeUserCheckinSummary",
  "succeededUserCount": 1024,
  "failedUserCount": 1024
}
```



