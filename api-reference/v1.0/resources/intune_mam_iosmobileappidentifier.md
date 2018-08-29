# <a name="iosmobileappidentifier-resource-type"></a><span data-ttu-id="80865-101">Tipo de recurso iosMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="80865-101">iosMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="80865-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="80865-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="80865-103">El identificador de una aplicación móvil de iOS.</span><span class="sxs-lookup"><span data-stu-id="80865-103">The identifier for an iOS app.</span></span>

<span data-ttu-id="80865-104">Hereda de [mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="80865-104">Inherits from [mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="80865-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80865-105">Properties</span></span>
|<span data-ttu-id="80865-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80865-106">Property</span></span>|<span data-ttu-id="80865-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="80865-107">Type</span></span>|<span data-ttu-id="80865-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="80865-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80865-109">bundleId</span><span class="sxs-lookup"><span data-stu-id="80865-109">bundleId</span></span>|<span data-ttu-id="80865-110">cadena</span><span class="sxs-lookup"><span data-stu-id="80865-110">String</span></span>|<span data-ttu-id="80865-111">El identificador de una aplicación, como se especifica en la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="80865-111">The identifier for an app, as specified in the app store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="80865-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="80865-112">Relationships</span></span>
<span data-ttu-id="80865-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="80865-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="80865-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="80865-114">JSON Representation</span></span>
<span data-ttu-id="80865-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="80865-115">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.mobileAppIdentifier",
  "@odata.type": "microsoft.graph.iosMobileAppIdentifier"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMobileAppIdentifier",
  "bundleId": "String"
}
```



