# <a name="windows10networkproxyserver-resource-type"></a><span data-ttu-id="f5ad3-101">Tipo de recurso windows10NetworkProxyServer</span><span class="sxs-lookup"><span data-stu-id="f5ad3-101">windows10NetworkProxyServer resource type</span></span>

> <span data-ttu-id="f5ad3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f5ad3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f5ad3-103">Directiva del servidor proxy de red</span><span class="sxs-lookup"><span data-stu-id="f5ad3-103">Network Proxy Server Policy.</span></span>
## <a name="properties"></a><span data-ttu-id="f5ad3-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5ad3-104">Properties</span></span>
|<span data-ttu-id="f5ad3-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f5ad3-105">Property</span></span>|<span data-ttu-id="f5ad3-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5ad3-106">Type</span></span>|<span data-ttu-id="f5ad3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5ad3-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f5ad3-108">address</span><span class="sxs-lookup"><span data-stu-id="f5ad3-108">address</span></span>|<span data-ttu-id="f5ad3-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="f5ad3-109">String</span></span>|<span data-ttu-id="f5ad3-110">Dirección del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="f5ad3-110">Address to the proxy server.</span></span> <span data-ttu-id="f5ad3-111">Especifique una dirección en formato <server>\[":"<port>\]</span><span class="sxs-lookup"><span data-stu-id="f5ad3-111">Specify an address in the format <server>\[“:”<port>\]</span></span>|
|<span data-ttu-id="f5ad3-112">excepciones</span><span class="sxs-lookup"><span data-stu-id="f5ad3-112">exceptions</span></span>|<span data-ttu-id="f5ad3-113">Colección string</span><span class="sxs-lookup"><span data-stu-id="f5ad3-113">String collection</span></span>|<span data-ttu-id="f5ad3-114">Direcciones que el servidor proxy no debe usar.</span><span class="sxs-lookup"><span data-stu-id="f5ad3-114">Addresses that should not use the proxy server.</span></span> <span data-ttu-id="f5ad3-115">El sistema no usará el servidor proxy para las direcciones que empiecen por lo que se especifica en este nodo.</span><span class="sxs-lookup"><span data-stu-id="f5ad3-115">The system will not use the proxy server for addresses beginning with what is specified in this node.</span></span>|
|<span data-ttu-id="f5ad3-116">useForLocalAddresses</span><span class="sxs-lookup"><span data-stu-id="f5ad3-116">useForLocalAddresses</span></span>|<span data-ttu-id="f5ad3-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="f5ad3-117">Boolean</span></span>|<span data-ttu-id="f5ad3-118">Especifica si el servidor proxy se debe usar para direcciones locales (intranet).</span><span class="sxs-lookup"><span data-stu-id="f5ad3-118">Specifies whether the proxy server should be used for local (intranet) addresses.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f5ad3-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f5ad3-119">Relationships</span></span>
<span data-ttu-id="f5ad3-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f5ad3-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f5ad3-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f5ad3-121">JSON Representation</span></span>
<span data-ttu-id="f5ad3-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f5ad3-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10NetworkProxyServer"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10NetworkProxyServer",
  "address": "String",
  "exceptions": [
    "String"
  ],
  "useForLocalAddresses": true
}
```



