# <a name="windowsinformationprotectiondatarecoverycertificate-resource-type"></a><span data-ttu-id="87289-101">Tipo de recurso windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="87289-101">windowsInformationProtectionDataRecoveryCertificate resource type</span></span>

> <span data-ttu-id="87289-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="87289-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="87289-103">Certificado de recuperación de datos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="87289-103">Windows Information Protection DataRecoveryCertificate</span></span>
## <a name="properties"></a><span data-ttu-id="87289-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="87289-104">Properties</span></span>
|<span data-ttu-id="87289-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="87289-105">Property</span></span>|<span data-ttu-id="87289-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="87289-106">Type</span></span>|<span data-ttu-id="87289-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="87289-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="87289-108">subjectName</span><span class="sxs-lookup"><span data-stu-id="87289-108">subjectName</span></span>|<span data-ttu-id="87289-109">cadena</span><span class="sxs-lookup"><span data-stu-id="87289-109">String</span></span>|<span data-ttu-id="87289-110">Nombre de asunto del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="87289-110">Data recovery Certificate subject name</span></span>|
|<span data-ttu-id="87289-111">descripción</span><span class="sxs-lookup"><span data-stu-id="87289-111">description</span></span>|<span data-ttu-id="87289-112">cadena</span><span class="sxs-lookup"><span data-stu-id="87289-112">String</span></span>|<span data-ttu-id="87289-113">Descripción del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="87289-113">Data recovery Certificate description</span></span>|
|<span data-ttu-id="87289-114">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="87289-114">expirationDateTime</span></span>|<span data-ttu-id="87289-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="87289-115">DateTimeOffset</span></span>|<span data-ttu-id="87289-116">Fecha y hora de expiración del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="87289-116">Data recovery Certificate expiration datetime</span></span>|
|<span data-ttu-id="87289-117">certificado</span><span class="sxs-lookup"><span data-stu-id="87289-117">ACS, certificate</span></span>|<span data-ttu-id="87289-118">Binario</span><span class="sxs-lookup"><span data-stu-id="87289-118">Binary</span></span>|<span data-ttu-id="87289-119">Certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="87289-119">Data recovery Certificate</span></span>|

## <a name="relationships"></a><span data-ttu-id="87289-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="87289-120">Relationships</span></span>
<span data-ttu-id="87289-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="87289-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="87289-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="87289-122">JSON Representation</span></span>
<span data-ttu-id="87289-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="87289-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
  "subjectName": "String",
  "description": "String",
  "expirationDateTime": "String (timestamp)",
  "certificate": "binary"
}
```



