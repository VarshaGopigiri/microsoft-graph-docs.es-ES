---
title: tipo de recurso officeClientCheckinStatus
description: Entidad que describe el inquilino protección de estadísticas.
ms.openlocfilehash: a87a085d42ce0754e046b319b270ddf90a3bdba7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085759"
---
# <a name="officeclientcheckinstatus-resource-type"></a><span data-ttu-id="d4674-103">tipo de recurso officeClientCheckinStatus</span><span class="sxs-lookup"><span data-stu-id="d4674-103">officeClientCheckinStatus resource type</span></span>

> <span data-ttu-id="d4674-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d4674-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d4674-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d4674-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d4674-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d4674-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d4674-107">Entidad que describe el inquilino protección de estadísticas.</span><span class="sxs-lookup"><span data-stu-id="d4674-107">Entity that describes  tenant check-in stats.</span></span>
## <a name="properties"></a><span data-ttu-id="d4674-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4674-108">Properties</span></span>
|<span data-ttu-id="d4674-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4674-109">Property</span></span>|<span data-ttu-id="d4674-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4674-110">Type</span></span>|<span data-ttu-id="d4674-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4674-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d4674-112">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4674-112">userPrincipalName</span></span>|<span data-ttu-id="d4674-113">String</span><span class="sxs-lookup"><span data-stu-id="d4674-113">String</span></span>|<span data-ttu-id="d4674-114">Nombre principal de usuario con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4674-114">User principal name using the device.</span></span>|
|<span data-ttu-id="d4674-115">deviceName</span><span class="sxs-lookup"><span data-stu-id="d4674-115">deviceName</span></span>|<span data-ttu-id="d4674-116">String</span><span class="sxs-lookup"><span data-stu-id="d4674-116">String</span></span>|<span data-ttu-id="d4674-117">Nombre del dispositivo intenta protección.</span><span class="sxs-lookup"><span data-stu-id="d4674-117">Device name trying to check-in.</span></span>|
|<span data-ttu-id="d4674-118">devicePlatform</span><span class="sxs-lookup"><span data-stu-id="d4674-118">devicePlatform</span></span>|<span data-ttu-id="d4674-119">String</span><span class="sxs-lookup"><span data-stu-id="d4674-119">String</span></span>|<span data-ttu-id="d4674-120">Plataforma de dispositivo intenta protección.</span><span class="sxs-lookup"><span data-stu-id="d4674-120">Device platform trying to check-in.</span></span>|
|<span data-ttu-id="d4674-121">devicePlatformVersion</span><span class="sxs-lookup"><span data-stu-id="d4674-121">devicePlatformVersion</span></span>|<span data-ttu-id="d4674-122">String</span><span class="sxs-lookup"><span data-stu-id="d4674-122">String</span></span>|<span data-ttu-id="d4674-123">Versión de plataforma de dispositivo intenta protección.</span><span class="sxs-lookup"><span data-stu-id="d4674-123">Device platform version trying to check-in.</span></span>|
|<span data-ttu-id="d4674-124">wasSuccessful</span><span class="sxs-lookup"><span data-stu-id="d4674-124">wasSuccessful</span></span>|<span data-ttu-id="d4674-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4674-125">Boolean</span></span>|<span data-ttu-id="d4674-126">Si el último registro se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4674-126">If the last checkin was successful.</span></span>|
|<span data-ttu-id="d4674-127">userId</span><span class="sxs-lookup"><span data-stu-id="d4674-127">userId</span></span>|<span data-ttu-id="d4674-128">String</span><span class="sxs-lookup"><span data-stu-id="d4674-128">String</span></span>|<span data-ttu-id="d4674-129">Identificador de usuario usando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4674-129">User identifier using the device.</span></span>|
|<span data-ttu-id="d4674-130">checkinDateTime</span><span class="sxs-lookup"><span data-stu-id="d4674-130">checkinDateTime</span></span>|<span data-ttu-id="d4674-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4674-131">DateTimeOffset</span></span>|<span data-ttu-id="d4674-132">Dispositivo última verificación en hora en UTC.</span><span class="sxs-lookup"><span data-stu-id="d4674-132">Last device check-in time in UTC.</span></span>|
|<span data-ttu-id="d4674-133">errorMessage</span><span class="sxs-lookup"><span data-stu-id="d4674-133">errorMessage</span></span>|<span data-ttu-id="d4674-134">String</span><span class="sxs-lookup"><span data-stu-id="d4674-134">String</span></span>|<span data-ttu-id="d4674-135">Aparece un mensaje de error si hay alguno asociado para el último registro.</span><span class="sxs-lookup"><span data-stu-id="d4674-135">Error message if any associated for the last checkin.</span></span>|
|<span data-ttu-id="d4674-136">appliedPolicies</span><span class="sxs-lookup"><span data-stu-id="d4674-136">appliedPolicies</span></span>|<span data-ttu-id="d4674-137">Colección String</span><span class="sxs-lookup"><span data-stu-id="d4674-137">String collection</span></span>|<span data-ttu-id="d4674-138">Lista de directivas de entrega en el dispositivo como último checkin.</span><span class="sxs-lookup"><span data-stu-id="d4674-138">List of policies delivered to the device as last checkin.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d4674-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d4674-139">Relationships</span></span>
<span data-ttu-id="d4674-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d4674-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d4674-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d4674-141">JSON Representation</span></span>
<span data-ttu-id="d4674-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d4674-142">Here is a JSON representation of the resource.</span></span>
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



