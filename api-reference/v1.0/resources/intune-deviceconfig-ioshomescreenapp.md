---
title: Tipo de recurso iosHomeScreenApp
description: Representa un icono de una aplicación en la pantalla de inicio
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bb63950229f88fb9987e75f42abfbe39793864ad
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845699"
---
# <a name="ioshomescreenapp-resource-type"></a><span data-ttu-id="65d1a-103">Tipo de recurso iosHomeScreenApp</span><span class="sxs-lookup"><span data-stu-id="65d1a-103">iosHomeScreenApp resource type</span></span>

> <span data-ttu-id="65d1a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="65d1a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="65d1a-105">Representa un icono de una aplicación en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="65d1a-105">Represents an icon for an app on the Home Screen</span></span>

<span data-ttu-id="65d1a-106">Hereda de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="65d1a-106">Inherits from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="65d1a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65d1a-107">Properties</span></span>
|<span data-ttu-id="65d1a-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="65d1a-108">Property</span></span>|<span data-ttu-id="65d1a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="65d1a-109">Type</span></span>|<span data-ttu-id="65d1a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="65d1a-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="65d1a-111">displayName</span><span class="sxs-lookup"><span data-stu-id="65d1a-111">displayName</span></span>|<span data-ttu-id="65d1a-112">cadena</span><span class="sxs-lookup"><span data-stu-id="65d1a-112">String</span></span>|<span data-ttu-id="65d1a-113">Nombre de la aplicación heredado de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="65d1a-113">Name of the app Inherited from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="65d1a-114">bundleID</span><span class="sxs-lookup"><span data-stu-id="65d1a-114">bundleID</span></span>|<span data-ttu-id="65d1a-115">cadena</span><span class="sxs-lookup"><span data-stu-id="65d1a-115">String</span></span>|<span data-ttu-id="65d1a-116">BundleID de la aplicación</span><span class="sxs-lookup"><span data-stu-id="65d1a-116">BundleID of app</span></span>|

## <a name="relationships"></a><span data-ttu-id="65d1a-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="65d1a-117">Relationships</span></span>
<span data-ttu-id="65d1a-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="65d1a-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="65d1a-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="65d1a-119">JSON Representation</span></span>
<span data-ttu-id="65d1a-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="65d1a-120">Here is a JSON representation of the resource.</span></span>
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



