# <a name="firewallpresharedkeyencodingmethodtype-enum-type"></a><span data-ttu-id="68492-101">tipo de enumeración firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="68492-101">firewallPreSharedKeyEncodingMethodType enum type</span></span>

> <span data-ttu-id="68492-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="68492-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="68492-103">Valores posibles para firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="68492-103">Possible values for firewallPreSharedKeyEncodingMethod</span></span>
## <a name="members"></a><span data-ttu-id="68492-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="68492-104">Members</span></span>
|<span data-ttu-id="68492-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="68492-105">Member</span></span>|<span data-ttu-id="68492-106">Valor</span><span class="sxs-lookup"><span data-stu-id="68492-106">Value</span></span>|<span data-ttu-id="68492-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="68492-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="68492-108">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="68492-108">deviceDefault</span></span>|<span data-ttu-id="68492-109">0</span><span class="sxs-lookup"><span data-stu-id="68492-109">0%</span></span>|<span data-ttu-id="68492-110">No hay ningún valor configurado por Intune, no se invalida el valor predeterminado del dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="68492-110">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="68492-111">none</span><span class="sxs-lookup"><span data-stu-id="68492-111">none</span></span>|<span data-ttu-id="68492-112">1</span><span class="sxs-lookup"><span data-stu-id="68492-112">-1</span></span>|<span data-ttu-id="68492-113">No se ha codificado una clave previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="68492-113">Preshared key is not encoded.</span></span> <span data-ttu-id="68492-114">En su lugar, se ha mantenido en el formato de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="68492-114">Instead, it is kept in its wide-character format</span></span>|
|<span data-ttu-id="68492-115">utF8</span><span class="sxs-lookup"><span data-stu-id="68492-115">utf-8</span></span>|<span data-ttu-id="68492-116">2</span><span class="sxs-lookup"><span data-stu-id="68492-116">-2</span></span>|<span data-ttu-id="68492-117">Codifica la clave previamente compartida con UTF-8</span><span class="sxs-lookup"><span data-stu-id="68492-117">Encode the preshared key using UTF-8</span></span>|








