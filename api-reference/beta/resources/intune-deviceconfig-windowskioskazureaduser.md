---
title: tipo de recurso windowsKioskAzureADUser
description: La clase que se usa para identificar una cuenta de usuario de AzureAD para la configuración de quiosco
author: tfitzmac
ms.openlocfilehash: e4048b4cbea592af350af20bf433ca00ac6d4980
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330075"
---
# <a name="windowskioskazureaduser-resource-type"></a><span data-ttu-id="ca898-103">tipo de recurso windowsKioskAzureADUser</span><span class="sxs-lookup"><span data-stu-id="ca898-103">windowsKioskAzureADUser resource type</span></span>

> <span data-ttu-id="ca898-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ca898-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ca898-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ca898-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ca898-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ca898-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ca898-107">La clase que se usa para identificar una cuenta de usuario de AzureAD para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="ca898-107">The class used to identify an AzureAD user account for the kiosk configuration</span></span>

<span data-ttu-id="ca898-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="ca898-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ca898-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca898-109">Properties</span></span>
|<span data-ttu-id="ca898-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ca898-110">Property</span></span>|<span data-ttu-id="ca898-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca898-111">Type</span></span>|<span data-ttu-id="ca898-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca898-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ca898-113">userId</span><span class="sxs-lookup"><span data-stu-id="ca898-113">userId</span></span>|<span data-ttu-id="ca898-114">String</span><span class="sxs-lookup"><span data-stu-id="ca898-114">String</span></span>|<span data-ttu-id="ca898-115">El identificador del usuario AzureAD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="ca898-115">The ID of the AzureAD user that will be locked to this kiosk configuration</span></span>|
|<span data-ttu-id="ca898-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca898-116">userPrincipalName</span></span>|<span data-ttu-id="ca898-117">String</span><span class="sxs-lookup"><span data-stu-id="ca898-117">String</span></span>|<span data-ttu-id="ca898-118">Las cuentas de usuario que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="ca898-118">The user accounts that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="ca898-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ca898-119">Relationships</span></span>
<span data-ttu-id="ca898-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ca898-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ca898-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ca898-121">JSON Representation</span></span>
<span data-ttu-id="ca898-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ca898-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskAzureADUser"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskAzureADUser",
  "userId": "String",
  "userPrincipalName": "String"
}
```





