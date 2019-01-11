---
title: tipo de recurso windowsAppXAppAssignmentSettings
description: Contiene propiedades que se usan cuando se asigna una aplicación móvil de Windows AppX a un grupo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2ee4079bcaf25802fe2e1ceac5bbba5eb47c8da4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854267"
---
# <a name="windowsappxappassignmentsettings-resource-type"></a><span data-ttu-id="d1bbb-103">tipo de recurso windowsAppXAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="d1bbb-103">windowsAppXAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="d1bbb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d1bbb-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d1bbb-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d1bbb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d1bbb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d1bbb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d1bbb-107">Contiene propiedades que se usan cuando se asigna una aplicación móvil de Windows AppX a un grupo.</span><span class="sxs-lookup"><span data-stu-id="d1bbb-107">Contains properties used when assigning a Windows AppX mobile app to a group.</span></span>

<span data-ttu-id="d1bbb-108">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="d1bbb-108">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="d1bbb-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1bbb-109">Properties</span></span>
|<span data-ttu-id="d1bbb-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1bbb-110">Property</span></span>|<span data-ttu-id="d1bbb-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1bbb-111">Type</span></span>|<span data-ttu-id="d1bbb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1bbb-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d1bbb-113">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="d1bbb-113">useDeviceContext</span></span>|<span data-ttu-id="d1bbb-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="d1bbb-114">Boolean</span></span>|<span data-ttu-id="d1bbb-115">Si desea usar el contexto de ejecución de dispositivo para la aplicación móvil de Windows AppX.</span><span class="sxs-lookup"><span data-stu-id="d1bbb-115">Whether or not to use device execution context for Windows AppX mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d1bbb-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d1bbb-116">Relationships</span></span>
<span data-ttu-id="d1bbb-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d1bbb-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d1bbb-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d1bbb-118">JSON Representation</span></span>
<span data-ttu-id="d1bbb-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d1bbb-119">Here is a JSON representation of the resource.</span></span>
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





