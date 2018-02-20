# <a name="fileencryptioninfo-resource-type"></a><span data-ttu-id="24841-101">Tipo de recurso fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="24841-101">fileEncryptionInfo resource type</span></span>

> <span data-ttu-id="24841-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="24841-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="24841-103">Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="24841-103">Contains properties for file encryption information for the content version of a line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="24841-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24841-104">Properties</span></span>
|<span data-ttu-id="24841-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="24841-105">Property</span></span>|<span data-ttu-id="24841-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="24841-106">Type</span></span>|<span data-ttu-id="24841-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="24841-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="24841-108">encryptionKey</span><span class="sxs-lookup"><span data-stu-id="24841-108">encryptionKey</span></span>|<span data-ttu-id="24841-109">Binario</span><span class="sxs-lookup"><span data-stu-id="24841-109">Binary</span></span>|<span data-ttu-id="24841-110">La clave que se usa para cifrar el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="24841-110">The key used to encrypt the file content.</span></span>|
|<span data-ttu-id="24841-111">initializationVector</span><span class="sxs-lookup"><span data-stu-id="24841-111">initializationVector</span></span>|<span data-ttu-id="24841-112">Binario</span><span class="sxs-lookup"><span data-stu-id="24841-112">Binary</span></span>|<span data-ttu-id="24841-113">El vector de inicialización utilizado para el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="24841-113">The initialization vector used for the encryption algorithm.</span></span>|
|<span data-ttu-id="24841-114">mac</span><span class="sxs-lookup"><span data-stu-id="24841-114">Mac</span></span>|<span data-ttu-id="24841-115">Binario</span><span class="sxs-lookup"><span data-stu-id="24841-115">Binary</span></span>|<span data-ttu-id="24841-116">El hash del contenido del archivo cifrado + IV (hash de contenido).</span><span class="sxs-lookup"><span data-stu-id="24841-116">The hash of the encrypted file content + IV (content hash).</span></span>|
|<span data-ttu-id="24841-117">macKey</span><span class="sxs-lookup"><span data-stu-id="24841-117">macKey</span></span>|<span data-ttu-id="24841-118">Binario</span><span class="sxs-lookup"><span data-stu-id="24841-118">Binary</span></span>|<span data-ttu-id="24841-119">La clave utilizada para obtener el MAC.</span><span class="sxs-lookup"><span data-stu-id="24841-119">The key used to get mac.</span></span>|
|<span data-ttu-id="24841-120">profileIdentifier</span><span class="sxs-lookup"><span data-stu-id="24841-120">profileIdentifier</span></span>|<span data-ttu-id="24841-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="24841-121">String</span></span>|<span data-ttu-id="24841-122">El identificador del perfil.</span><span class="sxs-lookup"><span data-stu-id="24841-122">The the profile identifier.</span></span>|
|<span data-ttu-id="24841-123">fileDigest</span><span class="sxs-lookup"><span data-stu-id="24841-123">fileDigest</span></span>|<span data-ttu-id="24841-124">Binario</span><span class="sxs-lookup"><span data-stu-id="24841-124">Binary</span></span>|<span data-ttu-id="24841-125">El resumen de los archivos antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="24841-125">The file digest prior to encryption.</span></span>|
|<span data-ttu-id="24841-126">fileDigestAlgorithm</span><span class="sxs-lookup"><span data-stu-id="24841-126">fileDigestAlgorithm</span></span>|<span data-ttu-id="24841-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="24841-127">String</span></span>|<span data-ttu-id="24841-128">El algoritmo del resumen de los archivos.</span><span class="sxs-lookup"><span data-stu-id="24841-128">The file digest algorithm.</span></span>|

## <a name="relationships"></a><span data-ttu-id="24841-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="24841-129">Relationships</span></span>
<span data-ttu-id="24841-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="24841-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="24841-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="24841-131">JSON Representation</span></span>
<span data-ttu-id="24841-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="24841-132">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.fileEncryptionInfo"
}
-->
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



