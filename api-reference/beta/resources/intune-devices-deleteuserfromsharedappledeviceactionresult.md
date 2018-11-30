---
title: Tipo de recurso deleteUserFromSharedAppleDeviceActionResult
description: Resultado de la acción Eliminar usuario del dispositivo Apple compartido
ms.openlocfilehash: 5ed6d7b8c07c28dce5ee8cc830a9e86bcdcafa1b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085781"
---
# <a name="deleteuserfromsharedappledeviceactionresult-resource-type"></a><span data-ttu-id="8a4d1-103">Tipo de recurso deleteUserFromSharedAppleDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="8a4d1-103">deleteUserFromSharedAppleDeviceActionResult resource type</span></span>

> <span data-ttu-id="8a4d1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8a4d1-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8a4d1-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8a4d1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8a4d1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8a4d1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8a4d1-107">Resultado de la acción Eliminar usuario del dispositivo Apple compartido</span><span class="sxs-lookup"><span data-stu-id="8a4d1-107">Delete user from shared apple device action result</span></span>

<span data-ttu-id="8a4d1-108">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8a4d1-108">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8a4d1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a4d1-109">Properties</span></span>
|<span data-ttu-id="8a4d1-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a4d1-110">Property</span></span>|<span data-ttu-id="8a4d1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a4d1-111">Type</span></span>|<span data-ttu-id="8a4d1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a4d1-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8a4d1-113">actionName</span><span class="sxs-lookup"><span data-stu-id="8a4d1-113">actionName</span></span>|<span data-ttu-id="8a4d1-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a4d1-114">String</span></span>|<span data-ttu-id="8a4d1-115">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8a4d1-115">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="8a4d1-116">actionState</span><span class="sxs-lookup"><span data-stu-id="8a4d1-116">actionState</span></span>|[<span data-ttu-id="8a4d1-117">actionState</span><span class="sxs-lookup"><span data-stu-id="8a4d1-117">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="8a4d1-118">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="8a4d1-118">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="8a4d1-119">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="8a4d1-119">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="8a4d1-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="8a4d1-120">startDateTime</span></span>|<span data-ttu-id="8a4d1-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a4d1-121">DateTimeOffset</span></span>|<span data-ttu-id="8a4d1-122">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8a4d1-122">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="8a4d1-123">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="8a4d1-123">lastUpdatedDateTime</span></span>|<span data-ttu-id="8a4d1-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a4d1-124">DateTimeOffset</span></span>|<span data-ttu-id="8a4d1-125">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8a4d1-125">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="8a4d1-126">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a4d1-126">userPrincipalName</span></span>|<span data-ttu-id="8a4d1-127">cadena</span><span class="sxs-lookup"><span data-stu-id="8a4d1-127">String</span></span>|<span data-ttu-id="8a4d1-128">Nombre principal de usuario del usuario que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8a4d1-128">User principal name of the user to be deleted</span></span>|

## <a name="relationships"></a><span data-ttu-id="8a4d1-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8a4d1-129">Relationships</span></span>
<span data-ttu-id="8a4d1-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8a4d1-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8a4d1-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8a4d1-131">JSON Representation</span></span>
<span data-ttu-id="8a4d1-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8a4d1-132">Here is a JSON representation of the resource.</span></span>
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





