# <a name="ioshomescreenpage-resource-type"></a><span data-ttu-id="2f946-101">Tipo de recurso iosHomeScreenPage</span><span class="sxs-lookup"><span data-stu-id="2f946-101">iosHomeScreenPage resource type</span></span>

> <span data-ttu-id="2f946-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2f946-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2f946-103">Una página que contiene aplicaciones y carpetas en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="2f946-103">A page containing apps and folders on the Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="2f946-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f946-104">Properties</span></span>
|<span data-ttu-id="2f946-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2f946-105">Property</span></span>|<span data-ttu-id="2f946-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f946-106">Type</span></span>|<span data-ttu-id="2f946-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f946-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2f946-108">displayName</span><span class="sxs-lookup"><span data-stu-id="2f946-108">displayName</span></span>|<span data-ttu-id="2f946-109">cadena</span><span class="sxs-lookup"><span data-stu-id="2f946-109">String</span></span>|<span data-ttu-id="2f946-110">Nombre de la página</span><span class="sxs-lookup"><span data-stu-id="2f946-110">Name of the page</span></span>|
|<span data-ttu-id="2f946-111">iconos</span><span class="sxs-lookup"><span data-stu-id="2f946-111">Icons</span></span>|<span data-ttu-id="2f946-112">Colección [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="2f946-112">[iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md) collection</span></span>|<span data-ttu-id="2f946-113">Una lista de aplicaciones y carpetas que aparecen en una página.</span><span class="sxs-lookup"><span data-stu-id="2f946-113">A list of apps and folders to appear on a page.</span></span> <span data-ttu-id="2f946-114">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="2f946-114">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2f946-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2f946-115">Relationships</span></span>
<span data-ttu-id="2f946-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2f946-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2f946-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2f946-117">JSON Representation</span></span>
<span data-ttu-id="2f946-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2f946-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosHomeScreenPage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenPage",
  "displayName": "String",
  "icons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
      "displayName": "String",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "String",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "String",
              "bundleID": "String"
            }
          ]
        }
      ]
    }
  ]
}
```



