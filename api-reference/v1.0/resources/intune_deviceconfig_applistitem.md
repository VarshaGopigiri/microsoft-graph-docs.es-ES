# <a name="applistitem-resource-type"></a><span data-ttu-id="9cc10-101">Tipo de recurso appListItem</span><span class="sxs-lookup"><span data-stu-id="9cc10-101">appListItem resource type</span></span>

> <span data-ttu-id="9cc10-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9cc10-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9cc10-103">Representa una aplicación en la lista de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="9cc10-103">Represents an app in the list of managed applications</span></span>
## <a name="properties"></a><span data-ttu-id="9cc10-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9cc10-104">Properties</span></span>
|<span data-ttu-id="9cc10-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9cc10-105">Property</span></span>|<span data-ttu-id="9cc10-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="9cc10-106">Type</span></span>|<span data-ttu-id="9cc10-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cc10-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9cc10-108">name</span><span class="sxs-lookup"><span data-stu-id="9cc10-108">name</span></span>|<span data-ttu-id="9cc10-109">cadena</span><span class="sxs-lookup"><span data-stu-id="9cc10-109">String</span></span>|<span data-ttu-id="9cc10-110">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="9cc10-110">The application name</span></span>|
|<span data-ttu-id="9cc10-111">publicador</span><span class="sxs-lookup"><span data-stu-id="9cc10-111">publisher</span></span>|<span data-ttu-id="9cc10-112">cadena</span><span class="sxs-lookup"><span data-stu-id="9cc10-112">String</span></span>|<span data-ttu-id="9cc10-113">Publicador de la aplicación</span><span class="sxs-lookup"><span data-stu-id="9cc10-113">The publisher of the application</span></span>|
|<span data-ttu-id="9cc10-114">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="9cc10-114">appStoreUrl</span></span>|<span data-ttu-id="9cc10-115">cadena</span><span class="sxs-lookup"><span data-stu-id="9cc10-115">String</span></span>|<span data-ttu-id="9cc10-116">Dirección URL de la tienda de la aplicación</span><span class="sxs-lookup"><span data-stu-id="9cc10-116">The Store URL of the application</span></span>|
|<span data-ttu-id="9cc10-117">appId</span><span class="sxs-lookup"><span data-stu-id="9cc10-117">appId</span></span>|<span data-ttu-id="9cc10-118">cadena</span><span class="sxs-lookup"><span data-stu-id="9cc10-118">String</span></span>|<span data-ttu-id="9cc10-119">El identificador de la aplicación o de la agrupación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="9cc10-119">The application or bundle identifier of the application</span></span>|

## <a name="relationships"></a><span data-ttu-id="9cc10-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9cc10-120">Relationships</span></span>
<span data-ttu-id="9cc10-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9cc10-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9cc10-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9cc10-122">JSON Representation</span></span>
<span data-ttu-id="9cc10-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9cc10-123">Here is a JSON representation of the resource.</span></span>
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








