---
title: Tipo de recurso iosHomeScreenApp
description: Representa un icono de una aplicación en la pantalla de inicio
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 39db8de19fbfc568f85c4930e8c3124ffea2dd57
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850599"
---
# <a name="ioshomescreenapp-resource-type"></a><span data-ttu-id="f77eb-103">Tipo de recurso iosHomeScreenApp</span><span class="sxs-lookup"><span data-stu-id="f77eb-103">iosHomeScreenApp resource type</span></span>

> <span data-ttu-id="f77eb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f77eb-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f77eb-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f77eb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f77eb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f77eb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f77eb-107">Representa un icono de una aplicación en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="f77eb-107">Represents an icon for an app on the Home Screen</span></span>

<span data-ttu-id="f77eb-108">Hereda de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="f77eb-108">Inherits from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="f77eb-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f77eb-109">Properties</span></span>
|<span data-ttu-id="f77eb-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f77eb-110">Property</span></span>|<span data-ttu-id="f77eb-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="f77eb-111">Type</span></span>|<span data-ttu-id="f77eb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f77eb-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f77eb-113">displayName</span><span class="sxs-lookup"><span data-stu-id="f77eb-113">displayName</span></span>|<span data-ttu-id="f77eb-114">cadena</span><span class="sxs-lookup"><span data-stu-id="f77eb-114">String</span></span>|<span data-ttu-id="f77eb-115">Nombre de la aplicación heredado de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="f77eb-115">Name of the app Inherited from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="f77eb-116">bundleID</span><span class="sxs-lookup"><span data-stu-id="f77eb-116">bundleID</span></span>|<span data-ttu-id="f77eb-117">cadena</span><span class="sxs-lookup"><span data-stu-id="f77eb-117">String</span></span>|<span data-ttu-id="f77eb-118">BundleID de la aplicación</span><span class="sxs-lookup"><span data-stu-id="f77eb-118">BundleID of app</span></span>|

## <a name="relationships"></a><span data-ttu-id="f77eb-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f77eb-119">Relationships</span></span>
<span data-ttu-id="f77eb-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f77eb-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f77eb-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f77eb-121">JSON Representation</span></span>
<span data-ttu-id="f77eb-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f77eb-122">Here is a JSON representation of the resource.</span></span>
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





