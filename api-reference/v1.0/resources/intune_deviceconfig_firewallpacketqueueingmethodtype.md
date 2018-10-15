# <a name="firewallpacketqueueingmethodtype-enum-type"></a><span data-ttu-id="d97e2-101">Tipo de enumeración firewallPacketQueueingMethodType</span><span class="sxs-lookup"><span data-stu-id="d97e2-101">firewallPacketQueueingMethodType enum type</span></span>

> <span data-ttu-id="d97e2-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d97e2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d97e2-103">Valores posibles para firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="d97e2-103">Possible values for firewallPacketQueueingMethod</span></span>
## <a name="members"></a><span data-ttu-id="d97e2-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="d97e2-104">Members</span></span>
|<span data-ttu-id="d97e2-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="d97e2-105">Member</span></span>|<span data-ttu-id="d97e2-106">Valor</span><span class="sxs-lookup"><span data-stu-id="d97e2-106">Value</span></span>|<span data-ttu-id="d97e2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d97e2-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d97e2-108">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="d97e2-108">deviceDefault</span></span>|<span data-ttu-id="d97e2-109">0</span><span class="sxs-lookup"><span data-stu-id="d97e2-109">0%</span></span>|<span data-ttu-id="d97e2-110">No hay ningún valor configurado por Intune, no invalide el valor predeterminado del dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="d97e2-110">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="d97e2-111">disabled</span><span class="sxs-lookup"><span data-stu-id="d97e2-111">disabled</span></span>|<span data-ttu-id="d97e2-112">1</span><span class="sxs-lookup"><span data-stu-id="d97e2-112">-1</span></span>|<span data-ttu-id="d97e2-113">Deshabilitar la puesta en cola de paquetes</span><span class="sxs-lookup"><span data-stu-id="d97e2-113">Disable packet queuing</span></span>|
|<span data-ttu-id="d97e2-114">queueInbound</span><span class="sxs-lookup"><span data-stu-id="d97e2-114">queueInbound</span></span>|<span data-ttu-id="d97e2-115">2</span><span class="sxs-lookup"><span data-stu-id="d97e2-115">-2</span></span>|<span data-ttu-id="d97e2-116">Poner en cola los paquetes cifrados entrantes</span><span class="sxs-lookup"><span data-stu-id="d97e2-116">Queue inbound encrypted packets</span></span>|
|<span data-ttu-id="d97e2-117">queueOutbound</span><span class="sxs-lookup"><span data-stu-id="d97e2-117">queueOutbound</span></span>|<span data-ttu-id="d97e2-118">3</span><span class="sxs-lookup"><span data-stu-id="d97e2-118">-3</span></span>|<span data-ttu-id="d97e2-119">Poner en cola los paquetes salientes descifrados para reenviarlos</span><span class="sxs-lookup"><span data-stu-id="d97e2-119">Queue decrypted outbound packets for forwarding</span></span>|
|<span data-ttu-id="d97e2-120">queueBoth</span><span class="sxs-lookup"><span data-stu-id="d97e2-120">queueBoth</span></span>|<span data-ttu-id="d97e2-121">4</span><span class="sxs-lookup"><span data-stu-id="d97e2-121">-4</span></span>|<span data-ttu-id="d97e2-122">Poner en cola los paquetes entrantes y salientes</span><span class="sxs-lookup"><span data-stu-id="d97e2-122">Queue both inbound and outbound packets</span></span>|








