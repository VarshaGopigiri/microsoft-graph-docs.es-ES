# <a name="applisttype-enum-type"></a><span data-ttu-id="0ed55-101">Tipo de enumeración appListType</span><span class="sxs-lookup"><span data-stu-id="0ed55-101">appListType enum type</span></span>

> <span data-ttu-id="0ed55-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0ed55-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0ed55-103">Posibles valores de la lista de aplicaciones de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="0ed55-103">Possible values of the compliance app list.</span></span>
## <a name="members"></a><span data-ttu-id="0ed55-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ed55-104">Members</span></span>
|<span data-ttu-id="0ed55-105">Miembro</span><span class="sxs-lookup"><span data-stu-id="0ed55-105">Member</span></span>|<span data-ttu-id="0ed55-106">Valor</span><span class="sxs-lookup"><span data-stu-id="0ed55-106">Value</span></span>|<span data-ttu-id="0ed55-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ed55-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0ed55-108">none</span><span class="sxs-lookup"><span data-stu-id="0ed55-108">none</span></span>|<span data-ttu-id="0ed55-109">0</span><span class="sxs-lookup"><span data-stu-id="0ed55-109">0%</span></span>|<span data-ttu-id="0ed55-110">Valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="0ed55-110">Default value, no intent.</span></span>|
|<span data-ttu-id="0ed55-111">appsInListCompliant</span><span class="sxs-lookup"><span data-stu-id="0ed55-111">appsInListCompliant</span></span>|<span data-ttu-id="0ed55-112">1</span><span class="sxs-lookup"><span data-stu-id="0ed55-112">-1</span></span>|<span data-ttu-id="0ed55-113">La lista representa las aplicaciones que se considerarán compatibles (solo las aplicaciones de la lista son compatibles).</span><span class="sxs-lookup"><span data-stu-id="0ed55-113">The list represents the apps that will be considered compliant (only apps on the list are compliant).</span></span>|
|<span data-ttu-id="0ed55-114">appsNotInListCompliant</span><span class="sxs-lookup"><span data-stu-id="0ed55-114">appsNotInListCompliant</span></span>|<span data-ttu-id="0ed55-115">2</span><span class="sxs-lookup"><span data-stu-id="0ed55-115">-2</span></span>|<span data-ttu-id="0ed55-116">La lista representa las aplicaciones que se considerarán no compatibles (todas las aplicaciones son compatibles excepto las aplicaciones de la lista).</span><span class="sxs-lookup"><span data-stu-id="0ed55-116">The list represents the apps that will be considered non compliant (all apps are compliant except apps on the list).</span></span>|








