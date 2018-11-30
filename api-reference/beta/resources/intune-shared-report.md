---
title: Tipo de recurso report
description: 'Devuelve el contenido apropiado para el contexto, incluidos:'
ms.openlocfilehash: b05e5db2b948455f14746cf23a07b3fd788ccad9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088554"
---
# <a name="report-resource-type"></a><span data-ttu-id="841c9-103">Tipo de recurso report</span><span class="sxs-lookup"><span data-stu-id="841c9-103">report resource type</span></span>

> <span data-ttu-id="841c9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="841c9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="841c9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="841c9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="841c9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="841c9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="841c9-107">Devuelve el contenido apropiado para el contexto, incluidos:</span><span class="sxs-lookup"><span data-stu-id="841c9-107">Returns the content appropriate for the context, including:</span></span>

- <span data-ttu-id="841c9-108">Informes de historial de perfil de configuración de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="841c9-108">Device Configuration profile history reports.</span></span>
- <span data-ttu-id="841c9-109">Informes de errores de inscripción.</span><span class="sxs-lookup"><span data-stu-id="841c9-109">Enrollment failure reports.</span></span>

## <a name="properties"></a><span data-ttu-id="841c9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="841c9-110">Properties</span></span>
|<span data-ttu-id="841c9-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="841c9-111">Property</span></span>|<span data-ttu-id="841c9-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="841c9-112">Type</span></span>|<span data-ttu-id="841c9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="841c9-113">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="841c9-114">content</span><span class="sxs-lookup"><span data-stu-id="841c9-114">content</span></span>|<span data-ttu-id="841c9-115">Stream</span><span class="sxs-lookup"><span data-stu-id="841c9-115">Stream</span></span>|<span data-ttu-id="841c9-116">Contenido del informe; detalles varían según el tipo de informe.</span><span class="sxs-lookup"><span data-stu-id="841c9-116">Report content; details vary by report type.</span></span>|

## <a name="relationships"></a><span data-ttu-id="841c9-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="841c9-117">Relationships</span></span>
<span data-ttu-id="841c9-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="841c9-118">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="841c9-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="841c9-119">JSON Representation</span></span>
<span data-ttu-id="841c9-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="841c9-120">Here is a JSON representation of the resource.</span></span>
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



