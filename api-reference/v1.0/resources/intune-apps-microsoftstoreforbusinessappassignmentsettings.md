---
title: Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.
ms.openlocfilehash: 62224841548c01ce84901251ab67204b82cbb4c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032562"
---
# <a name="microsoftstoreforbusinessappassignmentsettings-resource-type"></a><span data-ttu-id="bbf8d-103">Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="bbf8d-103">microsoftStoreForBusinessAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="bbf8d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bbf8d-105">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-105">Contains properties used to assign an Microsoft Store for Business mobile app to a group.</span></span>

<span data-ttu-id="bbf8d-106">Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="bbf8d-106">Inherits from [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="bbf8d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbf8d-107">Properties</span></span>
|<span data-ttu-id="bbf8d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bbf8d-108">Property</span></span>|<span data-ttu-id="bbf8d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbf8d-109">Type</span></span>|<span data-ttu-id="bbf8d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbf8d-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bbf8d-111">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="bbf8d-111">useDeviceContext</span></span>|<span data-ttu-id="bbf8d-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="bbf8d-112">Boolean</span></span>|<span data-ttu-id="bbf8d-113">Si se debe usar o no el contexto de ejecución del dispositivo para la aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-113">Whether or not to use device execution context for Microsoft Store for Business mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bbf8d-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bbf8d-114">Relationships</span></span>
<span data-ttu-id="bbf8d-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bbf8d-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="bbf8d-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bbf8d-116">JSON Representation</span></span>
<span data-ttu-id="bbf8d-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-117">Here is a JSON representation of the resource.</span></span>
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



