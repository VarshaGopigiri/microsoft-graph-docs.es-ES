# <a name="windowsinformationprotectionproxieddomaincollection-resource-type"></a><span data-ttu-id="c23de-101">Tipo de recurso windowsInformationProtectionProxiedDomainCollection</span><span class="sxs-lookup"><span data-stu-id="c23de-101">windowsInformationProtectionProxiedDomainCollection resource type</span></span>

> <span data-ttu-id="c23de-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c23de-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c23de-103">Colección de dominios con proxy de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="c23de-103">Windows Information Protection Proxied Domain Collection</span></span>
## <a name="properties"></a><span data-ttu-id="c23de-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c23de-104">Properties</span></span>
|<span data-ttu-id="c23de-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c23de-105">Property</span></span>|<span data-ttu-id="c23de-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="c23de-106">Type</span></span>|<span data-ttu-id="c23de-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c23de-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c23de-108">displayName</span><span class="sxs-lookup"><span data-stu-id="c23de-108">displayName</span></span>|<span data-ttu-id="c23de-109">cadena</span><span class="sxs-lookup"><span data-stu-id="c23de-109">String</span></span>|<span data-ttu-id="c23de-110">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="c23de-110">Display name</span></span>|
|<span data-ttu-id="c23de-111">proxiedDomains</span><span class="sxs-lookup"><span data-stu-id="c23de-111">proxiedDomains</span></span>|<span data-ttu-id="c23de-112">Colección [proxiedDomain](../resources/intune_mam_proxieddomain.md)</span><span class="sxs-lookup"><span data-stu-id="c23de-112">[proxiedDomain](../resources/intune_mam_proxieddomain.md) collection</span></span>|<span data-ttu-id="c23de-113">Conjunto de dominios con proxy</span><span class="sxs-lookup"><span data-stu-id="c23de-113">Collection of proxied domains</span></span>|

## <a name="relationships"></a><span data-ttu-id="c23de-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c23de-114">Relationships</span></span>
<span data-ttu-id="c23de-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c23de-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c23de-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c23de-116">JSON Representation</span></span>
<span data-ttu-id="c23de-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c23de-117">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
  "displayName": "String",
  "proxiedDomains": [
    {
      "@odata.type": "microsoft.graph.proxiedDomain",
      "ipAddressOrFQDN": "String",
      "proxy": "String"
    }
  ]
}
```



