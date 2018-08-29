# <a name="deleteuserfromsharedappledeviceactionresult-resource-type"></a><span data-ttu-id="aa0b7-101">Tipo de recurso deleteUserFromSharedAppleDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="aa0b7-101">deleteUserFromSharedAppleDeviceActionResult resource type</span></span>

> <span data-ttu-id="aa0b7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aa0b7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aa0b7-103">Resultado de la acción Eliminar usuario del dispositivo Apple compartido</span><span class="sxs-lookup"><span data-stu-id="aa0b7-103">Delete user from shared apple device action result</span></span>

<span data-ttu-id="aa0b7-104">Hereda de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="aa0b7-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="aa0b7-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa0b7-105">Properties</span></span>
|<span data-ttu-id="aa0b7-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa0b7-106">Property</span></span>|<span data-ttu-id="aa0b7-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa0b7-107">Type</span></span>|<span data-ttu-id="aa0b7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa0b7-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aa0b7-109">actionName</span><span class="sxs-lookup"><span data-stu-id="aa0b7-109">actionName</span></span>|<span data-ttu-id="aa0b7-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa0b7-110">String</span></span>|<span data-ttu-id="aa0b7-111">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="aa0b7-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="aa0b7-112">actionState</span><span class="sxs-lookup"><span data-stu-id="aa0b7-112">actionState</span></span>|[<span data-ttu-id="aa0b7-113">actionState</span><span class="sxs-lookup"><span data-stu-id="aa0b7-113">actionState</span></span>](../resources/intune_devices_actionstate.md)|<span data-ttu-id="aa0b7-114">Estado de la acción Inherited desde [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="aa0b7-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md) Possible values are: , , , , , , .</span></span> <span data-ttu-id="aa0b7-115">Los valores posibles son `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="aa0b7-115">The possible values are `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`, , , , , or .</span></span>|
|<span data-ttu-id="aa0b7-116">startDateTime</span><span class="sxs-lookup"><span data-stu-id="aa0b7-116">startDateTime</span></span>|<span data-ttu-id="aa0b7-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa0b7-117">DateTimeOffset</span></span>|<span data-ttu-id="aa0b7-118">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="aa0b7-118">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="aa0b7-119">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="aa0b7-119">lastUpdatedDateTime</span></span>|<span data-ttu-id="aa0b7-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa0b7-120">DateTimeOffset</span></span>|<span data-ttu-id="aa0b7-121">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="aa0b7-121">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="aa0b7-122">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa0b7-122">userPrincipalName</span></span>|<span data-ttu-id="aa0b7-123">cadena</span><span class="sxs-lookup"><span data-stu-id="aa0b7-123">String</span></span>|<span data-ttu-id="aa0b7-124">Nombre principal de usuario del usuario que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="aa0b7-124">User principal name of the user to be deleted</span></span>|

## <a name="relationships"></a><span data-ttu-id="aa0b7-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="aa0b7-125">Relationships</span></span>
<span data-ttu-id="aa0b7-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="aa0b7-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="aa0b7-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aa0b7-127">JSON Representation</span></span>
<span data-ttu-id="aa0b7-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="aa0b7-128">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.deviceActionResult",
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



