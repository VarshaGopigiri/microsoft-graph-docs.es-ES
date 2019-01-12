---
title: Tipo de recurso report
description: 'Devuelve el contenido apropiado para el contexto, incluidos:'
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: dbad8a8808d40c2ae1f7769773b6b29ef65d680f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970650"
---
# <a name="report-resource-type"></a><span data-ttu-id="1e544-103">Tipo de recurso report</span><span class="sxs-lookup"><span data-stu-id="1e544-103">report resource type</span></span>

> <span data-ttu-id="1e544-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1e544-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1e544-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1e544-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1e544-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1e544-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1e544-107">Devuelve el contenido apropiado para el contexto, incluidos:</span><span class="sxs-lookup"><span data-stu-id="1e544-107">Returns the content appropriate for the context, including:</span></span>

- <span data-ttu-id="1e544-108">Informes de historial de perfil de configuración de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1e544-108">Device Configuration profile history reports.</span></span>
- <span data-ttu-id="1e544-109">Informes de errores de inscripción.</span><span class="sxs-lookup"><span data-stu-id="1e544-109">Enrollment failure reports.</span></span>

## <a name="properties"></a><span data-ttu-id="1e544-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e544-110">Properties</span></span>
|<span data-ttu-id="1e544-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e544-111">Property</span></span>|<span data-ttu-id="1e544-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e544-112">Type</span></span>|<span data-ttu-id="1e544-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e544-113">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1e544-114">content</span><span class="sxs-lookup"><span data-stu-id="1e544-114">content</span></span>|<span data-ttu-id="1e544-115">Stream</span><span class="sxs-lookup"><span data-stu-id="1e544-115">Stream</span></span>|<span data-ttu-id="1e544-116">Contenido del informe; detalles varían según el tipo de informe.</span><span class="sxs-lookup"><span data-stu-id="1e544-116">Report content; details vary by report type.</span></span>|

## <a name="relationships"></a><span data-ttu-id="1e544-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1e544-117">Relationships</span></span>
<span data-ttu-id="1e544-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1e544-118">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="1e544-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1e544-119">JSON Representation</span></span>
<span data-ttu-id="1e544-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1e544-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.report"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.report",
  "content": "<Unknown Primitive Type Edm.Stream>"
}
```



