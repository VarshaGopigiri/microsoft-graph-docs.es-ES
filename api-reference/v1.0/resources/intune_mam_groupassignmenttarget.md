# <a name="groupassignmenttarget-resource-type"></a><span data-ttu-id="05ef6-101">Tipo de recurso groupAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="05ef6-101">groupAssignmentTarget resource type</span></span>

> <span data-ttu-id="05ef6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="05ef6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="05ef6-103">Representa una tarea de un grupo.</span><span class="sxs-lookup"><span data-stu-id="05ef6-103">Represents an assignment to a group.</span></span>

<span data-ttu-id="05ef6-104">Hereda de [deviceAndAppManagementAssignmentTarget](../resources/intune_mam_deviceandappmanagementassignmenttarget.md)</span><span class="sxs-lookup"><span data-stu-id="05ef6-104">Inherits from [deviceAndAppManagementAssignmentTarget](../resources/intune_mam_deviceandappmanagementassignmenttarget.md)</span></span>

## <a name="properties"></a><span data-ttu-id="05ef6-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="05ef6-105">Properties</span></span>
|<span data-ttu-id="05ef6-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="05ef6-106">Property</span></span>|<span data-ttu-id="05ef6-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="05ef6-107">Type</span></span>|<span data-ttu-id="05ef6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="05ef6-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="05ef6-109">groupId</span><span class="sxs-lookup"><span data-stu-id="05ef6-109">groupId</span></span>|<span data-ttu-id="05ef6-110">cadena</span><span class="sxs-lookup"><span data-stu-id="05ef6-110">String</span></span>|<span data-ttu-id="05ef6-111">El identificador de grupo que es el destino de la tarea.</span><span class="sxs-lookup"><span data-stu-id="05ef6-111">The group Id that is the target of the assignment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="05ef6-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="05ef6-112">Relationships</span></span>
<span data-ttu-id="05ef6-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="05ef6-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="05ef6-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="05ef6-114">JSON Representation</span></span>
<span data-ttu-id="05ef6-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="05ef6-115">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.groupAssignmentTarget"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.groupAssignmentTarget",
  "groupId": "String"
}
```



