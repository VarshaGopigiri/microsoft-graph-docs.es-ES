---
title: Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2a3af30aeb9be332f5111d2600916a806422fb20
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912053"
---
# <a name="microsoftstoreforbusinessappassignmentsettings-resource-type"></a><span data-ttu-id="72316-103">Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="72316-103">microsoftStoreForBusinessAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="72316-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="72316-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="72316-105">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="72316-105">Contains properties used to assign an Microsoft Store for Business mobile app to a group.</span></span>

<span data-ttu-id="72316-106">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="72316-106">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="72316-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72316-107">Properties</span></span>
|<span data-ttu-id="72316-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72316-108">Property</span></span>|<span data-ttu-id="72316-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="72316-109">Type</span></span>|<span data-ttu-id="72316-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="72316-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="72316-111">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="72316-111">useDeviceContext</span></span>|<span data-ttu-id="72316-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="72316-112">Boolean</span></span>|<span data-ttu-id="72316-113">Si se debe usar o no el contexto de ejecución del dispositivo para la aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="72316-113">Whether or not to use device execution context for Microsoft Store for Business mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="72316-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="72316-114">Relationships</span></span>
<span data-ttu-id="72316-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="72316-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="72316-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="72316-116">JSON Representation</span></span>
<span data-ttu-id="72316-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="72316-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings",
  "useDeviceContext": true
}
```



