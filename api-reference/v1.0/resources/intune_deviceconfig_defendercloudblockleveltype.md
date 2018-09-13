# <a name="defendercloudblockleveltype-enum-type"></a><span data-ttu-id="a1da1-101">Tipo de enumeración defenderCloudBlockLevelType</span><span class="sxs-lookup"><span data-stu-id="a1da1-101">defenderCloudBlockLevelType enum type</span></span>

> <span data-ttu-id="a1da1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a1da1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a1da1-103">Posibles valores de nivel de bloqueo en la nube</span><span class="sxs-lookup"><span data-stu-id="a1da1-103">Possible values of Cloud Block Level</span></span>
## <a name="members"></a><span data-ttu-id="a1da1-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1da1-104">Members</span></span>
|<span data-ttu-id="a1da1-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="a1da1-105">Member</span></span>|<span data-ttu-id="a1da1-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a1da1-106">Value</span></span>|<span data-ttu-id="a1da1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1da1-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a1da1-108">notConfigured</span><span class="sxs-lookup"><span data-stu-id="a1da1-108">notConfigured</span></span>|<span data-ttu-id="a1da1-109">0</span><span class="sxs-lookup"><span data-stu-id="a1da1-109">0%</span></span>|<span data-ttu-id="a1da1-110">Valor predeterminado, se utiliza el nivel de bloqueo predeterminado de Windows Defender Antivirus y se proporciona una detección segura sin aumentar el riesgo de detectar archivos legítimos.</span><span class="sxs-lookup"><span data-stu-id="a1da1-110">Default value, uses the default Windows Defender Antivirus blocking level and provides strong detection without increasing the risk of detecting legitimate files</span></span>|
|<span data-ttu-id="a1da1-111">high</span><span class="sxs-lookup"><span data-stu-id="a1da1-111">High.</span></span>|<span data-ttu-id="a1da1-112">1</span><span class="sxs-lookup"><span data-stu-id="a1da1-112">-1</span></span>|<span data-ttu-id="a1da1-113">High aplica un nivel de detección alto.</span><span class="sxs-lookup"><span data-stu-id="a1da1-113">High applies a strong level of detection.</span></span>|
|<span data-ttu-id="a1da1-114">highPlus</span><span class="sxs-lookup"><span data-stu-id="a1da1-114">highPlus</span></span>|<span data-ttu-id="a1da1-115">2</span><span class="sxs-lookup"><span data-stu-id="a1da1-115">-2</span></span>|<span data-ttu-id="a1da1-116">High + utiliza el nivel High y aplica medidas de protección adicionales.</span><span class="sxs-lookup"><span data-stu-id="a1da1-116">High + uses the High level and applies addition protection measures</span></span>|
|<span data-ttu-id="a1da1-117">zeroTolerance</span><span class="sxs-lookup"><span data-stu-id="a1da1-117">zeroTolerance</span></span>|<span data-ttu-id="a1da1-118">3</span><span class="sxs-lookup"><span data-stu-id="a1da1-118">-3</span></span>|<span data-ttu-id="a1da1-119">Zero tolerance bloquea todos los archivos ejecutables desconocidos.</span><span class="sxs-lookup"><span data-stu-id="a1da1-119">Zero tolerance blocks all unknown executables</span></span>|








