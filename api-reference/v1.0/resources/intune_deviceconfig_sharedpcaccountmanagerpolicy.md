# <a name="sharedpcaccountmanagerpolicy-resource-type"></a><span data-ttu-id="7c994-101">Tipo de recurso sharedPCAccountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="7c994-101">sharedPCAccountManagerPolicy resource type</span></span>

> <span data-ttu-id="7c994-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7c994-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7c994-103">Directiva de administrador de cuentas de PC compartido.</span><span class="sxs-lookup"><span data-stu-id="7c994-103">SharedPC Account Manager Policy.</span></span> <span data-ttu-id="7c994-104">Solo se aplica cuando el administrador de cuentas está activado.</span><span class="sxs-lookup"><span data-stu-id="7c994-104">Only applies when the account manager is enabled.</span></span>
## <a name="properties"></a><span data-ttu-id="7c994-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c994-105">Properties</span></span>
|<span data-ttu-id="7c994-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c994-106">Property</span></span>|<span data-ttu-id="7c994-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c994-107">Type</span></span>|<span data-ttu-id="7c994-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c994-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7c994-109">accountDeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c994-109">accountDeletionPolicy</span></span>|[<span data-ttu-id="7c994-110">sharedPCAccountDeletionPolicyType</span><span class="sxs-lookup"><span data-stu-id="7c994-110">sharedPCAccountDeletionPolicyType</span></span>](../resources/intune_deviceconfig_sharedpcaccountdeletionpolicytype.md)|<span data-ttu-id="7c994-p102">Configura cuándo se eliminan las cuentas. Los valores posibles son: `immediate`, `diskSpaceThreshold`, `diskSpaceThresholdOrInactiveThreshold`.</span><span class="sxs-lookup"><span data-stu-id="7c994-p102">Configures when accounts are deleted. The possible values are: `immediate`, `diskSpaceThreshold`, `diskSpaceThresholdOrInactiveThreshold`.</span></span>|
|<span data-ttu-id="7c994-113">cacheAccountsAboveDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="7c994-113">cacheAccountsAboveDiskFreePercentage</span></span>|<span data-ttu-id="7c994-114">Int32</span><span class="sxs-lookup"><span data-stu-id="7c994-114">Int32</span></span>|<span data-ttu-id="7c994-115">Establece el porcentaje de espacio en disco disponible que debería tener un equipo antes de detener la eliminación de cuentas de equipo compartido en caché.</span><span class="sxs-lookup"><span data-stu-id="7c994-115">Sets the percentage of available disk space a PC should have before it stops deleting cached shared PC accounts.</span></span> <span data-ttu-id="7c994-116">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="7c994-116">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="7c994-117">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="7c994-117">Valid values 0 to 100</span></span>|
|<span data-ttu-id="7c994-118">inactiveThresholdDays</span><span class="sxs-lookup"><span data-stu-id="7c994-118">inactiveThresholdDays</span></span>|<span data-ttu-id="7c994-119">Int32</span><span class="sxs-lookup"><span data-stu-id="7c994-119">Int32</span></span>|<span data-ttu-id="7c994-120">Especifica si se empezarán a eliminar las cuentas cuando no se haya iniciado sesión durante el período especificado, expresado como número de días.</span><span class="sxs-lookup"><span data-stu-id="7c994-120">Specifies when the accounts will start being deleted when they have not been logged on during the specified period, given as number of days.</span></span> <span data-ttu-id="7c994-121">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThreshold o DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="7c994-121">Only applies when AccountDeletionPolicy is DiskSpaceThreshold or DiskSpaceThresholdOrInactiveThreshold.</span></span>|
|<span data-ttu-id="7c994-122">removeAccountsBelowDiskFreePercentage</span><span class="sxs-lookup"><span data-stu-id="7c994-122">removeAccountsBelowDiskFreePercentage</span></span>|<span data-ttu-id="7c994-123">Int32</span><span class="sxs-lookup"><span data-stu-id="7c994-123">Int32</span></span>|<span data-ttu-id="7c994-124">Establece el porcentaje de espacio en disco restante en un equipo antes de que se eliminen las cuentas en caché para liberar espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="7c994-124">Sets the percentage of disk space remaining on a PC before cached accounts will be deleted to free disk space.</span></span> <span data-ttu-id="7c994-125">Las cuentas que hayan estado inactivas más tiempo se eliminarán en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="7c994-125">Accounts that have been inactive the longest will be deleted first.</span></span> <span data-ttu-id="7c994-126">Solo se aplica cuando AccountDeletionPolicy es DiskSpaceThresholdOrInactiveThreshold.</span><span class="sxs-lookup"><span data-stu-id="7c994-126">Only applies when AccountDeletionPolicy is DiskSpaceThresholdOrInactiveThreshold.</span></span> <span data-ttu-id="7c994-127">Valores válidos de 0 a 100</span><span class="sxs-lookup"><span data-stu-id="7c994-127">Valid values 0 to 100</span></span>|

## <a name="relationships"></a><span data-ttu-id="7c994-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7c994-128">Relationships</span></span>
<span data-ttu-id="7c994-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7c994-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7c994-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7c994-130">JSON Representation</span></span>
<span data-ttu-id="7c994-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7c994-131">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.sharedPCAccountManagerPolicy",
  "accountDeletionPolicy": "String",
  "cacheAccountsAboveDiskFreePercentage": 1024,
  "inactiveThresholdDays": 1024,
  "removeAccountsBelowDiskFreePercentage": 1024
}
```








