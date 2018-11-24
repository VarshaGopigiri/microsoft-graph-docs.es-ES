# <a name="windowsinformationprotectionapp-resource-type"></a><span data-ttu-id="93e41-101">Tipo de recurso windowsInformationProtectionApp</span><span class="sxs-lookup"><span data-stu-id="93e41-101">windowsInformationProtectionApp resource type</span></span>

> <span data-ttu-id="93e41-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="93e41-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="93e41-103">Aplicación para Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="93e41-103">App for Windows information protection</span></span>
## <a name="properties"></a><span data-ttu-id="93e41-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93e41-104">Properties</span></span>
|<span data-ttu-id="93e41-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="93e41-105">Property</span></span>|<span data-ttu-id="93e41-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="93e41-106">Type</span></span>|<span data-ttu-id="93e41-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="93e41-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="93e41-108">displayName</span><span class="sxs-lookup"><span data-stu-id="93e41-108">displayName</span></span>|<span data-ttu-id="93e41-109">cadena</span><span class="sxs-lookup"><span data-stu-id="93e41-109">String</span></span>|<span data-ttu-id="93e41-110">Nombre para mostrar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="93e41-110">App display name.</span></span>|
|<span data-ttu-id="93e41-111">descripción</span><span class="sxs-lookup"><span data-stu-id="93e41-111">description</span></span>|<span data-ttu-id="93e41-112">cadena</span><span class="sxs-lookup"><span data-stu-id="93e41-112">String</span></span>|<span data-ttu-id="93e41-113">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="93e41-113">The app's description.</span></span>|
|<span data-ttu-id="93e41-114">publisherName</span><span class="sxs-lookup"><span data-stu-id="93e41-114">publisherName</span></span>|<span data-ttu-id="93e41-115">cadena</span><span class="sxs-lookup"><span data-stu-id="93e41-115">String</span></span>|<span data-ttu-id="93e41-116">El nombre del editor</span><span class="sxs-lookup"><span data-stu-id="93e41-116">The publisher name</span></span>|
|<span data-ttu-id="93e41-117">productName</span><span class="sxs-lookup"><span data-stu-id="93e41-117">productName</span></span>|<span data-ttu-id="93e41-118">cadena</span><span class="sxs-lookup"><span data-stu-id="93e41-118">String</span></span>|<span data-ttu-id="93e41-119">El nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="93e41-119">The product name.</span></span>|
|<span data-ttu-id="93e41-120">denegado</span><span class="sxs-lookup"><span data-stu-id="93e41-120">denied</span></span>|<span data-ttu-id="93e41-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="93e41-121">Boolean</span></span>|<span data-ttu-id="93e41-122">Si es true, se deniega la protección o la exención a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="93e41-122">If true, app is denied protection or exemption.</span></span>|

## <a name="relationships"></a><span data-ttu-id="93e41-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="93e41-123">Relationships</span></span>
<span data-ttu-id="93e41-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="93e41-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="93e41-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="93e41-125">JSON Representation</span></span>
<span data-ttu-id="93e41-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="93e41-126">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionApp",
  "displayName": "String",
  "description": "String",
  "publisherName": "String",
  "productName": "String",
  "denied": true
}
```



