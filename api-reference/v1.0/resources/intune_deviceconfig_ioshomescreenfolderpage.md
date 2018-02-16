# <a name="ioshomescreenfolderpage-resource-type"></a><span data-ttu-id="7d8bd-101">Tipo de recurso iosHomeScreenFolderPage</span><span class="sxs-lookup"><span data-stu-id="7d8bd-101">iosHomeScreenFolderPage resource type</span></span>

> <span data-ttu-id="7d8bd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7d8bd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7d8bd-103">Una carpeta que contiene aplicaciones en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="7d8bd-103">A folder containing apps on the Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="7d8bd-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d8bd-104">Properties</span></span>
|<span data-ttu-id="7d8bd-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7d8bd-105">Property</span></span>|<span data-ttu-id="7d8bd-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d8bd-106">Type</span></span>|<span data-ttu-id="7d8bd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d8bd-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7d8bd-108">displayName</span><span class="sxs-lookup"><span data-stu-id="7d8bd-108">displayName</span></span>|<span data-ttu-id="7d8bd-109">cadena</span><span class="sxs-lookup"><span data-stu-id="7d8bd-109">String</span></span>|<span data-ttu-id="7d8bd-110">Nombre de la página de la carpeta</span><span class="sxs-lookup"><span data-stu-id="7d8bd-110">Name of the page</span></span>|
|<span data-ttu-id="7d8bd-111">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="7d8bd-111">apps</span></span>|<span data-ttu-id="7d8bd-112">Colección [iosHomeScreenApp](../resources/intune_deviceconfig_ioshomescreenapp.md)</span><span class="sxs-lookup"><span data-stu-id="7d8bd-112">[iosHomeScreenApp](../resources/intune_deviceconfig_ioshomescreenapp.md) collection</span></span>|<span data-ttu-id="7d8bd-113">Una lista de aplicaciones que aparecen en una página dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="7d8bd-113">A list of apps to appear on a page within a folder.</span></span> <span data-ttu-id="7d8bd-114">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="7d8bd-114">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7d8bd-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7d8bd-115">Relationships</span></span>
<span data-ttu-id="7d8bd-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7d8bd-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7d8bd-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7d8bd-117">JSON Representation</span></span>
<span data-ttu-id="7d8bd-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7d8bd-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosHomeScreenFolderPage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenFolderPage",
  "displayName": "String",
  "apps": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenApp",
      "displayName": "String",
      "bundleID": "String"
    }
  ]
}
```



