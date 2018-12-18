---
title: Tipo de recurso sharedPCAccountManagerPolicy
description: Directiva de administrador de cuentas de PC compartido. Solo se aplica cuando el administrador de cuentas está activado.
author: tfitzmac
ms.openlocfilehash: f41efe5c3f1dc033d25df7f931ff860d6c27de70
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27312227"
---
# <a name="sharedpcaccountmanagerpolicy-resource-type"></a><span data-ttu-id="ea66d-104">Tipo de recurso sharedPCAccountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="ea66d-104">sharedPCAccountManagerPolicy resource type</span></span>

> <span data-ttu-id="ea66d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ea66d-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ea66d-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ea66d-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ea66d-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea66d-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea66d-108">Directiva de administrador de cuentas de PC compartido.</span><span class="sxs-lookup"><span data-stu-id="ea66d-108">SharedPC Account Manager Policy.</span></span> <span data-ttu-id="ea66d-109">Solo se aplica cuando el administrador de cuentas está activado.</span><span class="sxs-lookup"><span data-stu-id="ea66d-109">Only applies when the account manager is enabled.</span></span>
## <a name="properties"></a><span data-ttu-id="ea66d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea66d-110">Properties</span></span>
|<span data-ttu-id="ea66d-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea66d-111">Property</span></span>|<span data-ttu-id="ea66d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea66d-112">Type</span></span>|<span data-ttu-id="ea66d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea66d-113">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ea66d-114">accountDeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="ea66d-114">accountDeletionPolicy</span></span>|[<span data-ttu-id="ea66d-115">sharedPCAccountDeletionPolicyType</span><span class="sxs-lookup"><span data-stu-id="ea66d-115">sharedPCAccountDeletionPolicyType</span></span>](../resources/intune-deviceconfig-sharedpcaccountdeletionpolicytype.md)|<span data-ttu-id="ea66d-116">Configura cuándo se eliminan las cuentas.</span><span class="sxs-lookup"><span data-stu-id="ea66d-116">Configures when accounts are deleted.</span></span> <span data-ttu-id="ea66d-117">Los valores posibles son: `immediate`, `diskSpaceThreshold` y `diskSpaceThresholdOrInactiveThreshold`.</span><span class="sxs-lookup"><span data-stu-id="ea66d-117">Possible values are: `immediate`, `diskSpaceThreshold`, `diskSpaceThresholdOrInactiveThreshold`.</span></span>|
|<span data-ttu-id="ea66d-118">cacheAccountsAboveDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="ea66d-118">cacheAccountsAboveDiskFreePercentage</span></span>|<span data-ttu-id="ea66d-119">Int32</span><span class="sxs-lookup"><span data-stu-id="ea66d-119">Int32</span></span>|<span data-ttu-id="ea66d-120">Establece el porcentaje de espacio en disco disponible que debería tener un equipo antes de detener la eliminación de cuentas de equipo compartido en caché.</span><span class="sxs-lookup"><span data-stu-id="ea66d-120">Sets the percentage of available disk space a PC should have before it stops deleting cached shared PC accounts.</span></span> <span data-ttu-id="ea66d-121">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="ea66d-121">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="ea66d-122">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="ea66d-122">Valid values 0 to 100</span></span>|
|<span data-ttu-id="ea66d-123">inactiveThresholdDays</span><span class="sxs-lookup"><span data-stu-id="ea66d-123">inactiveThresholdDays</span></span>|<span data-ttu-id="ea66d-124">Int32</span><span class="sxs-lookup"><span data-stu-id="ea66d-124">Int32</span></span>|<span data-ttu-id="ea66d-125">Especifica si se empezarán a eliminar las cuentas cuando no se haya iniciado sesión durante el período especificado, expresado como número de días.</span><span class="sxs-lookup"><span data-stu-id="ea66d-125">Specifies when the accounts will start being deleted when they have not been logged on during the specified period, given as number of days.</span></span> <span data-ttu-id="ea66d-126">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="ea66d-126">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span>|
|<span data-ttu-id="ea66d-127">removeAccountsBelowDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="ea66d-127">removeAccountsBelowDiskFreePercentage</span></span>|<span data-ttu-id="ea66d-128">Int32</span><span class="sxs-lookup"><span data-stu-id="ea66d-128">Int32</span></span>|<span data-ttu-id="ea66d-129">Establece el porcentaje de espacio en disco restante en un equipo antes de que se eliminen las cuentas en caché para liberar espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="ea66d-129">Sets the percentage of disk space remaining on a PC before cached accounts will be deleted to free disk space.</span></span> <span data-ttu-id="ea66d-130">Las cuentas que hayan estado inactivas más tiempo se eliminarán en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="ea66d-130">Accounts that have been inactive the longest will be deleted first.</span></span> <span data-ttu-id="ea66d-131">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="ea66d-131">Only applies when AccountDeletionPolicy is DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="ea66d-132">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="ea66d-132">Valid values 0 to 100</span></span>|

## <a name="relationships"></a><span data-ttu-id="ea66d-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ea66d-133">Relationships</span></span>
<span data-ttu-id="ea66d-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ea66d-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ea66d-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ea66d-135">JSON Representation</span></span>
<span data-ttu-id="ea66d-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ea66d-136">Here is a JSON representation of the resource.</span></span>
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





