---
title: tipo de recurso managedDeviceReportedApp
description: Datos de aplicación para la creación de informes
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8aa9a4d825e2333e135a676fa1eeb88e7cfe079c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942979"
---
# <a name="manageddevicereportedapp-resource-type"></a><span data-ttu-id="7947d-103">tipo de recurso managedDeviceReportedApp</span><span class="sxs-lookup"><span data-stu-id="7947d-103">managedDeviceReportedApp resource type</span></span>

> <span data-ttu-id="7947d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7947d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7947d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7947d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7947d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7947d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7947d-107">Datos de aplicación para la creación de informes</span><span class="sxs-lookup"><span data-stu-id="7947d-107">Application data for reporting</span></span>
## <a name="properties"></a><span data-ttu-id="7947d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7947d-108">Properties</span></span>
|<span data-ttu-id="7947d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7947d-109">Property</span></span>|<span data-ttu-id="7947d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7947d-110">Type</span></span>|<span data-ttu-id="7947d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7947d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7947d-112">appId</span><span class="sxs-lookup"><span data-stu-id="7947d-112">appId</span></span>|<span data-ttu-id="7947d-113">cadena</span><span class="sxs-lookup"><span data-stu-id="7947d-113">String</span></span>|<span data-ttu-id="7947d-114">El identificador de la aplicación o de la agrupación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7947d-114">The application or bundle identifier of the application</span></span>|

## <a name="relationships"></a><span data-ttu-id="7947d-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7947d-115">Relationships</span></span>
<span data-ttu-id="7947d-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7947d-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7947d-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7947d-117">JSON Representation</span></span>
<span data-ttu-id="7947d-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7947d-118">Here is a JSON representation of the resource.</span></span>
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





