# <a name="deleteuserfromsharedappledeviceactionresult-resource-type"></a><span data-ttu-id="9f4da-101">Tipo de recurso deleteUserFromSharedAppleDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="9f4da-101">deleteUserFromSharedAppleDeviceActionResult resource type</span></span>

> <span data-ttu-id="9f4da-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9f4da-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9f4da-103">Resultado de la acción Eliminar usuario del dispositivo Apple compartido</span><span class="sxs-lookup"><span data-stu-id="9f4da-103">Delete user from shared apple device action result</span></span>

<span data-ttu-id="9f4da-104">Hereda de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="9f4da-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="9f4da-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f4da-105">Properties</span></span>
|<span data-ttu-id="9f4da-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f4da-106">Property</span></span>|<span data-ttu-id="9f4da-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f4da-107">Type</span></span>|<span data-ttu-id="9f4da-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f4da-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9f4da-109">actionName</span><span class="sxs-lookup"><span data-stu-id="9f4da-109">actionName</span></span>|<span data-ttu-id="9f4da-110">cadena</span><span class="sxs-lookup"><span data-stu-id="9f4da-110">String</span></span>|<span data-ttu-id="9f4da-111">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="9f4da-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="9f4da-112">actionState</span><span class="sxs-lookup"><span data-stu-id="9f4da-112">actionState</span></span>|[<span data-ttu-id="9f4da-113">actionState</span><span class="sxs-lookup"><span data-stu-id="9f4da-113">actionState</span></span>](../resources/intune_devices_actionstate.md)|<span data-ttu-id="9f4da-114">Estado de la acción Inherited desde [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="9f4da-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span></span> <span data-ttu-id="9f4da-115">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="9f4da-115">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="9f4da-116">startDateTime</span><span class="sxs-lookup"><span data-stu-id="9f4da-116">startDateTime</span></span>|<span data-ttu-id="9f4da-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f4da-117">DateTimeOffset</span></span>|<span data-ttu-id="9f4da-118">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="9f4da-118">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="9f4da-119">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="9f4da-119">lastUpdatedDateTime</span></span>|<span data-ttu-id="9f4da-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f4da-120">DateTimeOffset</span></span>|<span data-ttu-id="9f4da-121">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="9f4da-121">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="9f4da-122">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9f4da-122">userPrincipalName</span></span>|<span data-ttu-id="9f4da-123">cadena</span><span class="sxs-lookup"><span data-stu-id="9f4da-123">String</span></span>|<span data-ttu-id="9f4da-124">Nombre principal de usuario del usuario que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="9f4da-124">User principal name of the user to be deleted</span></span>|

## <a name="relationships"></a><span data-ttu-id="9f4da-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9f4da-125">Relationships</span></span>
<span data-ttu-id="9f4da-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9f4da-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9f4da-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9f4da-127">JSON Representation</span></span>
<span data-ttu-id="9f4da-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9f4da-128">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deleteUserFromSharedAppleDeviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deleteUserFromSharedAppleDeviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "userPrincipalName": "String"
}
```



