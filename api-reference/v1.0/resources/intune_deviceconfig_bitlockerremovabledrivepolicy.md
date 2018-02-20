# <a name="bitlockerremovabledrivepolicy-resource-type"></a><span data-ttu-id="d59e1-101">Tipo de recurso bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="d59e1-101">bitLockerRemovableDrivePolicy resource type</span></span>

> <span data-ttu-id="d59e1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d59e1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d59e1-103">Directivas de unidad extraíble de BitLocker</span><span class="sxs-lookup"><span data-stu-id="d59e1-103">BitLocker Removable Drive Policies.</span></span>
## <a name="properties"></a><span data-ttu-id="d59e1-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d59e1-104">Properties</span></span>
|<span data-ttu-id="d59e1-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d59e1-105">Property</span></span>|<span data-ttu-id="d59e1-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="d59e1-106">Type</span></span>|<span data-ttu-id="d59e1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d59e1-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d59e1-108">encryptionMethod</span><span class="sxs-lookup"><span data-stu-id="d59e1-108">encryptionMethod</span></span>|<span data-ttu-id="d59e1-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="d59e1-109">String</span></span>|<span data-ttu-id="d59e1-110">Seleccione el método de cifrado para las unidades extraíbles.</span><span class="sxs-lookup"><span data-stu-id="d59e1-110">Select the encryption method for removable  drives.</span></span> <span data-ttu-id="d59e1-111">Los valores posibles son: `aesCbc128`, `aesCbc256`, `xtsAes128` y `xtsAes256`.</span><span class="sxs-lookup"><span data-stu-id="d59e1-111">Possible values are: `aesCbc128`, `aesCbc256`, `xtsAes128`, `xtsAes256`.</span></span>|
|<span data-ttu-id="d59e1-112">requireEncryptionForWriteAccess</span><span class="sxs-lookup"><span data-stu-id="d59e1-112">requireEncryptionForWriteAccess</span></span>|<span data-ttu-id="d59e1-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="d59e1-113">Boolean</span></span>|<span data-ttu-id="d59e1-114">Indica si se bloquea el acceso de escritura a dispositivos configurados en otra organización.</span><span class="sxs-lookup"><span data-stu-id="d59e1-114">Indicates whether to block write access to devices configured in another organization.</span></span>  <span data-ttu-id="d59e1-115">Si requireEncryptionForWriteAccess es false, este valor no se aplica.</span><span class="sxs-lookup"><span data-stu-id="d59e1-115">If requireEncryptionForWriteAccess is false, this value does not affect.</span></span>|
|<span data-ttu-id="d59e1-116">blockCrossOrganizationWriteAccess</span><span class="sxs-lookup"><span data-stu-id="d59e1-116">blockCrossOrganizationWriteAccess</span></span>|<span data-ttu-id="d59e1-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="d59e1-117">Boolean</span></span>|<span data-ttu-id="d59e1-118">Esta configuración de directiva determina si es necesaria la protección BitLocker para que se pueda escribir en las unidades de datos extraíbles en un equipo.</span><span class="sxs-lookup"><span data-stu-id="d59e1-118">This policy setting determines whether BitLocker protection is required for removable data drives to be writable on a computer.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d59e1-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d59e1-119">Relationships</span></span>
<span data-ttu-id="d59e1-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d59e1-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d59e1-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d59e1-121">JSON Representation</span></span>
<span data-ttu-id="d59e1-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d59e1-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerRemovableDrivePolicy",
  "encryptionMethod": "String",
  "requireEncryptionForWriteAccess": true,
  "blockCrossOrganizationWriteAccess": true
}
```



