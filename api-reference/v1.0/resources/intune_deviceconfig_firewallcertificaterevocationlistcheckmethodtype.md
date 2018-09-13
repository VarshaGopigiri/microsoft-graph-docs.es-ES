# <a name="firewallcertificaterevocationlistcheckmethodtype-enum-type"></a><span data-ttu-id="86846-101">Tipo de enumeración firewallCertificateRevocationListCheckMethodType</span><span class="sxs-lookup"><span data-stu-id="86846-101">firewallCertificateRevocationListCheckMethodType enum type</span></span>

> <span data-ttu-id="86846-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="86846-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="86846-103">Valores posibles para firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="86846-103">Possible values for firewallCertificateRevocationListCheckMethod</span></span>
## <a name="members"></a><span data-ttu-id="86846-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="86846-104">Members</span></span>
|<span data-ttu-id="86846-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="86846-105">Member</span></span>|<span data-ttu-id="86846-106">Valor</span><span class="sxs-lookup"><span data-stu-id="86846-106">Value</span></span>|<span data-ttu-id="86846-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="86846-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="86846-108">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="86846-108">deviceDefault</span></span>|<span data-ttu-id="86846-109">0</span><span class="sxs-lookup"><span data-stu-id="86846-109">0%</span></span>|<span data-ttu-id="86846-110">No hay ningún valor configurado por Intune, no invalidar el valor predeterminado del dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="86846-110">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="86846-111">none</span><span class="sxs-lookup"><span data-stu-id="86846-111">none</span></span>|<span data-ttu-id="86846-112">1</span><span class="sxs-lookup"><span data-stu-id="86846-112">-1</span></span>|<span data-ttu-id="86846-113">No comprobar la lista de revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="86846-113">Do not check certificate revocation list</span></span>|
|<span data-ttu-id="86846-114">attempt</span><span class="sxs-lookup"><span data-stu-id="86846-114">attempt</span></span>|<span data-ttu-id="86846-115">2</span><span class="sxs-lookup"><span data-stu-id="86846-115">-2</span></span>|<span data-ttu-id="86846-116">Intentar la comprobación de CRL y permitir un certificado solo si el certificado se confirma mediante la comprobación</span><span class="sxs-lookup"><span data-stu-id="86846-116">Attempt CRL check and allow a certificate only if the certificate is confirmed by the check</span></span>|
|<span data-ttu-id="86846-117">require</span><span class="sxs-lookup"><span data-stu-id="86846-117">Require</span></span>|<span data-ttu-id="86846-118">2</span><span class="sxs-lookup"><span data-stu-id="86846-118">-3</span></span>|<span data-ttu-id="86846-119">Requerir una comprobación de CRL correcta antes de permitir un certificado</span><span class="sxs-lookup"><span data-stu-id="86846-119">Require a successful CRL check before allowing a certificate</span></span>|








