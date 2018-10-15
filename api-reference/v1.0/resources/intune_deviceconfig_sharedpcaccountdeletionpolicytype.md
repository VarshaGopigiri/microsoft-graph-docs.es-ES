# <a name="sharedpcaccountdeletionpolicytype-enum-type"></a><span data-ttu-id="2a03d-101">Tipo de enumeración sharedPCAccountDeletionPolicyType</span><span class="sxs-lookup"><span data-stu-id="2a03d-101">sharedPCAccountDeletionPolicyType enum type</span></span>

> <span data-ttu-id="2a03d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2a03d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2a03d-103">Valores posibles para cuando se eliminan cuentas en un PC compartido.</span><span class="sxs-lookup"><span data-stu-id="2a03d-103">Possible values for when accounts are deleted on a shared PC.</span></span>
## <a name="members"></a><span data-ttu-id="2a03d-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="2a03d-104">Members</span></span>
|<span data-ttu-id="2a03d-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="2a03d-105">Member</span></span>|<span data-ttu-id="2a03d-106">Valor</span><span class="sxs-lookup"><span data-stu-id="2a03d-106">Value</span></span>|<span data-ttu-id="2a03d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a03d-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2a03d-108">immediate</span><span class="sxs-lookup"><span data-stu-id="2a03d-108">   [-immediate]</span></span>|<span data-ttu-id="2a03d-109">0</span><span class="sxs-lookup"><span data-stu-id="2a03d-109">0%</span></span>|<span data-ttu-id="2a03d-110">Eliminar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="2a03d-110">Delete immediately.</span></span>|
|<span data-ttu-id="2a03d-111">diskSpaceThreshold</span><span class="sxs-lookup"><span data-stu-id="2a03d-111">diskSpaceThreshold</span></span>|<span data-ttu-id="2a03d-112">1</span><span class="sxs-lookup"><span data-stu-id="2a03d-112">-1</span></span>|<span data-ttu-id="2a03d-113">Eliminar en el umbral de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="2a03d-113">Delete at disk space threshold.</span></span>|
|<span data-ttu-id="2a03d-114">diskSpaceThresholdOrInactiveThreshold</span><span class="sxs-lookup"><span data-stu-id="2a03d-114">diskSpaceThresholdOrInactiveThreshold</span></span>|<span data-ttu-id="2a03d-115">2</span><span class="sxs-lookup"><span data-stu-id="2a03d-115">-2</span></span>|<span data-ttu-id="2a03d-116">Eliminar en el umbral de espacio en disco o umbral inactivo.</span><span class="sxs-lookup"><span data-stu-id="2a03d-116">Delete at disk space threshold or inactive threshold.</span></span>|








