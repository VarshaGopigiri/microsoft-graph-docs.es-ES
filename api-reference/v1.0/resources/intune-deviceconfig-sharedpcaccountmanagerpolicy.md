---
title: Tipo de recurso sharedPCAccountManagerPolicy
description: Directiva de administrador de cuentas de PC compartido. Solo se aplica cuando el administrador de cuentas está activado.
ms.openlocfilehash: 72616fbecd20ab43db6aafcb9ecbce00530cb4db
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032663"
---
# <a name="sharedpcaccountmanagerpolicy-resource-type"></a><span data-ttu-id="83b40-104">Tipo de recurso sharedPCAccountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="83b40-104">sharedPCAccountManagerPolicy resource type</span></span>

> <span data-ttu-id="83b40-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="83b40-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="83b40-106">Directiva de administrador de cuentas de PC compartido.</span><span class="sxs-lookup"><span data-stu-id="83b40-106">SharedPC Account Manager Policy.</span></span> <span data-ttu-id="83b40-107">Solo se aplica cuando el administrador de cuentas está activado.</span><span class="sxs-lookup"><span data-stu-id="83b40-107">Only applies when the account manager is enabled.</span></span>
## <a name="properties"></a><span data-ttu-id="83b40-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83b40-108">Properties</span></span>
|<span data-ttu-id="83b40-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="83b40-109">Property</span></span>|<span data-ttu-id="83b40-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="83b40-110">Type</span></span>|<span data-ttu-id="83b40-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="83b40-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="83b40-112">accountDeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="83b40-112">accountDeletionPolicy</span></span>|[<span data-ttu-id="83b40-113">sharedPCAccountDeletionPolicyType</span><span class="sxs-lookup"><span data-stu-id="83b40-113">sharedPCAccountDeletionPolicyType</span></span>](../resources/intune-deviceconfig-sharedpcaccountdeletionpolicytype.md)|<span data-ttu-id="83b40-114">Configura cuándo se eliminan las cuentas.</span><span class="sxs-lookup"><span data-stu-id="83b40-114">Configures when accounts are deleted.</span></span> <span data-ttu-id="83b40-115">Los valores posibles son: `immediate`, `diskSpaceThreshold` y `diskSpaceThresholdOrInactiveThreshold`.</span><span class="sxs-lookup"><span data-stu-id="83b40-115">Possible values are: `immediate`, `diskSpaceThreshold`, `diskSpaceThresholdOrInactiveThreshold`.</span></span>|
|<span data-ttu-id="83b40-116">cacheAccountsAboveDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="83b40-116">cacheAccountsAboveDiskFreePercentage</span></span>|<span data-ttu-id="83b40-117">Int32</span><span class="sxs-lookup"><span data-stu-id="83b40-117">Int32</span></span>|<span data-ttu-id="83b40-118">Establece el porcentaje de espacio en disco disponible que debería tener un equipo antes de detener la eliminación de cuentas de equipo compartido en caché.</span><span class="sxs-lookup"><span data-stu-id="83b40-118">Sets the percentage of available disk space a PC should have before it stops deleting cached shared PC accounts.</span></span> <span data-ttu-id="83b40-119">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="83b40-119">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="83b40-120">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="83b40-120">Valid values 0 to 100</span></span>|
|<span data-ttu-id="83b40-121">inactiveThresholdDays</span><span class="sxs-lookup"><span data-stu-id="83b40-121">inactiveThresholdDays</span></span>|<span data-ttu-id="83b40-122">Int32</span><span class="sxs-lookup"><span data-stu-id="83b40-122">Int32</span></span>|<span data-ttu-id="83b40-123">Especifica si se empezarán a eliminar las cuentas cuando no se haya iniciado sesión durante el período especificado, expresado como número de días.</span><span class="sxs-lookup"><span data-stu-id="83b40-123">Specifies when the accounts will start being deleted when they have not been logged on during the specified period, given as number of days.</span></span> <span data-ttu-id="83b40-124">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="83b40-124">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span>|
|<span data-ttu-id="83b40-125">removeAccountsBelowDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="83b40-125">removeAccountsBelowDiskFreePercentage</span></span>|<span data-ttu-id="83b40-126">Int32</span><span class="sxs-lookup"><span data-stu-id="83b40-126">Int32</span></span>|<span data-ttu-id="83b40-127">Establece el porcentaje de espacio en disco restante en un equipo antes de que se eliminen las cuentas en caché para liberar espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="83b40-127">Sets the percentage of disk space remaining on a PC before cached accounts will be deleted to free disk space.</span></span> <span data-ttu-id="83b40-128">Las cuentas que hayan estado inactivas más tiempo se eliminarán en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="83b40-128">Accounts that have been inactive the longest will be deleted first.</span></span> <span data-ttu-id="83b40-129">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="83b40-129">Only applies when AccountDeletionPolicy is DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="83b40-130">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="83b40-130">Valid values 0 to 100</span></span>|

## <a name="relationships"></a><span data-ttu-id="83b40-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="83b40-131">Relationships</span></span>
<span data-ttu-id="83b40-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="83b40-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="83b40-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="83b40-133">JSON Representation</span></span>
<span data-ttu-id="83b40-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="83b40-134">Here is a JSON representation of the resource.</span></span>
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



