# <a name="mimecontent-resource-type"></a><span data-ttu-id="f052e-101">Tipo de recurso mimeContent</span><span class="sxs-lookup"><span data-stu-id="f052e-101">mimeContent resource type</span></span>

> <span data-ttu-id="f052e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f052e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f052e-103">Contiene las propiedades de un contenido MIME genérico.</span><span class="sxs-lookup"><span data-stu-id="f052e-103">Contains properties for a generic mime content.</span></span>
## <a name="properties"></a><span data-ttu-id="f052e-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f052e-104">Properties</span></span>
|<span data-ttu-id="f052e-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f052e-105">Property</span></span>|<span data-ttu-id="f052e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f052e-106">Type</span></span>|<span data-ttu-id="f052e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f052e-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f052e-108">type</span><span class="sxs-lookup"><span data-stu-id="f052e-108">type</span></span>|<span data-ttu-id="f052e-109">String</span><span class="sxs-lookup"><span data-stu-id="f052e-109">String</span></span>|<span data-ttu-id="f052e-110">Indica el tipo de contenido MIME.</span><span class="sxs-lookup"><span data-stu-id="f052e-110">Indicates the content mime type.</span></span>|
|<span data-ttu-id="f052e-111">valor</span><span class="sxs-lookup"><span data-stu-id="f052e-111">value</span></span>|<span data-ttu-id="f052e-112">Binario</span><span class="sxs-lookup"><span data-stu-id="f052e-112">Binary</span></span>|<span data-ttu-id="f052e-113">Matriz de bytes que contiene el contenido real.</span><span class="sxs-lookup"><span data-stu-id="f052e-113">The byte array that contains the actual content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f052e-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f052e-114">Relationships</span></span>
<span data-ttu-id="f052e-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f052e-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f052e-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f052e-116">JSON Representation</span></span>
<span data-ttu-id="f052e-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f052e-117">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mimeContent"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.mimeContent",
  "type": "String",
  "value": "binary"
}
```








