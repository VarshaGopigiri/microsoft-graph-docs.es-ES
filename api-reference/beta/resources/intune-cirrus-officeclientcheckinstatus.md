---
title: tipo de recurso officeClientCheckinStatus
description: Entidad que describe el inquilino protección de estadísticas.
author: tfitzmac
ms.openlocfilehash: 0c6359d3cb6c776d0f26fdaf88ce7f2f03e5f8c7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331720"
---
# <a name="officeclientcheckinstatus-resource-type"></a><span data-ttu-id="ee3f8-103">tipo de recurso officeClientCheckinStatus</span><span class="sxs-lookup"><span data-stu-id="ee3f8-103">officeClientCheckinStatus resource type</span></span>

> <span data-ttu-id="ee3f8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee3f8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ee3f8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ee3f8-107">Entidad que describe el inquilino protección de estadísticas.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-107">Entity that describes  tenant check-in stats.</span></span>
## <a name="properties"></a><span data-ttu-id="ee3f8-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee3f8-108">Properties</span></span>
|<span data-ttu-id="ee3f8-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee3f8-109">Property</span></span>|<span data-ttu-id="ee3f8-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee3f8-110">Type</span></span>|<span data-ttu-id="ee3f8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee3f8-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ee3f8-112">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ee3f8-112">userPrincipalName</span></span>|<span data-ttu-id="ee3f8-113">String</span><span class="sxs-lookup"><span data-stu-id="ee3f8-113">String</span></span>|<span data-ttu-id="ee3f8-114">Nombre principal de usuario con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-114">User principal name using the device.</span></span>|
|<span data-ttu-id="ee3f8-115">deviceName</span><span class="sxs-lookup"><span data-stu-id="ee3f8-115">deviceName</span></span>|<span data-ttu-id="ee3f8-116">String</span><span class="sxs-lookup"><span data-stu-id="ee3f8-116">String</span></span>|<span data-ttu-id="ee3f8-117">Nombre del dispositivo intenta protección.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-117">Device name trying to check-in.</span></span>|
|<span data-ttu-id="ee3f8-118">devicePlatform</span><span class="sxs-lookup"><span data-stu-id="ee3f8-118">devicePlatform</span></span>|<span data-ttu-id="ee3f8-119">String</span><span class="sxs-lookup"><span data-stu-id="ee3f8-119">String</span></span>|<span data-ttu-id="ee3f8-120">Plataforma de dispositivo intenta protección.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-120">Device platform trying to check-in.</span></span>|
|<span data-ttu-id="ee3f8-121">devicePlatformVersion</span><span class="sxs-lookup"><span data-stu-id="ee3f8-121">devicePlatformVersion</span></span>|<span data-ttu-id="ee3f8-122">String</span><span class="sxs-lookup"><span data-stu-id="ee3f8-122">String</span></span>|<span data-ttu-id="ee3f8-123">Versión de plataforma de dispositivo intenta protección.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-123">Device platform version trying to check-in.</span></span>|
|<span data-ttu-id="ee3f8-124">wasSuccessful</span><span class="sxs-lookup"><span data-stu-id="ee3f8-124">wasSuccessful</span></span>|<span data-ttu-id="ee3f8-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee3f8-125">Boolean</span></span>|<span data-ttu-id="ee3f8-126">Si el último registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-126">If the last checkin was successful.</span></span>|
|<span data-ttu-id="ee3f8-127">userId</span><span class="sxs-lookup"><span data-stu-id="ee3f8-127">userId</span></span>|<span data-ttu-id="ee3f8-128">String</span><span class="sxs-lookup"><span data-stu-id="ee3f8-128">String</span></span>|<span data-ttu-id="ee3f8-129">Identificador de usuario usando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-129">User identifier using the device.</span></span>|
|<span data-ttu-id="ee3f8-130">checkinDateTime</span><span class="sxs-lookup"><span data-stu-id="ee3f8-130">checkinDateTime</span></span>|<span data-ttu-id="ee3f8-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ee3f8-131">DateTimeOffset</span></span>|<span data-ttu-id="ee3f8-132">Dispositivo última verificación en hora en UTC.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-132">Last device check-in time in UTC.</span></span>|
|<span data-ttu-id="ee3f8-133">errorMessage</span><span class="sxs-lookup"><span data-stu-id="ee3f8-133">errorMessage</span></span>|<span data-ttu-id="ee3f8-134">String</span><span class="sxs-lookup"><span data-stu-id="ee3f8-134">String</span></span>|<span data-ttu-id="ee3f8-135">Aparece un mensaje de error si hay alguno asociado para el último registro.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-135">Error message if any associated for the last checkin.</span></span>|
|<span data-ttu-id="ee3f8-136">appliedPolicies</span><span class="sxs-lookup"><span data-stu-id="ee3f8-136">appliedPolicies</span></span>|<span data-ttu-id="ee3f8-137">Colección String</span><span class="sxs-lookup"><span data-stu-id="ee3f8-137">String collection</span></span>|<span data-ttu-id="ee3f8-138">Lista de directivas de entrega en el dispositivo como último checkin.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-138">List of policies delivered to the device as last checkin.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ee3f8-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ee3f8-139">Relationships</span></span>
<span data-ttu-id="ee3f8-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ee3f8-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ee3f8-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ee3f8-141">JSON Representation</span></span>
<span data-ttu-id="ee3f8-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-142">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeClientCheckinStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeClientCheckinStatus",
  "userPrincipalName": "String",
  "deviceName": "String",
  "devicePlatform": "String",
  "devicePlatformVersion": "String",
  "wasSuccessful": true,
  "userId": "String",
  "checkinDateTime": "String (timestamp)",
  "errorMessage": "String",
  "appliedPolicies": [
    "String"
  ]
}
```



