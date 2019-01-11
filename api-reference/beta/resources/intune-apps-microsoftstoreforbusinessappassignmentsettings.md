---
title: Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8ef23919912d8a91beceefeb034de7cc09cb941c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805029"
---
# <a name="microsoftstoreforbusinessappassignmentsettings-resource-type"></a><span data-ttu-id="084a2-103">Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="084a2-103">microsoftStoreForBusinessAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="084a2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="084a2-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="084a2-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="084a2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="084a2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="084a2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="084a2-107">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="084a2-107">Contains properties used to assign an Microsoft Store for Business mobile app to a group.</span></span>

<span data-ttu-id="084a2-108">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="084a2-108">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="084a2-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="084a2-109">Properties</span></span>
|<span data-ttu-id="084a2-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="084a2-110">Property</span></span>|<span data-ttu-id="084a2-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="084a2-111">Type</span></span>|<span data-ttu-id="084a2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="084a2-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="084a2-113">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="084a2-113">useDeviceContext</span></span>|<span data-ttu-id="084a2-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="084a2-114">Boolean</span></span>|<span data-ttu-id="084a2-115">Si se debe usar o no el contexto de ejecución del dispositivo para la aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="084a2-115">Whether or not to use device execution context for Microsoft Store for Business mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="084a2-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="084a2-116">Relationships</span></span>
<span data-ttu-id="084a2-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="084a2-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="084a2-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="084a2-118">JSON Representation</span></span>
<span data-ttu-id="084a2-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="084a2-119">Here is a JSON representation of the resource.</span></span>
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





