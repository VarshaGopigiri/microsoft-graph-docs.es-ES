# <a name="managedappclipboardsharinglevel-enum-type"></a><span data-ttu-id="6e714-101">Tipo de enumeración managedAppClipboardSharingLevel</span><span class="sxs-lookup"><span data-stu-id="6e714-101">managedAppClipboardSharingLevel enum type</span></span>

> <span data-ttu-id="6e714-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6e714-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6e714-103">Representa el nivel al que el portapapeles del dispositivo puede compartirse entre aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6e714-103">The level to which the clipboard may be shared between apps on the managed device.</span></span>
## <a name="members"></a><span data-ttu-id="6e714-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e714-104">Members</span></span>
|<span data-ttu-id="6e714-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="6e714-105">Member</span></span>|<span data-ttu-id="6e714-106">Valor</span><span class="sxs-lookup"><span data-stu-id="6e714-106">Value</span></span>|<span data-ttu-id="6e714-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e714-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6e714-108">allApps</span><span class="sxs-lookup"><span data-stu-id="6e714-108">allApps</span></span>|<span data-ttu-id="6e714-109">0</span><span class="sxs-lookup"><span data-stu-id="6e714-109">0%</span></span>|<span data-ttu-id="6e714-110">Se permite el uso compartido entre todas las aplicaciones, administradas o no.</span><span class="sxs-lookup"><span data-stu-id="6e714-110">Sharing is allowed between all apps, managed or not</span></span>|
|<span data-ttu-id="6e714-111">managedAppsWithPasteIn</span><span class="sxs-lookup"><span data-stu-id="6e714-111">managedAppsWithPasteIn</span></span>|<span data-ttu-id="6e714-112">1</span><span class="sxs-lookup"><span data-stu-id="6e714-112">-1</span></span>|<span data-ttu-id="6e714-113">Se permite el uso compartido entre todas las aplicaciones administradas con pegar en habilitado</span><span class="sxs-lookup"><span data-stu-id="6e714-113">Sharing is allowed between all managed apps with paste in enabled</span></span>|
|<span data-ttu-id="6e714-114">managedApps</span><span class="sxs-lookup"><span data-stu-id="6e714-114">managedApps</span></span>|<span data-ttu-id="6e714-115">2</span><span class="sxs-lookup"><span data-stu-id="6e714-115">-2</span></span>|<span data-ttu-id="6e714-116">Se permite el uso compartido entre todas las aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="6e714-116">Sharing is allowed between all managed apps</span></span>|
|<span data-ttu-id="6e714-117">blocked</span><span class="sxs-lookup"><span data-stu-id="6e714-117">blocked</span></span>|<span data-ttu-id="6e714-118">3</span><span class="sxs-lookup"><span data-stu-id="6e714-118">-3</span></span>|<span data-ttu-id="6e714-119">El uso compartido entre aplicaciones está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="6e714-119">Sharing between apps is disabled</span></span>|








