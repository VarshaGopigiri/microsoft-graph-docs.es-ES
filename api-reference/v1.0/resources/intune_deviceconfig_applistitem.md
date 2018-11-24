# <a name="applistitem-resource-type"></a><span data-ttu-id="0845f-101">Tipo de recurso appListItem</span><span class="sxs-lookup"><span data-stu-id="0845f-101">appListItem resource type</span></span>

> <span data-ttu-id="0845f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0845f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0845f-103">Representa una aplicación en la lista de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="0845f-103">Represents an app in the list of managed applications</span></span>
## <a name="properties"></a><span data-ttu-id="0845f-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0845f-104">Properties</span></span>
|<span data-ttu-id="0845f-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0845f-105">Property</span></span>|<span data-ttu-id="0845f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="0845f-106">Type</span></span>|<span data-ttu-id="0845f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0845f-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0845f-108">name</span><span class="sxs-lookup"><span data-stu-id="0845f-108">name</span></span>|<span data-ttu-id="0845f-109">cadena</span><span class="sxs-lookup"><span data-stu-id="0845f-109">String</span></span>|<span data-ttu-id="0845f-110">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="0845f-110">The application name</span></span>|
|<span data-ttu-id="0845f-111">publicador</span><span class="sxs-lookup"><span data-stu-id="0845f-111">publisher</span></span>|<span data-ttu-id="0845f-112">cadena</span><span class="sxs-lookup"><span data-stu-id="0845f-112">String</span></span>|<span data-ttu-id="0845f-113">Publicador de la aplicación</span><span class="sxs-lookup"><span data-stu-id="0845f-113">The publisher of the application</span></span>|
|<span data-ttu-id="0845f-114">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="0845f-114">appStoreUrl</span></span>|<span data-ttu-id="0845f-115">cadena</span><span class="sxs-lookup"><span data-stu-id="0845f-115">String</span></span>|<span data-ttu-id="0845f-116">Dirección URL de la tienda de la aplicación</span><span class="sxs-lookup"><span data-stu-id="0845f-116">The Store URL of the application</span></span>|
|<span data-ttu-id="0845f-117">appId</span><span class="sxs-lookup"><span data-stu-id="0845f-117">appId</span></span>|<span data-ttu-id="0845f-118">cadena</span><span class="sxs-lookup"><span data-stu-id="0845f-118">String</span></span>|<span data-ttu-id="0845f-119">El identificador de la aplicación o de la agrupación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="0845f-119">The application or bundle identifier of the application</span></span>|

## <a name="relationships"></a><span data-ttu-id="0845f-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0845f-120">Relationships</span></span>
<span data-ttu-id="0845f-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0845f-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0845f-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0845f-122">JSON Representation</span></span>
<span data-ttu-id="0845f-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0845f-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.appListItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.appListItem",
  "name": "String",
  "publisher": "String",
  "appStoreUrl": "String",
  "appId": "String"
}
```



