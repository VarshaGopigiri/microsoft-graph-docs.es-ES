---
title: tipo de recurso windowsAppXAppAssignmentSettings
description: Contiene propiedades que se usan cuando se asigna una aplicación móvil de Windows AppX a un grupo.
ms.openlocfilehash: ce65e3fbc841e2df6dc378b7f440fd588c7bf1d5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085076"
---
# <a name="windowsappxappassignmentsettings-resource-type"></a><span data-ttu-id="af9f7-103">tipo de recurso windowsAppXAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="af9f7-103">windowsAppXAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="af9f7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="af9f7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="af9f7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="af9f7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="af9f7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="af9f7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="af9f7-107">Contiene propiedades que se usan cuando se asigna una aplicación móvil de Windows AppX a un grupo.</span><span class="sxs-lookup"><span data-stu-id="af9f7-107">Contains properties used when assigning a Windows AppX mobile app to a group.</span></span>

<span data-ttu-id="af9f7-108">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="af9f7-108">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="af9f7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af9f7-109">Properties</span></span>
|<span data-ttu-id="af9f7-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="af9f7-110">Property</span></span>|<span data-ttu-id="af9f7-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="af9f7-111">Type</span></span>|<span data-ttu-id="af9f7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="af9f7-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="af9f7-113">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="af9f7-113">useDeviceContext</span></span>|<span data-ttu-id="af9f7-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="af9f7-114">Boolean</span></span>|<span data-ttu-id="af9f7-115">Si desea usar el contexto de ejecución de dispositivo para la aplicación móvil de Windows AppX.</span><span class="sxs-lookup"><span data-stu-id="af9f7-115">Whether or not to use device execution context for Windows AppX mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="af9f7-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="af9f7-116">Relationships</span></span>
<span data-ttu-id="af9f7-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="af9f7-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="af9f7-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="af9f7-118">JSON Representation</span></span>
<span data-ttu-id="af9f7-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="af9f7-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsAppXAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsAppXAppAssignmentSettings",
  "useDeviceContext": true
}
```




