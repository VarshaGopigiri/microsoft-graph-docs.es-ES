---
title: Tipo de recurso sharedPCAccountManagerPolicy
description: Directiva de administrador de cuentas de PC compartido. Solo se aplica cuando el administrador de cuentas está activado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b094f4761680da2fbead6f522a297f6d6450c197
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937666"
---
# <a name="sharedpcaccountmanagerpolicy-resource-type"></a><span data-ttu-id="2a950-104">Tipo de recurso sharedPCAccountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="2a950-104">sharedPCAccountManagerPolicy resource type</span></span>

> <span data-ttu-id="2a950-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2a950-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2a950-106">Directiva de administrador de cuentas de PC compartido.</span><span class="sxs-lookup"><span data-stu-id="2a950-106">SharedPC Account Manager Policy.</span></span> <span data-ttu-id="2a950-107">Solo se aplica cuando el administrador de cuentas está activado.</span><span class="sxs-lookup"><span data-stu-id="2a950-107">Only applies when the account manager is enabled.</span></span>
## <a name="properties"></a><span data-ttu-id="2a950-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a950-108">Properties</span></span>
|<span data-ttu-id="2a950-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2a950-109">Property</span></span>|<span data-ttu-id="2a950-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a950-110">Type</span></span>|<span data-ttu-id="2a950-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a950-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2a950-112">accountDeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="2a950-112">accountDeletionPolicy</span></span>|[<span data-ttu-id="2a950-113">sharedPCAccountDeletionPolicyType</span><span class="sxs-lookup"><span data-stu-id="2a950-113">sharedPCAccountDeletionPolicyType</span></span>](../resources/intune-deviceconfig-sharedpcaccountdeletionpolicytype.md)|<span data-ttu-id="2a950-114">Configura cuándo se eliminan las cuentas.</span><span class="sxs-lookup"><span data-stu-id="2a950-114">Configures when accounts are deleted.</span></span> <span data-ttu-id="2a950-115">Los valores posibles son: `immediate`, `diskSpaceThreshold` y `diskSpaceThresholdOrInactiveThreshold`.</span><span class="sxs-lookup"><span data-stu-id="2a950-115">Possible values are: `immediate`, `diskSpaceThreshold`, `diskSpaceThresholdOrInactiveThreshold`.</span></span>|
|<span data-ttu-id="2a950-116">cacheAccountsAboveDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="2a950-116">cacheAccountsAboveDiskFreePercentage</span></span>|<span data-ttu-id="2a950-117">Int32</span><span class="sxs-lookup"><span data-stu-id="2a950-117">Int32</span></span>|<span data-ttu-id="2a950-118">Establece el porcentaje de espacio en disco disponible que debería tener un equipo antes de detener la eliminación de cuentas de equipo compartido en caché.</span><span class="sxs-lookup"><span data-stu-id="2a950-118">Sets the percentage of available disk space a PC should have before it stops deleting cached shared PC accounts.</span></span> <span data-ttu-id="2a950-119">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="2a950-119">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="2a950-120">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="2a950-120">Valid values 0 to 100</span></span>|
|<span data-ttu-id="2a950-121">inactiveThresholdDays</span><span class="sxs-lookup"><span data-stu-id="2a950-121">inactiveThresholdDays</span></span>|<span data-ttu-id="2a950-122">Int32</span><span class="sxs-lookup"><span data-stu-id="2a950-122">Int32</span></span>|<span data-ttu-id="2a950-123">Especifica si se empezarán a eliminar las cuentas cuando no se haya iniciado sesión durante el período especificado, expresado como número de días.</span><span class="sxs-lookup"><span data-stu-id="2a950-123">Specifies when the accounts will start being deleted when they have not been logged on during the specified period, given as number of days.</span></span> <span data-ttu-id="2a950-124">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="2a950-124">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span>|
|<span data-ttu-id="2a950-125">removeAccountsBelowDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="2a950-125">removeAccountsBelowDiskFreePercentage</span></span>|<span data-ttu-id="2a950-126">Int32</span><span class="sxs-lookup"><span data-stu-id="2a950-126">Int32</span></span>|<span data-ttu-id="2a950-127">Establece el porcentaje de espacio en disco restante en un equipo antes de que se eliminen las cuentas en caché para liberar espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="2a950-127">Sets the percentage of disk space remaining on a PC before cached accounts will be deleted to free disk space.</span></span> <span data-ttu-id="2a950-128">Las cuentas que hayan estado inactivas más tiempo se eliminarán en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="2a950-128">Accounts that have been inactive the longest will be deleted first.</span></span> <span data-ttu-id="2a950-129">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="2a950-129">Only applies when AccountDeletionPolicy is DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="2a950-130">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="2a950-130">Valid values 0 to 100</span></span>|

## <a name="relationships"></a><span data-ttu-id="2a950-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2a950-131">Relationships</span></span>
<span data-ttu-id="2a950-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2a950-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2a950-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2a950-133">JSON Representation</span></span>
<span data-ttu-id="2a950-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2a950-134">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.sharedPCAccountManagerPolicy",
  "accountDeletionPolicy": "String",
  "cacheAccountsAboveDiskFreePercentage": 1024,
  "inactiveThresholdDays": 1024,
  "removeAccountsBelowDiskFreePercentage": 1024
}
```



