---
title: tipo de recurso windowsKioskAzureADUser
description: La clase que se usa para identificar una cuenta de usuario de AzureAD para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4497c6d42db45f518e3ef93e78e50d25f473ac00
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984146"
---
# <a name="windowskioskazureaduser-resource-type"></a><span data-ttu-id="81164-103">tipo de recurso windowsKioskAzureADUser</span><span class="sxs-lookup"><span data-stu-id="81164-103">windowsKioskAzureADUser resource type</span></span>

> <span data-ttu-id="81164-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="81164-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="81164-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="81164-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="81164-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="81164-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="81164-107">La clase que se usa para identificar una cuenta de usuario de AzureAD para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="81164-107">The class used to identify an AzureAD user account for the kiosk configuration</span></span>

<span data-ttu-id="81164-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="81164-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="81164-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81164-109">Properties</span></span>
|<span data-ttu-id="81164-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="81164-110">Property</span></span>|<span data-ttu-id="81164-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="81164-111">Type</span></span>|<span data-ttu-id="81164-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="81164-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="81164-113">userId</span><span class="sxs-lookup"><span data-stu-id="81164-113">userId</span></span>|<span data-ttu-id="81164-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="81164-114">String</span></span>|<span data-ttu-id="81164-115">El identificador del usuario AzureAD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="81164-115">The ID of the AzureAD user that will be locked to this kiosk configuration</span></span>|
|<span data-ttu-id="81164-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="81164-116">userPrincipalName</span></span>|<span data-ttu-id="81164-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="81164-117">String</span></span>|<span data-ttu-id="81164-118">Las cuentas de usuario que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="81164-118">The user accounts that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="81164-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="81164-119">Relationships</span></span>
<span data-ttu-id="81164-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="81164-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="81164-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="81164-121">JSON Representation</span></span>
<span data-ttu-id="81164-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="81164-122">Here is a JSON representation of the resource.</span></span>
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





