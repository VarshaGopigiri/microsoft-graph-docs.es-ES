---
title: tipo de recurso windowsKioskLocalUser
description: La clase que se usa para identificar una cuenta local para la configuración de quiosco
ms.openlocfilehash: 1b5b8837f4f93005dabf839a7fc20e3b05b1fbf9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084728"
---
# <a name="windowskiosklocaluser-resource-type"></a><span data-ttu-id="b70fc-103">tipo de recurso windowsKioskLocalUser</span><span class="sxs-lookup"><span data-stu-id="b70fc-103">windowsKioskLocalUser resource type</span></span>

> <span data-ttu-id="b70fc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b70fc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b70fc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b70fc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b70fc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b70fc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b70fc-107">La clase que se usa para identificar una cuenta local para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="b70fc-107">The class used to identify a local account for the kiosk configuration</span></span>

<span data-ttu-id="b70fc-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="b70fc-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="b70fc-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b70fc-109">Properties</span></span>
|<span data-ttu-id="b70fc-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b70fc-110">Property</span></span>|<span data-ttu-id="b70fc-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b70fc-111">Type</span></span>|<span data-ttu-id="b70fc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b70fc-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b70fc-113">userName</span><span class="sxs-lookup"><span data-stu-id="b70fc-113">userName</span></span>|<span data-ttu-id="b70fc-114">String</span><span class="sxs-lookup"><span data-stu-id="b70fc-114">String</span></span>|<span data-ttu-id="b70fc-115">El usuario local que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="b70fc-115">The local user that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="b70fc-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b70fc-116">Relationships</span></span>
<span data-ttu-id="b70fc-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b70fc-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b70fc-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b70fc-118">JSON Representation</span></span>
<span data-ttu-id="b70fc-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b70fc-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskLocalUser"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskLocalUser",
  "userName": "String"
}
```





