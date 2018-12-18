---
title: Tipo de recurso iosHomeScreenApp
description: Representa un icono de una aplicación en la pantalla de inicio
author: tfitzmac
ms.openlocfilehash: 68fe4e7b5a226422cc0aaf980ac7fb0421a9bfc0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350375"
---
# <a name="ioshomescreenapp-resource-type"></a><span data-ttu-id="651fd-103">Tipo de recurso iosHomeScreenApp</span><span class="sxs-lookup"><span data-stu-id="651fd-103">iosHomeScreenApp resource type</span></span>

> <span data-ttu-id="651fd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="651fd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="651fd-105">Representa un icono de una aplicación en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="651fd-105">Represents an icon for an app on the Home Screen</span></span>

<span data-ttu-id="651fd-106">Hereda de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="651fd-106">Inherits from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="651fd-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="651fd-107">Properties</span></span>
|<span data-ttu-id="651fd-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="651fd-108">Property</span></span>|<span data-ttu-id="651fd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="651fd-109">Type</span></span>|<span data-ttu-id="651fd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="651fd-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="651fd-111">displayName</span><span class="sxs-lookup"><span data-stu-id="651fd-111">displayName</span></span>|<span data-ttu-id="651fd-112">cadena</span><span class="sxs-lookup"><span data-stu-id="651fd-112">String</span></span>|<span data-ttu-id="651fd-113">Nombre de la aplicación heredado de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="651fd-113">Name of the app Inherited from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="651fd-114">bundleID</span><span class="sxs-lookup"><span data-stu-id="651fd-114">bundleID</span></span>|<span data-ttu-id="651fd-115">cadena</span><span class="sxs-lookup"><span data-stu-id="651fd-115">String</span></span>|<span data-ttu-id="651fd-116">BundleID de la aplicación</span><span class="sxs-lookup"><span data-stu-id="651fd-116">BundleID of app</span></span>|

## <a name="relationships"></a><span data-ttu-id="651fd-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="651fd-117">Relationships</span></span>
<span data-ttu-id="651fd-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="651fd-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="651fd-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="651fd-119">JSON Representation</span></span>
<span data-ttu-id="651fd-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="651fd-120">Here is a JSON representation of the resource.</span></span>
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



