# <a name="applicationguardblockclipboardsharingtype-enum-type"></a><span data-ttu-id="bc941-101">Tipo de enumeración applicationGuardBlockClipboardSharingType</span><span class="sxs-lookup"><span data-stu-id="bc941-101">applicationGuardBlockClipboardSharingType enum type</span></span>

> <span data-ttu-id="bc941-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bc941-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bc941-103">Valores posibles para applicationGuardBlockClipboardSharingType</span><span class="sxs-lookup"><span data-stu-id="bc941-103">Possible values for applicationGuardBlockClipboardSharingType</span></span>
## <a name="members"></a><span data-ttu-id="bc941-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="bc941-104">Members</span></span>
|<span data-ttu-id="bc941-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="bc941-105">Member</span></span>|<span data-ttu-id="bc941-106">Valor</span><span class="sxs-lookup"><span data-stu-id="bc941-106">Value</span></span>|<span data-ttu-id="bc941-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc941-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bc941-108">notConfigured</span><span class="sxs-lookup"><span data-stu-id="bc941-108">notConfigured</span></span>|<span data-ttu-id="bc941-109">0</span><span class="sxs-lookup"><span data-stu-id="bc941-109">0%</span></span>|<span data-ttu-id="bc941-110">No configurado.</span><span class="sxs-lookup"><span data-stu-id="bc941-110">Not configured</span></span>|
|<span data-ttu-id="bc941-111">blockBoth</span><span class="sxs-lookup"><span data-stu-id="bc941-111">blockBoth</span></span>|<span data-ttu-id="bc941-112">1</span><span class="sxs-lookup"><span data-stu-id="bc941-112">-1</span></span>|<span data-ttu-id="bc941-113">Impide que el Portapapeles comparta los datos del host al contenedor y del contenedor al host</span><span class="sxs-lookup"><span data-stu-id="bc941-113">Block clipboard to share data from Host to Container, or from Container to Host, or both ways, or neither ways.</span></span>|
|<span data-ttu-id="bc941-114">blockHostToContainer</span><span class="sxs-lookup"><span data-stu-id="bc941-114">blockHostToContainer</span></span>|<span data-ttu-id="bc941-115">2</span><span class="sxs-lookup"><span data-stu-id="bc941-115">-2</span></span>|<span data-ttu-id="bc941-116">Impide que el Portapapeles comparta los datos del host al contenedor.</span><span class="sxs-lookup"><span data-stu-id="bc941-116">Block clipboard to share data from Host to Container, or from Container to Host, or both ways, or neither ways.</span></span>|
|<span data-ttu-id="bc941-117">blockContainerToHost</span><span class="sxs-lookup"><span data-stu-id="bc941-117">blockContainerToHost</span></span>|<span data-ttu-id="bc941-118">3</span><span class="sxs-lookup"><span data-stu-id="bc941-118">-3</span></span>|<span data-ttu-id="bc941-119">Impide que el Portapapeles comparta los datos del contenedor al host.</span><span class="sxs-lookup"><span data-stu-id="bc941-119">Block clipboard to share data from Host to Container, or from Container to Host, or both ways, or neither ways.</span></span>|
|<span data-ttu-id="bc941-120">blockNone</span><span class="sxs-lookup"><span data-stu-id="bc941-120">blockNone</span></span>|<span data-ttu-id="bc941-121">4</span><span class="sxs-lookup"><span data-stu-id="bc941-121">-4</span></span>|<span data-ttu-id="bc941-122">Impide que el Portapapeles comparta los datos del host al contenedor y del contenedor al host.</span><span class="sxs-lookup"><span data-stu-id="bc941-122">Block clipboard to share data from Host to Container, or from Container to Host, or both ways, or neither ways.</span></span>|








