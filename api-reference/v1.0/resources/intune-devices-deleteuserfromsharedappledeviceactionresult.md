---
title: Tipo de recurso deleteUserFromSharedAppleDeviceActionResult
description: Resultado de la acción Eliminar usuario del dispositivo Apple compartido
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1c6e014f0461c1e6a72a4d67791c27dc401f87f6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804952"
---
# <a name="deleteuserfromsharedappledeviceactionresult-resource-type"></a><span data-ttu-id="c8577-103">Tipo de recurso deleteUserFromSharedAppleDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="c8577-103">deleteUserFromSharedAppleDeviceActionResult resource type</span></span>

> <span data-ttu-id="c8577-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c8577-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c8577-105">Resultado de la acción Eliminar usuario del dispositivo Apple compartido</span><span class="sxs-lookup"><span data-stu-id="c8577-105">Delete user from shared apple device action result</span></span>

<span data-ttu-id="c8577-106">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="c8577-106">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="c8577-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8577-107">Properties</span></span>
|<span data-ttu-id="c8577-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8577-108">Property</span></span>|<span data-ttu-id="c8577-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8577-109">Type</span></span>|<span data-ttu-id="c8577-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8577-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c8577-111">actionName</span><span class="sxs-lookup"><span data-stu-id="c8577-111">actionName</span></span>|<span data-ttu-id="c8577-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8577-112">String</span></span>|<span data-ttu-id="c8577-113">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="c8577-113">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="c8577-114">actionState</span><span class="sxs-lookup"><span data-stu-id="c8577-114">actionState</span></span>|[<span data-ttu-id="c8577-115">actionState</span><span class="sxs-lookup"><span data-stu-id="c8577-115">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="c8577-116">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="c8577-116">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="c8577-117">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="c8577-117">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="c8577-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="c8577-118">startDateTime</span></span>|<span data-ttu-id="c8577-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8577-119">DateTimeOffset</span></span>|<span data-ttu-id="c8577-120">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="c8577-120">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="c8577-121">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="c8577-121">lastUpdatedDateTime</span></span>|<span data-ttu-id="c8577-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8577-122">DateTimeOffset</span></span>|<span data-ttu-id="c8577-123">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="c8577-123">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="c8577-124">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c8577-124">userPrincipalName</span></span>|<span data-ttu-id="c8577-125">cadena</span><span class="sxs-lookup"><span data-stu-id="c8577-125">String</span></span>|<span data-ttu-id="c8577-126">Nombre principal de usuario del usuario que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="c8577-126">User principal name of the user to be deleted</span></span>|

## <a name="relationships"></a><span data-ttu-id="c8577-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c8577-127">Relationships</span></span>
<span data-ttu-id="c8577-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c8577-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c8577-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c8577-129">JSON Representation</span></span>
<span data-ttu-id="c8577-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c8577-130">Here is a JSON representation of the resource.</span></span>
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



