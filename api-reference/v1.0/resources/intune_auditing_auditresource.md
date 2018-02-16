# <a name="auditresource-resource-type"></a><span data-ttu-id="26d8d-101">Tipo de recurso auditResource</span><span class="sxs-lookup"><span data-stu-id="26d8d-101">auditResource resource type</span></span>

> <span data-ttu-id="26d8d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="26d8d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="26d8d-103">Una clase que contiene las propiedades del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="26d8d-103">A class containing the properties for Audit Resource.</span></span>
## <a name="properties"></a><span data-ttu-id="26d8d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26d8d-104">Properties</span></span>
|<span data-ttu-id="26d8d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26d8d-105">Property</span></span>|<span data-ttu-id="26d8d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="26d8d-106">Type</span></span>|<span data-ttu-id="26d8d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="26d8d-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="26d8d-108">displayName</span><span class="sxs-lookup"><span data-stu-id="26d8d-108">displayName</span></span>|<span data-ttu-id="26d8d-109">cadena</span><span class="sxs-lookup"><span data-stu-id="26d8d-109">String</span></span>|<span data-ttu-id="26d8d-110">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="26d8d-110">Display Name</span></span>|
|<span data-ttu-id="26d8d-111">modifiedProperties</span><span class="sxs-lookup"><span data-stu-id="26d8d-111">modifiedProperties</span></span>|<span data-ttu-id="26d8d-112">Colección [auditProperty](../resources/intune_auditing_auditproperty.md)</span><span class="sxs-lookup"><span data-stu-id="26d8d-112">[auditProperty](../resources/intune_auditing_auditproperty.md) collection</span></span>|<span data-ttu-id="26d8d-113">Lista de propiedades modificadas.</span><span class="sxs-lookup"><span data-stu-id="26d8d-113">List of managed properties</span></span>|
|<span data-ttu-id="26d8d-114">tipo</span><span class="sxs-lookup"><span data-stu-id="26d8d-114">type</span></span>|<span data-ttu-id="26d8d-115">cadena</span><span class="sxs-lookup"><span data-stu-id="26d8d-115">String</span></span>|<span data-ttu-id="26d8d-116">Tipo del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="26d8d-116">Audit resource's type.</span></span>|
|<span data-ttu-id="26d8d-117">resourceId</span><span class="sxs-lookup"><span data-stu-id="26d8d-117">resourceId</span></span>|<span data-ttu-id="26d8d-118">cadena</span><span class="sxs-lookup"><span data-stu-id="26d8d-118">String</span></span>|<span data-ttu-id="26d8d-119">Identificador del recurso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="26d8d-119">Audit resource's Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="26d8d-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="26d8d-120">Relationships</span></span>
<span data-ttu-id="26d8d-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="26d8d-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="26d8d-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="26d8d-122">JSON Representation</span></span>
<span data-ttu-id="26d8d-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="26d8d-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.auditResource"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditResource",
  "displayName": "String",
  "modifiedProperties": [
    {
      "@odata.type": "microsoft.graph.auditProperty",
      "displayName": "String",
      "oldValue": "String",
      "newValue": "String"
    }
  ],
  "type": "String",
  "resourceId": "String"
}
```



