---
title: tipo de recurso managedDeviceReportedApp
description: Datos de aplicación para la creación de informes
ms.openlocfilehash: 820269422891e01352a7f605d62147a84facea67
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083977"
---
# <a name="manageddevicereportedapp-resource-type"></a><span data-ttu-id="c12b7-103">tipo de recurso managedDeviceReportedApp</span><span class="sxs-lookup"><span data-stu-id="c12b7-103">managedDeviceReportedApp resource type</span></span>

> <span data-ttu-id="c12b7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c12b7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c12b7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c12b7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c12b7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c12b7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c12b7-107">Datos de aplicación para la creación de informes</span><span class="sxs-lookup"><span data-stu-id="c12b7-107">Application data for reporting</span></span>
## <a name="properties"></a><span data-ttu-id="c12b7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c12b7-108">Properties</span></span>
|<span data-ttu-id="c12b7-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c12b7-109">Property</span></span>|<span data-ttu-id="c12b7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c12b7-110">Type</span></span>|<span data-ttu-id="c12b7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c12b7-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c12b7-112">appId</span><span class="sxs-lookup"><span data-stu-id="c12b7-112">appId</span></span>|<span data-ttu-id="c12b7-113">cadena</span><span class="sxs-lookup"><span data-stu-id="c12b7-113">String</span></span>|<span data-ttu-id="c12b7-114">El identificador de la aplicación o de la agrupación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="c12b7-114">The application or bundle identifier of the application</span></span>|

## <a name="relationships"></a><span data-ttu-id="c12b7-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c12b7-115">Relationships</span></span>
<span data-ttu-id="c12b7-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c12b7-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c12b7-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c12b7-117">JSON Representation</span></span>
<span data-ttu-id="c12b7-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c12b7-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedDeviceReportedApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceReportedApp",
  "appId": "String"
}
```





