---
title: tipo de recurso windowsUniversalAppXAppAssignmentSettings
description: Contiene propiedades que se usan cuando se asigna una aplicación móvil AppX universales de Windows a un grupo.
author: tfitzmac
ms.openlocfilehash: 46f54acb1116c177e330bda868b975bdf361fe5c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329228"
---
# <a name="windowsuniversalappxappassignmentsettings-resource-type"></a><span data-ttu-id="c220d-103">tipo de recurso windowsUniversalAppXAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="c220d-103">windowsUniversalAppXAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="c220d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c220d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c220d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c220d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c220d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c220d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c220d-107">Contiene propiedades que se usan cuando se asigna una aplicación móvil AppX universales de Windows a un grupo.</span><span class="sxs-lookup"><span data-stu-id="c220d-107">Contains properties used when assigning a Windows Universal AppX mobile app to a group.</span></span>

<span data-ttu-id="c220d-108">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="c220d-108">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="c220d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c220d-109">Properties</span></span>
|<span data-ttu-id="c220d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c220d-110">Property</span></span>|<span data-ttu-id="c220d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="c220d-111">Type</span></span>|<span data-ttu-id="c220d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c220d-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c220d-113">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="c220d-113">useDeviceContext</span></span>|<span data-ttu-id="c220d-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="c220d-114">Boolean</span></span>|<span data-ttu-id="c220d-115">Si desea usar el contexto de ejecución de dispositivo para aplicación móvil AppX universales de Windows.</span><span class="sxs-lookup"><span data-stu-id="c220d-115">Whether or not to use device execution context for Windows Universal AppX mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c220d-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c220d-116">Relationships</span></span>
<span data-ttu-id="c220d-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c220d-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c220d-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c220d-118">JSON Representation</span></span>
<span data-ttu-id="c220d-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c220d-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsUniversalAppXAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUniversalAppXAppAssignmentSettings",
  "useDeviceContext": true
}
```





