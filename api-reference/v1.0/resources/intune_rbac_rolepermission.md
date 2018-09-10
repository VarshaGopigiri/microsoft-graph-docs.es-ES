# <a name="rolepermission-resource-type"></a><span data-ttu-id="1bbcd-101">Tipo de recurso rolePermission</span><span class="sxs-lookup"><span data-stu-id="1bbcd-101">rolePermission resource type</span></span>

> <span data-ttu-id="1bbcd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1bbcd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1bbcd-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1bbcd-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="1bbcd-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bbcd-104">Properties</span></span>
|<span data-ttu-id="1bbcd-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1bbcd-105">Property</span></span>|<span data-ttu-id="1bbcd-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="1bbcd-106">Type</span></span>|<span data-ttu-id="1bbcd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1bbcd-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1bbcd-108">resourceActions</span><span class="sxs-lookup"><span data-stu-id="1bbcd-108">resourceActions</span></span>|<span data-ttu-id="1bbcd-109">Colección [resourceAction](../resources/intune_rbac_resourceaction.md)</span><span class="sxs-lookup"><span data-stu-id="1bbcd-109">[resourceAction](../resources/intune_rbac_resourceaction.md) collection</span></span>|<span data-ttu-id="1bbcd-110">Acciones</span><span class="sxs-lookup"><span data-stu-id="1bbcd-110">Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="1bbcd-111">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1bbcd-111">Relationships</span></span>
<span data-ttu-id="1bbcd-112">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1bbcd-112">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1bbcd-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1bbcd-113">JSON Representation</span></span>
<span data-ttu-id="1bbcd-114">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1bbcd-114">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.rolePermission"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.rolePermission",
  "resourceActions": [
    {
      "@odata.type": "microsoft.graph.resourceAction",
      "allowedResourceActions": [
        "String"
      ],
      "notAllowedResourceActions": [
        "String"
      ]
    }
  ]
}
```








