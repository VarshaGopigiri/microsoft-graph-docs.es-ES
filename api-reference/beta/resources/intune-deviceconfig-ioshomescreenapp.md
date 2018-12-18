---
title: Tipo de recurso iosHomeScreenApp
description: Representa un icono de una aplicación en la pantalla de inicio
author: tfitzmac
ms.openlocfilehash: 63bcfe53cc2d3ee60b5f784e99798f1f97e883af
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334968"
---
# <a name="ioshomescreenapp-resource-type"></a><span data-ttu-id="e2092-103">Tipo de recurso iosHomeScreenApp</span><span class="sxs-lookup"><span data-stu-id="e2092-103">iosHomeScreenApp resource type</span></span>

> <span data-ttu-id="e2092-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e2092-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e2092-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e2092-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e2092-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e2092-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e2092-107">Representa un icono de una aplicación en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="e2092-107">Represents an icon for an app on the Home Screen</span></span>

<span data-ttu-id="e2092-108">Hereda de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="e2092-108">Inherits from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e2092-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2092-109">Properties</span></span>
|<span data-ttu-id="e2092-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2092-110">Property</span></span>|<span data-ttu-id="e2092-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2092-111">Type</span></span>|<span data-ttu-id="e2092-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2092-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e2092-113">displayName</span><span class="sxs-lookup"><span data-stu-id="e2092-113">displayName</span></span>|<span data-ttu-id="e2092-114">cadena</span><span class="sxs-lookup"><span data-stu-id="e2092-114">String</span></span>|<span data-ttu-id="e2092-115">Nombre de la aplicación heredado de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="e2092-115">Name of the app Inherited from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="e2092-116">bundleID</span><span class="sxs-lookup"><span data-stu-id="e2092-116">bundleID</span></span>|<span data-ttu-id="e2092-117">cadena</span><span class="sxs-lookup"><span data-stu-id="e2092-117">String</span></span>|<span data-ttu-id="e2092-118">BundleID de la aplicación</span><span class="sxs-lookup"><span data-stu-id="e2092-118">BundleID of app</span></span>|

## <a name="relationships"></a><span data-ttu-id="e2092-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e2092-119">Relationships</span></span>
<span data-ttu-id="e2092-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e2092-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e2092-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e2092-121">JSON Representation</span></span>
<span data-ttu-id="e2092-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e2092-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosHomeScreenApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenApp",
  "displayName": "String",
  "bundleID": "String"
}
```





