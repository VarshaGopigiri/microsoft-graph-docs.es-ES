# <a name="fileencryptioninfo-resource-type"></a><span data-ttu-id="32b1e-101">Tipo de recurso fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="32b1e-101">fileEncryptionInfo resource type</span></span>

> <span data-ttu-id="32b1e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="32b1e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="32b1e-103">Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="32b1e-103">Contains properties for file encryption information for the content version of a line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="32b1e-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32b1e-104">Properties</span></span>
|<span data-ttu-id="32b1e-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32b1e-105">Property</span></span>|<span data-ttu-id="32b1e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="32b1e-106">Type</span></span>|<span data-ttu-id="32b1e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="32b1e-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="32b1e-108">encryptionKey</span><span class="sxs-lookup"><span data-stu-id="32b1e-108">encryptionKey</span></span>|<span data-ttu-id="32b1e-109">Binario</span><span class="sxs-lookup"><span data-stu-id="32b1e-109">Binary</span></span>|<span data-ttu-id="32b1e-110">La clave que se usa para cifrar el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="32b1e-110">The key used to encrypt the file content.</span></span>|
|<span data-ttu-id="32b1e-111">initializationVector</span><span class="sxs-lookup"><span data-stu-id="32b1e-111">initializationVector</span></span>|<span data-ttu-id="32b1e-112">Binario</span><span class="sxs-lookup"><span data-stu-id="32b1e-112">Binary</span></span>|<span data-ttu-id="32b1e-113">El vector de inicialización utilizado para el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="32b1e-113">The initialization vector used for the encryption algorithm.</span></span>|
|<span data-ttu-id="32b1e-114">mac</span><span class="sxs-lookup"><span data-stu-id="32b1e-114">mac</span></span>|<span data-ttu-id="32b1e-115">Binario</span><span class="sxs-lookup"><span data-stu-id="32b1e-115">Binary</span></span>|<span data-ttu-id="32b1e-116">El hash del contenido del archivo cifrado + IV (hash de contenido).</span><span class="sxs-lookup"><span data-stu-id="32b1e-116">The hash of the encrypted file content + IV (content hash).</span></span>|
|<span data-ttu-id="32b1e-117">macKey</span><span class="sxs-lookup"><span data-stu-id="32b1e-117">macKey</span></span>|<span data-ttu-id="32b1e-118">Binario</span><span class="sxs-lookup"><span data-stu-id="32b1e-118">Binary</span></span>|<span data-ttu-id="32b1e-119">La clave utilizada para obtener el MAC.</span><span class="sxs-lookup"><span data-stu-id="32b1e-119">The key used to get mac.</span></span>|
|<span data-ttu-id="32b1e-120">profileIdentifier</span><span class="sxs-lookup"><span data-stu-id="32b1e-120">profileIdentifier</span></span>|<span data-ttu-id="32b1e-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="32b1e-121">String</span></span>|<span data-ttu-id="32b1e-122">El identificador del perfil.</span><span class="sxs-lookup"><span data-stu-id="32b1e-122">The the profile identifier.</span></span>|
|<span data-ttu-id="32b1e-123">fileDigest</span><span class="sxs-lookup"><span data-stu-id="32b1e-123">fileDigest</span></span>|<span data-ttu-id="32b1e-124">Binario</span><span class="sxs-lookup"><span data-stu-id="32b1e-124">Binary</span></span>|<span data-ttu-id="32b1e-125">El resumen de los archivos antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="32b1e-125">The file digest prior to encryption.</span></span>|
|<span data-ttu-id="32b1e-126">fileDigestAlgorithm</span><span class="sxs-lookup"><span data-stu-id="32b1e-126">fileDigestAlgorithm</span></span>|<span data-ttu-id="32b1e-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="32b1e-127">String</span></span>|<span data-ttu-id="32b1e-128">El algoritmo del resumen de los archivos.</span><span class="sxs-lookup"><span data-stu-id="32b1e-128">The file digest algorithm.</span></span>|

## <a name="relationships"></a><span data-ttu-id="32b1e-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="32b1e-129">Relationships</span></span>
<span data-ttu-id="32b1e-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="32b1e-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="32b1e-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="32b1e-131">JSON Representation</span></span>
<span data-ttu-id="32b1e-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="32b1e-132">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.fileEncryptionInfo"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.fileEncryptionInfo",
  "encryptionKey": "binary",
  "initializationVector": "binary",
  "mac": "binary",
  "macKey": "binary",
  "profileIdentifier": "String",
  "fileDigest": "binary",
  "fileDigestAlgorithm": "String"
}
```








