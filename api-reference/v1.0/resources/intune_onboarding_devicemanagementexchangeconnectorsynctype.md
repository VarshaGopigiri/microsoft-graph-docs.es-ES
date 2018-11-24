# <a name="devicemanagementexchangeconnectorsynctype-enum-type"></a><span data-ttu-id="a27b0-101">tipo de enumeración deviceManagementExchangeConnectorSyncType</span><span class="sxs-lookup"><span data-stu-id="a27b0-101">deviceManagementExchangeConnectorSyncType enum type</span></span>

> <span data-ttu-id="a27b0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a27b0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a27b0-103">El tipo de sincronización de conector de Exchange solicitada.</span><span class="sxs-lookup"><span data-stu-id="a27b0-103">The type of Exchange Connector sync requested.</span></span>
## <a name="members"></a><span data-ttu-id="a27b0-104">Miembros</span><span class="sxs-lookup"><span data-stu-id="a27b0-104">Members</span></span>
|<span data-ttu-id="a27b0-105">Miembro	</span><span class="sxs-lookup"><span data-stu-id="a27b0-105">Member</span></span>|<span data-ttu-id="a27b0-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a27b0-106">Value</span></span>|<span data-ttu-id="a27b0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a27b0-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a27b0-108">fullSync</span><span class="sxs-lookup"><span data-stu-id="a27b0-108">fullSync</span></span>|<span data-ttu-id="a27b0-109">0</span><span class="sxs-lookup"><span data-stu-id="a27b0-109">0</span></span>|<span data-ttu-id="a27b0-110">Descubrir todos los el dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="a27b0-110">Discover all the device in Exchange.</span></span>|
|<span data-ttu-id="a27b0-111">deltaSync</span><span class="sxs-lookup"><span data-stu-id="a27b0-111">deltaSync</span></span>|<span data-ttu-id="a27b0-112">1</span><span class="sxs-lookup"><span data-stu-id="a27b0-112">1</span></span>|<span data-ttu-id="a27b0-113">Descubrir sólo el dispositivo en Exchange que se actualizaron durante la ventana de sincronización delta.</span><span class="sxs-lookup"><span data-stu-id="a27b0-113">Discover only the device in Exchange which have updated during the delta sync window.</span></span>|



