# <a name="microsoftstoreforbusinessappassignmentsettings-resource-type"></a><span data-ttu-id="bd4a7-101">Tipo de recurso microsoftStoreForBusinessAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="bd4a7-101">microsoftStoreForBusinessAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="bd4a7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bd4a7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bd4a7-103">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="bd4a7-103">Contains properties used to assign an Microsoft Store for Business mobile app to a group.</span></span>

<span data-ttu-id="bd4a7-104">Hereda de [mobileAppAssignmentSettings](../resources/intune_apps_mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="bd4a7-104">Inherits from [mobileAppAssignmentSettings](../resources/intune_apps_mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="bd4a7-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bd4a7-105">Properties</span></span>
|<span data-ttu-id="bd4a7-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bd4a7-106">Property</span></span>|<span data-ttu-id="bd4a7-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd4a7-107">Type</span></span>|<span data-ttu-id="bd4a7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd4a7-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bd4a7-109">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="bd4a7-109">useDeviceContext</span></span>|<span data-ttu-id="bd4a7-110">Booleano</span><span class="sxs-lookup"><span data-stu-id="bd4a7-110">Boolean</span></span>|<span data-ttu-id="bd4a7-111">Si se debe usar o no el contexto de ejecución del dispositivo para la aplicación móvil de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="bd4a7-111">Whether or not to use device execution context for Microsoft Store for Business mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bd4a7-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bd4a7-112">Relationships</span></span>
<span data-ttu-id="bd4a7-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bd4a7-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="bd4a7-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bd4a7-114">JSON Representation</span></span>
<span data-ttu-id="bd4a7-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bd4a7-115">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.mobileAppAssignmentSettings",
  "@odata.type": "microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings",
  "useDeviceContext": true
}
```



