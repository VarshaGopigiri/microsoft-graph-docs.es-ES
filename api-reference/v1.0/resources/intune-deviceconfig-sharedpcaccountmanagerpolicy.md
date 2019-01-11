---
title: Tipo de recurso sharedPCAccountManagerPolicy
description: Directiva de administrador de cuentas de PC compartido. Solo se aplica cuando el administrador de cuentas está activado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4597d4bc6fd818bc0437a3ad3675c2aa5683ec61
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815683"
---
# <a name="sharedpcaccountmanagerpolicy-resource-type"></a><span data-ttu-id="a7d47-104">Tipo de recurso sharedPCAccountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="a7d47-104">sharedPCAccountManagerPolicy resource type</span></span>

> <span data-ttu-id="a7d47-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a7d47-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a7d47-106">Directiva de administrador de cuentas de PC compartido.</span><span class="sxs-lookup"><span data-stu-id="a7d47-106">SharedPC Account Manager Policy.</span></span> <span data-ttu-id="a7d47-107">Solo se aplica cuando el administrador de cuentas está activado.</span><span class="sxs-lookup"><span data-stu-id="a7d47-107">Only applies when the account manager is enabled.</span></span>
## <a name="properties"></a><span data-ttu-id="a7d47-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7d47-108">Properties</span></span>
|<span data-ttu-id="a7d47-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7d47-109">Property</span></span>|<span data-ttu-id="a7d47-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7d47-110">Type</span></span>|<span data-ttu-id="a7d47-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7d47-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a7d47-112">accountDeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7d47-112">accountDeletionPolicy</span></span>|[<span data-ttu-id="a7d47-113">sharedPCAccountDeletionPolicyType</span><span class="sxs-lookup"><span data-stu-id="a7d47-113">sharedPCAccountDeletionPolicyType</span></span>](../resources/intune-deviceconfig-sharedpcaccountdeletionpolicytype.md)|<span data-ttu-id="a7d47-114">Configura cuándo se eliminan las cuentas.</span><span class="sxs-lookup"><span data-stu-id="a7d47-114">Configures when accounts are deleted.</span></span> <span data-ttu-id="a7d47-115">Los valores posibles son: `immediate`, `diskSpaceThreshold` y `diskSpaceThresholdOrInactiveThreshold`.</span><span class="sxs-lookup"><span data-stu-id="a7d47-115">Possible values are: `immediate`, `diskSpaceThreshold`, `diskSpaceThresholdOrInactiveThreshold`.</span></span>|
|<span data-ttu-id="a7d47-116">cacheAccountsAboveDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="a7d47-116">cacheAccountsAboveDiskFreePercentage</span></span>|<span data-ttu-id="a7d47-117">Int32</span><span class="sxs-lookup"><span data-stu-id="a7d47-117">Int32</span></span>|<span data-ttu-id="a7d47-118">Establece el porcentaje de espacio en disco disponible que debería tener un equipo antes de detener la eliminación de cuentas de equipo compartido en caché.</span><span class="sxs-lookup"><span data-stu-id="a7d47-118">Sets the percentage of available disk space a PC should have before it stops deleting cached shared PC accounts.</span></span> <span data-ttu-id="a7d47-119">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="a7d47-119">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="a7d47-120">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="a7d47-120">Valid values 0 to 100</span></span>|
|<span data-ttu-id="a7d47-121">inactiveThresholdDays</span><span class="sxs-lookup"><span data-stu-id="a7d47-121">inactiveThresholdDays</span></span>|<span data-ttu-id="a7d47-122">Int32</span><span class="sxs-lookup"><span data-stu-id="a7d47-122">Int32</span></span>|<span data-ttu-id="a7d47-123">Especifica si se empezarán a eliminar las cuentas cuando no se haya iniciado sesión durante el período especificado, expresado como número de días.</span><span class="sxs-lookup"><span data-stu-id="a7d47-123">Specifies when the accounts will start being deleted when they have not been logged on during the specified period, given as number of days.</span></span> <span data-ttu-id="a7d47-124">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="a7d47-124">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span>|
|<span data-ttu-id="a7d47-125">removeAccountsBelowDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="a7d47-125">removeAccountsBelowDiskFreePercentage</span></span>|<span data-ttu-id="a7d47-126">Int32</span><span class="sxs-lookup"><span data-stu-id="a7d47-126">Int32</span></span>|<span data-ttu-id="a7d47-127">Establece el porcentaje de espacio en disco restante en un equipo antes de que se eliminen las cuentas en caché para liberar espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="a7d47-127">Sets the percentage of disk space remaining on a PC before cached accounts will be deleted to free disk space.</span></span> <span data-ttu-id="a7d47-128">Las cuentas que hayan estado inactivas más tiempo se eliminarán en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="a7d47-128">Accounts that have been inactive the longest will be deleted first.</span></span> <span data-ttu-id="a7d47-129">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="a7d47-129">Only applies when AccountDeletionPolicy is DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="a7d47-130">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="a7d47-130">Valid values 0 to 100</span></span>|

## <a name="relationships"></a><span data-ttu-id="a7d47-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a7d47-131">Relationships</span></span>
<span data-ttu-id="a7d47-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a7d47-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a7d47-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a7d47-133">JSON Representation</span></span>
<span data-ttu-id="a7d47-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a7d47-134">Here is a JSON representation of the resource.</span></span>
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



