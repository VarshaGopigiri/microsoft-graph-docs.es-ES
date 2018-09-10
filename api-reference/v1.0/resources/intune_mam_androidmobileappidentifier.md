# <a name="androidmobileappidentifier-resource-type"></a><span data-ttu-id="97c21-101">Tipo de recurso androidMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="97c21-101">androidMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="97c21-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="97c21-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="97c21-103">El identificador de una aplicación móvil de Android.</span><span class="sxs-lookup"><span data-stu-id="97c21-103">The identifier for an Android app.</span></span>

<span data-ttu-id="97c21-104">Hereda de [mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="97c21-104">Inherits from [mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="97c21-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97c21-105">Properties</span></span>
|<span data-ttu-id="97c21-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="97c21-106">Property</span></span>|<span data-ttu-id="97c21-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="97c21-107">Type</span></span>|<span data-ttu-id="97c21-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="97c21-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="97c21-109">packageId</span><span class="sxs-lookup"><span data-stu-id="97c21-109">packageId</span></span>|<span data-ttu-id="97c21-110">cadena</span><span class="sxs-lookup"><span data-stu-id="97c21-110">String</span></span>|<span data-ttu-id="97c21-111">El identificador de una aplicación, como se especifica en la Play Store.</span><span class="sxs-lookup"><span data-stu-id="97c21-111">The identifier for an app, as specified in the play store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="97c21-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="97c21-112">Relationships</span></span>
<span data-ttu-id="97c21-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="97c21-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="97c21-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="97c21-114">JSON Representation</span></span>
<span data-ttu-id="97c21-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="97c21-115">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidMobileAppIdentifier"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.androidMobileAppIdentifier",
  "packageId": "String"
}
```








