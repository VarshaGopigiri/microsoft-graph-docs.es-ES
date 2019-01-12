---
title: tipo de recurso windowsKioskAzureADGroup
description: La clase que se usa para identificar un grupo de AzureAD para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 18ca386f0e1ee4647cff2a0ff5be9f2098d8f447
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964735"
---
# <a name="windowskioskazureadgroup-resource-type"></a><span data-ttu-id="846ef-103">tipo de recurso windowsKioskAzureADGroup</span><span class="sxs-lookup"><span data-stu-id="846ef-103">windowsKioskAzureADGroup resource type</span></span>

> <span data-ttu-id="846ef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="846ef-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="846ef-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="846ef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="846ef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="846ef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="846ef-107">La clase que se usa para identificar un grupo de AzureAD para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="846ef-107">The class used to identify an AzureAD group for the kiosk configuration</span></span>

<span data-ttu-id="846ef-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="846ef-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="846ef-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="846ef-109">Properties</span></span>
|<span data-ttu-id="846ef-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="846ef-110">Property</span></span>|<span data-ttu-id="846ef-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="846ef-111">Type</span></span>|<span data-ttu-id="846ef-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="846ef-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="846ef-113">displayName</span><span class="sxs-lookup"><span data-stu-id="846ef-113">displayName</span></span>|<span data-ttu-id="846ef-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="846ef-114">String</span></span>|<span data-ttu-id="846ef-115">El nombre para mostrar del grupo AzureAD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="846ef-115">The display name of the AzureAD group that will be locked to this kiosk configuration</span></span>|
|<span data-ttu-id="846ef-116">groupId</span><span class="sxs-lookup"><span data-stu-id="846ef-116">groupId</span></span>|<span data-ttu-id="846ef-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="846ef-117">String</span></span>|<span data-ttu-id="846ef-118">El identificador del grupo AzureAD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="846ef-118">The ID of the AzureAD group that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="846ef-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="846ef-119">Relationships</span></span>
<span data-ttu-id="846ef-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="846ef-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="846ef-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="846ef-121">JSON Representation</span></span>
<span data-ttu-id="846ef-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="846ef-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskAzureADGroup"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskAzureADGroup",
  "displayName": "String",
  "groupId": "String"
}
```





