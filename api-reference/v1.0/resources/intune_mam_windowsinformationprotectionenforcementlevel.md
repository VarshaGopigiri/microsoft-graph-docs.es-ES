# <a name="windowsinformationprotectionenforcementlevel-enum-type"></a><span data-ttu-id="ee320-101">Tipo de enumeración windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="ee320-101">windowsInformationProtectionEnforcementLevel enum type</span></span>

> <span data-ttu-id="ee320-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ee320-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ee320-103">Valores posibles para los niveles de cumplimiento de WIP</span><span class="sxs-lookup"><span data-stu-id="ee320-103">Possible values for WIP Protection enforcement levels</span></span>
## <a name="members"></a><span data-ttu-id="ee320-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="ee320-104">Members</span></span>
|<span data-ttu-id="ee320-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="ee320-105">Member</span></span>|<span data-ttu-id="ee320-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ee320-106">Value</span></span>|<span data-ttu-id="ee320-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee320-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ee320-108">noProtection</span><span class="sxs-lookup"><span data-stu-id="ee320-108">noProtection</span></span>|<span data-ttu-id="ee320-109">0</span><span class="sxs-lookup"><span data-stu-id="ee320-109">0%</span></span>|<span data-ttu-id="ee320-110">Sin cumplimiento de protección</span><span class="sxs-lookup"><span data-stu-id="ee320-110">No protection enforcement</span></span>|
|<span data-ttu-id="ee320-111">encryptAndAuditOnly</span><span class="sxs-lookup"><span data-stu-id="ee320-111">encryptAndAuditOnly</span></span>|<span data-ttu-id="ee320-112">1</span><span class="sxs-lookup"><span data-stu-id="ee320-112">-1</span></span>|<span data-ttu-id="ee320-113">Solo cifrado y auditoría</span><span class="sxs-lookup"><span data-stu-id="ee320-113">Encrypt and Audit only</span></span>|
|<span data-ttu-id="ee320-114">encryptAuditAndPrompt</span><span class="sxs-lookup"><span data-stu-id="ee320-114">encryptAuditAndPrompt</span></span>|<span data-ttu-id="ee320-115">2</span><span class="sxs-lookup"><span data-stu-id="ee320-115">-2</span></span>|<span data-ttu-id="ee320-116">Cifrado, auditoría y solicitud de confirmación</span><span class="sxs-lookup"><span data-stu-id="ee320-116">Encrypt, Audit and Prompt</span></span>|
|<span data-ttu-id="ee320-117">encryptAuditAndBlock</span><span class="sxs-lookup"><span data-stu-id="ee320-117">encryptAuditAndBlock</span></span>|<span data-ttu-id="ee320-118">3</span><span class="sxs-lookup"><span data-stu-id="ee320-118">-3</span></span>|<span data-ttu-id="ee320-119">Cifrado, auditoría y bloqueo</span><span class="sxs-lookup"><span data-stu-id="ee320-119">Encrypt, Audit and Block</span></span>|








