---
title: Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.
author: tfitzmac
ms.openlocfilehash: 6c7fed2efda2b4c6d36eb53923b578535cce90e9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354624"
---
# <a name="microsoftstoreforbusinessappassignmentsettings-resource-type"></a><span data-ttu-id="4b023-103">Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="4b023-103">microsoftStoreForBusinessAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="4b023-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4b023-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4b023-105">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="4b023-105">Contains properties used to assign an Microsoft Store for Business mobile app to a group.</span></span>

<span data-ttu-id="4b023-106">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="4b023-106">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="4b023-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4b023-107">Properties</span></span>
|<span data-ttu-id="4b023-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b023-108">Property</span></span>|<span data-ttu-id="4b023-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b023-109">Type</span></span>|<span data-ttu-id="4b023-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b023-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4b023-111">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="4b023-111">useDeviceContext</span></span>|<span data-ttu-id="4b023-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="4b023-112">Boolean</span></span>|<span data-ttu-id="4b023-113">Si se debe usar o no el contexto de ejecución del dispositivo para la aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="4b023-113">Whether or not to use device execution context for Microsoft Store for Business mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4b023-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4b023-114">Relationships</span></span>
<span data-ttu-id="4b023-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4b023-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4b023-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4b023-116">JSON Representation</span></span>
<span data-ttu-id="4b023-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4b023-117">Here is a JSON representation of the resource.</span></span>
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



