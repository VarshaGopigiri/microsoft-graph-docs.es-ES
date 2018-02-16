# <a name="iosmobileappidentifier-resource-type"></a><span data-ttu-id="fdf82-101">Tipo de recurso iosMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="fdf82-101">iosMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="fdf82-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fdf82-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fdf82-103">El identificador de una aplicación móvil de iOS.</span><span class="sxs-lookup"><span data-stu-id="fdf82-103">The identifier for an iOS app.</span></span>

<span data-ttu-id="fdf82-104">Hereda de [mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="fdf82-104">Inherits from [mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="fdf82-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fdf82-105">Properties</span></span>
|<span data-ttu-id="fdf82-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fdf82-106">Property</span></span>|<span data-ttu-id="fdf82-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdf82-107">Type</span></span>|<span data-ttu-id="fdf82-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdf82-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fdf82-109">bundleId</span><span class="sxs-lookup"><span data-stu-id="fdf82-109">bundleId</span></span>|<span data-ttu-id="fdf82-110">cadena</span><span class="sxs-lookup"><span data-stu-id="fdf82-110">String</span></span>|<span data-ttu-id="fdf82-111">El identificador de una aplicación, como se especifica en la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fdf82-111">The identifier for an app, as specified in the app store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fdf82-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fdf82-112">Relationships</span></span>
<span data-ttu-id="fdf82-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fdf82-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fdf82-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fdf82-114">JSON Representation</span></span>
<span data-ttu-id="fdf82-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fdf82-115">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosMobileAppIdentifier"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMobileAppIdentifier",
  "bundleId": "String"
}
```



