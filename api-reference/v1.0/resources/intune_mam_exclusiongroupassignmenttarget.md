# <a name="exclusiongroupassignmenttarget-resource-type"></a><span data-ttu-id="c2cd7-101">Tipo de recurso exclusionGroupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="c2cd7-101">exclusionGroupAssignmentTarget resource type</span></span>

> <span data-ttu-id="c2cd7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c2cd7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c2cd7-103">Representa un grupo que debería excluirse de una tarea.</span><span class="sxs-lookup"><span data-stu-id="c2cd7-103">Represents a group that should be excluded from an assignment.</span></span>

<span data-ttu-id="c2cd7-104">Hereda de [groupAssignmentTarget](../resources/intune_mam_groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="c2cd7-104">Inherits from [groupAssignmentTarget](../resources/intune_mam_groupassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="c2cd7-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2cd7-105">Properties</span></span>
|<span data-ttu-id="c2cd7-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2cd7-106">Property</span></span>|<span data-ttu-id="c2cd7-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2cd7-107">Type</span></span>|<span data-ttu-id="c2cd7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2cd7-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c2cd7-109">groupId</span><span class="sxs-lookup"><span data-stu-id="c2cd7-109">groupId</span></span>|<span data-ttu-id="c2cd7-110">cadena</span><span class="sxs-lookup"><span data-stu-id="c2cd7-110">String</span></span>|<span data-ttu-id="c2cd7-111">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="c2cd7-111">The group Id that is the target of the assignment.</span></span> <span data-ttu-id="c2cd7-112">Heredado de [groupAssignmentTarget](../resources/intune_mam_groupassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="c2cd7-112">Inherited from [groupAssignmentTarget](../resources/intune_mam_groupassignmenttarget.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="c2cd7-113">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c2cd7-113">Relationships</span></span>
<span data-ttu-id="c2cd7-114">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c2cd7-114">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c2cd7-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c2cd7-115">JSON Representation</span></span>
<span data-ttu-id="c2cd7-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c2cd7-116">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.exclusionGroupAssignmentTarget"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.exclusionGroupAssignmentTarget",
  "groupId": "String"
}
```



