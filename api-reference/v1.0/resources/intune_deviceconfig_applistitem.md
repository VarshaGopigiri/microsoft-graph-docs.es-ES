# <a name="applistitem-resource-type"></a><span data-ttu-id="849d6-101">Tipo de recurso appListItem</span><span class="sxs-lookup"><span data-stu-id="849d6-101">appListItem resource type</span></span>

> <span data-ttu-id="849d6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="849d6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="849d6-103">Representa una aplicación en la lista de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="849d6-103">Represents an app in the list of managed applications</span></span>
## <a name="properties"></a><span data-ttu-id="849d6-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="849d6-104">Properties</span></span>
|<span data-ttu-id="849d6-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="849d6-105">Property</span></span>|<span data-ttu-id="849d6-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="849d6-106">Type</span></span>|<span data-ttu-id="849d6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="849d6-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="849d6-108">name</span><span class="sxs-lookup"><span data-stu-id="849d6-108">name</span></span>|<span data-ttu-id="849d6-109">cadena</span><span class="sxs-lookup"><span data-stu-id="849d6-109">String</span></span>|<span data-ttu-id="849d6-110">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="849d6-110">The application name</span></span>|
|<span data-ttu-id="849d6-111">publicador</span><span class="sxs-lookup"><span data-stu-id="849d6-111">publisher</span></span>|<span data-ttu-id="849d6-112">cadena</span><span class="sxs-lookup"><span data-stu-id="849d6-112">String</span></span>|<span data-ttu-id="849d6-113">Publicador de la aplicación</span><span class="sxs-lookup"><span data-stu-id="849d6-113">The publisher of the application</span></span>|
|<span data-ttu-id="849d6-114">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="849d6-114">appStoreUrl</span></span>|<span data-ttu-id="849d6-115">cadena</span><span class="sxs-lookup"><span data-stu-id="849d6-115">String</span></span>|<span data-ttu-id="849d6-116">Dirección URL de la tienda de la aplicación</span><span class="sxs-lookup"><span data-stu-id="849d6-116">The Store URL of the application</span></span>|
|<span data-ttu-id="849d6-117">appId</span><span class="sxs-lookup"><span data-stu-id="849d6-117">appId</span></span>|<span data-ttu-id="849d6-118">cadena</span><span class="sxs-lookup"><span data-stu-id="849d6-118">String</span></span>|<span data-ttu-id="849d6-119">El identificador de la aplicación o de la agrupación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="849d6-119">The application or bundle identifier of the application</span></span>|

## <a name="relationships"></a><span data-ttu-id="849d6-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="849d6-120">Relationships</span></span>
<span data-ttu-id="849d6-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="849d6-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="849d6-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="849d6-122">JSON Representation</span></span>
<span data-ttu-id="849d6-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="849d6-123">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.appListItem"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.appListItem",
  "name": "String",
  "publisher": "String",
  "appStoreUrl": "String",
  "appId": "String"
}
```



