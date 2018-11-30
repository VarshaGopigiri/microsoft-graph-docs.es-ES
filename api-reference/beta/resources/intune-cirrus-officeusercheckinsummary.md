---
title: tipo de recurso officeUserCheckinSummary
description: Entidad que describe el inquilino protección de estadísticas.
ms.openlocfilehash: b8b3cc0c6129782a25a12cf22659cb6849a81e26
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085562"
---
# <a name="officeusercheckinsummary-resource-type"></a><span data-ttu-id="6a19c-103">tipo de recurso officeUserCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="6a19c-103">officeUserCheckinSummary resource type</span></span>

> <span data-ttu-id="6a19c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6a19c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6a19c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6a19c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6a19c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6a19c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6a19c-107">Entidad que describe el inquilino protección de estadísticas.</span><span class="sxs-lookup"><span data-stu-id="6a19c-107">Entity that describes  tenant check-in stats.</span></span>
## <a name="properties"></a><span data-ttu-id="6a19c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a19c-108">Properties</span></span>
|<span data-ttu-id="6a19c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6a19c-109">Property</span></span>|<span data-ttu-id="6a19c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a19c-110">Type</span></span>|<span data-ttu-id="6a19c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a19c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6a19c-112">succeededUserCount</span><span class="sxs-lookup"><span data-stu-id="6a19c-112">succeededUserCount</span></span>|<span data-ttu-id="6a19c-113">Int32</span><span class="sxs-lookup"><span data-stu-id="6a19c-113">Int32</span></span>|<span data-ttu-id="6a19c-114">Total de usuario correcta comprobar ins para los últimos 3 meses.</span><span class="sxs-lookup"><span data-stu-id="6a19c-114">Total successful user check ins for the last 3 months.</span></span>|
|<span data-ttu-id="6a19c-115">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="6a19c-115">failedUserCount</span></span>|<span data-ttu-id="6a19c-116">Int32</span><span class="sxs-lookup"><span data-stu-id="6a19c-116">Int32</span></span>|<span data-ttu-id="6a19c-117">Total usuario erróneas comprobar ins para los últimos 3 meses.</span><span class="sxs-lookup"><span data-stu-id="6a19c-117">Total failed user check ins for the last 3 months.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6a19c-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6a19c-118">Relationships</span></span>
<span data-ttu-id="6a19c-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6a19c-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6a19c-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6a19c-120">JSON Representation</span></span>
<span data-ttu-id="6a19c-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6a19c-121">Here is a JSON representation of the resource.</span></span>
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



