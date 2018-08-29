# <a name="ioshomescreenfolder-resource-type"></a><span data-ttu-id="5fce8-101">Tipo de recurso iosHomeScreenFolder</span><span class="sxs-lookup"><span data-stu-id="5fce8-101">iosHomeScreenFolder resource type</span></span>

> <span data-ttu-id="5fce8-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5fce8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5fce8-103">Una carpeta que contiene páginas de aplicaciones en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="5fce8-103">A folder containing pages of apps on the Home Screen</span></span>

<span data-ttu-id="5fce8-104">Hereda de [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="5fce8-104">Inherits from [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="5fce8-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5fce8-105">Properties</span></span>
|<span data-ttu-id="5fce8-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5fce8-106">Property</span></span>|<span data-ttu-id="5fce8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fce8-107">Type</span></span>|<span data-ttu-id="5fce8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fce8-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5fce8-109">displayName</span><span class="sxs-lookup"><span data-stu-id="5fce8-109">displayName</span></span>|<span data-ttu-id="5fce8-110">cadena</span><span class="sxs-lookup"><span data-stu-id="5fce8-110">String</span></span>|<span data-ttu-id="5fce8-111">Nombre de la aplicación heredado de [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="5fce8-111">Name of the app Inherited from [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="5fce8-112">páginas</span><span class="sxs-lookup"><span data-stu-id="5fce8-112">pages</span></span>|<span data-ttu-id="5fce8-113">Colección [iosHomeScreenFolderPage](../resources/intune_deviceconfig_ioshomescreenfolderpage.md)</span><span class="sxs-lookup"><span data-stu-id="5fce8-113">[iosHomeScreenFolderPage](../resources/intune_deviceconfig_ioshomescreenfolderpage.md) collection</span></span>|<span data-ttu-id="5fce8-114">Páginas de iconos de diseño de pantalla de inicio que deben ser Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fce8-114">Pages of Home Screen Layout Icons which must be Application Type.</span></span> <span data-ttu-id="5fce8-115">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="5fce8-115">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5fce8-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5fce8-116">Relationships</span></span>
<span data-ttu-id="5fce8-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5fce8-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5fce8-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5fce8-118">JSON Representation</span></span>
<span data-ttu-id="5fce8-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5fce8-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.iosHomeScreenItem",
  "@odata.type": "microsoft.graph.iosHomeScreenFolder"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenFolder",
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
```



