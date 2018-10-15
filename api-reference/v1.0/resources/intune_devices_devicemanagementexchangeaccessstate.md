# <a name="devicemanagementexchangeaccessstate-enum-type"></a><span data-ttu-id="1f531-101">tipo de enumeración deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="1f531-101">deviceManagementExchangeAccessState enum type</span></span>

> <span data-ttu-id="1f531-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1f531-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1f531-103">Estado de acceso de dispositivos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1f531-103">Device Exchange Access State summary</span></span>
## <a name="members"></a><span data-ttu-id="1f531-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="1f531-104">Members</span></span>
|<span data-ttu-id="1f531-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="1f531-105">Member</span></span>|<span data-ttu-id="1f531-106">Valor</span><span class="sxs-lookup"><span data-stu-id="1f531-106">Value</span></span>|<span data-ttu-id="1f531-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f531-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1f531-108">none</span><span class="sxs-lookup"><span data-stu-id="1f531-108">none</span></span>|<span data-ttu-id="1f531-109">0</span><span class="sxs-lookup"><span data-stu-id="1f531-109">0%</span></span>|<span data-ttu-id="1f531-110">No hay ningún estado de acceso detectado desde Exchange</span><span class="sxs-lookup"><span data-stu-id="1f531-110">No access state discovered from Exchange</span></span>|
|<span data-ttu-id="1f531-111">unknown</span><span class="sxs-lookup"><span data-stu-id="1f531-111">unknown</span></span>|<span data-ttu-id="1f531-112">1</span><span class="sxs-lookup"><span data-stu-id="1f531-112">-1</span></span>|<span data-ttu-id="1f531-113">Se desconoce el estado de acceso del dispositivo a Exchange</span><span class="sxs-lookup"><span data-stu-id="1f531-113">Device access state to Exchange is unknown</span></span>|
|<span data-ttu-id="1f531-114">allowed</span><span class="sxs-lookup"><span data-stu-id="1f531-114">Allowed</span></span>|<span data-ttu-id="1f531-115">2</span><span class="sxs-lookup"><span data-stu-id="1f531-115">-2</span></span>|<span data-ttu-id="1f531-116">El dispositivo tiene acceso a Exchange</span><span class="sxs-lookup"><span data-stu-id="1f531-116">Device has access to Exchange</span></span>|
|<span data-ttu-id="1f531-117">blocked</span><span class="sxs-lookup"><span data-stu-id="1f531-117">blocked</span></span>|<span data-ttu-id="1f531-118">3</span><span class="sxs-lookup"><span data-stu-id="1f531-118">-3</span></span>|<span data-ttu-id="1f531-119">El dispositivo está bloqueado en Exchange</span><span class="sxs-lookup"><span data-stu-id="1f531-119">Device is Blocked in Exchange</span></span>|
|<span data-ttu-id="1f531-120">quarantined</span><span class="sxs-lookup"><span data-stu-id="1f531-120">quarantined</span></span>|<span data-ttu-id="1f531-121">4</span><span class="sxs-lookup"><span data-stu-id="1f531-121">-4</span></span>|<span data-ttu-id="1f531-122">El dispositivo está en cuarentena en Exchange</span><span class="sxs-lookup"><span data-stu-id="1f531-122">Device is Quarantined in Exchange</span></span>|








