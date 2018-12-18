---
title: Tipo de recurso deleteUserFromSharedAppleDeviceActionResult
description: Resultado de la acción Eliminar usuario del dispositivo Apple compartido
author: tfitzmac
ms.openlocfilehash: 2dc6dbdeb8bb72314b25f695f82e4f4dfff0b8fd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356038"
---
# <a name="deleteuserfromsharedappledeviceactionresult-resource-type"></a><span data-ttu-id="2b88b-103">Tipo de recurso deleteUserFromSharedAppleDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="2b88b-103">deleteUserFromSharedAppleDeviceActionResult resource type</span></span>

> <span data-ttu-id="2b88b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2b88b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2b88b-105">Resultado de la acción Eliminar usuario del dispositivo Apple compartido</span><span class="sxs-lookup"><span data-stu-id="2b88b-105">Delete user from shared apple device action result</span></span>

<span data-ttu-id="2b88b-106">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="2b88b-106">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="2b88b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b88b-107">Properties</span></span>
|<span data-ttu-id="2b88b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b88b-108">Property</span></span>|<span data-ttu-id="2b88b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b88b-109">Type</span></span>|<span data-ttu-id="2b88b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b88b-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2b88b-111">actionName</span><span class="sxs-lookup"><span data-stu-id="2b88b-111">actionName</span></span>|<span data-ttu-id="2b88b-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="2b88b-112">String</span></span>|<span data-ttu-id="2b88b-113">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="2b88b-113">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="2b88b-114">actionState</span><span class="sxs-lookup"><span data-stu-id="2b88b-114">actionState</span></span>|[<span data-ttu-id="2b88b-115">actionState</span><span class="sxs-lookup"><span data-stu-id="2b88b-115">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="2b88b-116">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="2b88b-116">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="2b88b-117">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="2b88b-117">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="2b88b-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="2b88b-118">startDateTime</span></span>|<span data-ttu-id="2b88b-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2b88b-119">DateTimeOffset</span></span>|<span data-ttu-id="2b88b-120">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="2b88b-120">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="2b88b-121">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="2b88b-121">lastUpdatedDateTime</span></span>|<span data-ttu-id="2b88b-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2b88b-122">DateTimeOffset</span></span>|<span data-ttu-id="2b88b-123">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="2b88b-123">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="2b88b-124">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2b88b-124">userPrincipalName</span></span>|<span data-ttu-id="2b88b-125">cadena</span><span class="sxs-lookup"><span data-stu-id="2b88b-125">String</span></span>|<span data-ttu-id="2b88b-126">Nombre principal de usuario del usuario que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="2b88b-126">User principal name of the user to be deleted</span></span>|

## <a name="relationships"></a><span data-ttu-id="2b88b-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2b88b-127">Relationships</span></span>
<span data-ttu-id="2b88b-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2b88b-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2b88b-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2b88b-129">JSON Representation</span></span>
<span data-ttu-id="2b88b-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2b88b-130">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deleteUserFromSharedAppleDeviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deleteUserFromSharedAppleDeviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "userPrincipalName": "String"
}
```



