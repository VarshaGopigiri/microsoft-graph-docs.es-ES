# <a name="proxieddomain-resource-type"></a><span data-ttu-id="59c44-101">Tipo de recurso proxiedDomain</span><span class="sxs-lookup"><span data-stu-id="59c44-101">proxiedDomain resource type</span></span>

> <span data-ttu-id="59c44-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="59c44-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="59c44-103">Dominio con proxy</span><span class="sxs-lookup"><span data-stu-id="59c44-103">Proxied Domain</span></span>
## <a name="properties"></a><span data-ttu-id="59c44-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59c44-104">Properties</span></span>
|<span data-ttu-id="59c44-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59c44-105">Property</span></span>|<span data-ttu-id="59c44-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="59c44-106">Type</span></span>|<span data-ttu-id="59c44-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="59c44-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="59c44-108">ipAddressOrFQDN</span><span class="sxs-lookup"><span data-stu-id="59c44-108">ipAddressOrFQDN</span></span>|<span data-ttu-id="59c44-109">cadena</span><span class="sxs-lookup"><span data-stu-id="59c44-109">String</span></span>|<span data-ttu-id="59c44-110">La dirección IP o FQDN</span><span class="sxs-lookup"><span data-stu-id="59c44-110">The IP address or FQDN</span></span>|
|<span data-ttu-id="59c44-111">proxy</span><span class="sxs-lookup"><span data-stu-id="59c44-111">proxy</span></span>|<span data-ttu-id="59c44-112">cadena</span><span class="sxs-lookup"><span data-stu-id="59c44-112">String</span></span>|<span data-ttu-id="59c44-113">IP de proxy</span><span class="sxs-lookup"><span data-stu-id="59c44-113">Proxy IP</span></span>|

## <a name="relationships"></a><span data-ttu-id="59c44-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="59c44-114">Relationships</span></span>
<span data-ttu-id="59c44-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="59c44-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="59c44-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="59c44-116">JSON Representation</span></span>
<span data-ttu-id="59c44-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="59c44-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.proxiedDomain"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.proxiedDomain",
  "ipAddressOrFQDN": "String",
  "proxy": "String"
}
```



