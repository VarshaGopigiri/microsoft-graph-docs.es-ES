# <a name="compliancestate-enum-type"></a><span data-ttu-id="f384a-101">Tipo de enumeración complianceState</span><span class="sxs-lookup"><span data-stu-id="f384a-101">complianceState enum type</span></span>

> <span data-ttu-id="f384a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f384a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f384a-103">Estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f384a-103">Compliance state.</span></span>
## <a name="members"></a><span data-ttu-id="f384a-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="f384a-104">Members</span></span>
|<span data-ttu-id="f384a-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="f384a-105">Member</span></span>|<span data-ttu-id="f384a-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f384a-106">Value</span></span>|<span data-ttu-id="f384a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f384a-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f384a-108">unknown</span><span class="sxs-lookup"><span data-stu-id="f384a-108">unknown</span></span>|<span data-ttu-id="f384a-109">0</span><span class="sxs-lookup"><span data-stu-id="f384a-109">0%</span></span>|<span data-ttu-id="f384a-110">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="f384a-110">Unknown</span></span>|
|<span data-ttu-id="f384a-111">compliant</span><span class="sxs-lookup"><span data-stu-id="f384a-111">Compliant</span></span>|<span data-ttu-id="f384a-112">1</span><span class="sxs-lookup"><span data-stu-id="f384a-112">-1</span></span>|<span data-ttu-id="f384a-113">Compatible.</span><span class="sxs-lookup"><span data-stu-id="f384a-113">Compliant</span></span>|
|<span data-ttu-id="f384a-114">nonCompliant</span><span class="sxs-lookup"><span data-stu-id="f384a-114">noncompliant</span></span>|<span data-ttu-id="f384a-115">2</span><span class="sxs-lookup"><span data-stu-id="f384a-115">-2</span></span>|<span data-ttu-id="f384a-116">El dispositivo no es compatible y está bloqueado para acceder a los recursos corporativos.</span><span class="sxs-lookup"><span data-stu-id="f384a-116">Device is non-compliant and is blocked from corporate resources.</span></span>|
|<span data-ttu-id="f384a-117">conflict</span><span class="sxs-lookup"><span data-stu-id="f384a-117">Conflict</span></span>|<span data-ttu-id="f384a-118">3</span><span class="sxs-lookup"><span data-stu-id="f384a-118">-3</span></span>|<span data-ttu-id="f384a-119">Conflicto con otras reglas.</span><span class="sxs-lookup"><span data-stu-id="f384a-119">Conflict with other rules.</span></span>|
|<span data-ttu-id="f384a-120">error</span><span class="sxs-lookup"><span data-stu-id="f384a-120">error</span></span>|<span data-ttu-id="f384a-121">4</span><span class="sxs-lookup"><span data-stu-id="f384a-121">-4</span></span>|<span data-ttu-id="f384a-122">Error.</span><span class="sxs-lookup"><span data-stu-id="f384a-122">Error.</span></span>|
|<span data-ttu-id="f384a-123">inGracePeriod</span><span class="sxs-lookup"><span data-stu-id="f384a-123">inGracePeriod</span></span>|<span data-ttu-id="f384a-124">254</span><span class="sxs-lookup"><span data-stu-id="f384a-124">254</span></span>|<span data-ttu-id="f384a-125">El dispositivo no es compatible pero tiene acceso a recursos corporativos.</span><span class="sxs-lookup"><span data-stu-id="f384a-125">Device is non-compliant but still has access to corporate resources</span></span>|
|<span data-ttu-id="f384a-126">configManager</span><span class="sxs-lookup"><span data-stu-id="f384a-126">configManager</span></span>|<span data-ttu-id="f384a-127">255</span><span class="sxs-lookup"><span data-stu-id="f384a-127">255 characters</span></span>|<span data-ttu-id="f384a-128">Administrado por el administrador de configuraciones.</span><span class="sxs-lookup"><span data-stu-id="f384a-128">Managed by Config Manager</span></span>|








