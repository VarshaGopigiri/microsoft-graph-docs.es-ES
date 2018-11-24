# <a name="windowsinformationprotectiondatarecoverycertificate-resource-type"></a><span data-ttu-id="28c6a-101">Tipo de recurso windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="28c6a-101">windowsInformationProtectionDataRecoveryCertificate resource type</span></span>

> <span data-ttu-id="28c6a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="28c6a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="28c6a-103">Certificado de recuperación de datos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="28c6a-103">Windows Information Protection DataRecoveryCertificate</span></span>
## <a name="properties"></a><span data-ttu-id="28c6a-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28c6a-104">Properties</span></span>
|<span data-ttu-id="28c6a-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="28c6a-105">Property</span></span>|<span data-ttu-id="28c6a-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="28c6a-106">Type</span></span>|<span data-ttu-id="28c6a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="28c6a-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="28c6a-108">subjectName</span><span class="sxs-lookup"><span data-stu-id="28c6a-108">subjectName</span></span>|<span data-ttu-id="28c6a-109">cadena</span><span class="sxs-lookup"><span data-stu-id="28c6a-109">String</span></span>|<span data-ttu-id="28c6a-110">Nombre de asunto del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="28c6a-110">Data recovery Certificate subject name</span></span>|
|<span data-ttu-id="28c6a-111">descripción</span><span class="sxs-lookup"><span data-stu-id="28c6a-111">description</span></span>|<span data-ttu-id="28c6a-112">cadena</span><span class="sxs-lookup"><span data-stu-id="28c6a-112">String</span></span>|<span data-ttu-id="28c6a-113">Descripción del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="28c6a-113">Data recovery Certificate description</span></span>|
|<span data-ttu-id="28c6a-114">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="28c6a-114">expirationDateTime</span></span>|<span data-ttu-id="28c6a-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="28c6a-115">DateTimeOffset</span></span>|<span data-ttu-id="28c6a-116">Fecha y hora de expiración del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="28c6a-116">Data recovery Certificate expiration datetime</span></span>|
|<span data-ttu-id="28c6a-117">certificado</span><span class="sxs-lookup"><span data-stu-id="28c6a-117">certificate</span></span>|<span data-ttu-id="28c6a-118">Binario</span><span class="sxs-lookup"><span data-stu-id="28c6a-118">Binary</span></span>|<span data-ttu-id="28c6a-119">Certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="28c6a-119">Data recovery Certificate</span></span>|

## <a name="relationships"></a><span data-ttu-id="28c6a-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="28c6a-120">Relationships</span></span>
<span data-ttu-id="28c6a-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="28c6a-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="28c6a-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="28c6a-122">JSON Representation</span></span>
<span data-ttu-id="28c6a-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="28c6a-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
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



