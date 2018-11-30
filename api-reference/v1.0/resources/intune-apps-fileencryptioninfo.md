---
title: Tipo de recurso fileEncryptionInfo
description: Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.
ms.openlocfilehash: 92aceaa56221287dcde67dcefb4d9ae7109d9273
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032031"
---
# <a name="fileencryptioninfo-resource-type"></a><span data-ttu-id="48598-103">Tipo de recurso fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="48598-103">fileEncryptionInfo resource type</span></span>

> <span data-ttu-id="48598-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="48598-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="48598-105">Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="48598-105">Contains properties for file encryption information for the content version of a line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="48598-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48598-106">Properties</span></span>
|<span data-ttu-id="48598-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="48598-107">Property</span></span>|<span data-ttu-id="48598-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="48598-108">Type</span></span>|<span data-ttu-id="48598-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="48598-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="48598-110">encryptionKey</span><span class="sxs-lookup"><span data-stu-id="48598-110">encryptionKey</span></span>|<span data-ttu-id="48598-111">Binario</span><span class="sxs-lookup"><span data-stu-id="48598-111">Binary</span></span>|<span data-ttu-id="48598-112">La clave que se usa para cifrar el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="48598-112">The key used to encrypt the file content.</span></span>|
|<span data-ttu-id="48598-113">initializationVector</span><span class="sxs-lookup"><span data-stu-id="48598-113">initializationVector</span></span>|<span data-ttu-id="48598-114">Binario</span><span class="sxs-lookup"><span data-stu-id="48598-114">Binary</span></span>|<span data-ttu-id="48598-115">El vector de inicialización utilizado para el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="48598-115">The initialization vector used for the encryption algorithm.</span></span>|
|<span data-ttu-id="48598-116">mac</span><span class="sxs-lookup"><span data-stu-id="48598-116">mac</span></span>|<span data-ttu-id="48598-117">Binario</span><span class="sxs-lookup"><span data-stu-id="48598-117">Binary</span></span>|<span data-ttu-id="48598-118">El hash del contenido del archivo cifrado + IV (hash de contenido).</span><span class="sxs-lookup"><span data-stu-id="48598-118">The hash of the encrypted file content + IV (content hash).</span></span>|
|<span data-ttu-id="48598-119">macKey</span><span class="sxs-lookup"><span data-stu-id="48598-119">macKey</span></span>|<span data-ttu-id="48598-120">Binario</span><span class="sxs-lookup"><span data-stu-id="48598-120">Binary</span></span>|<span data-ttu-id="48598-121">La clave utilizada para obtener el MAC.</span><span class="sxs-lookup"><span data-stu-id="48598-121">The key used to get mac.</span></span>|
|<span data-ttu-id="48598-122">profileIdentifier</span><span class="sxs-lookup"><span data-stu-id="48598-122">profileIdentifier</span></span>|<span data-ttu-id="48598-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="48598-123">String</span></span>|<span data-ttu-id="48598-124">El identificador del perfil.</span><span class="sxs-lookup"><span data-stu-id="48598-124">The the profile identifier.</span></span>|
|<span data-ttu-id="48598-125">fileDigest</span><span class="sxs-lookup"><span data-stu-id="48598-125">fileDigest</span></span>|<span data-ttu-id="48598-126">Binario</span><span class="sxs-lookup"><span data-stu-id="48598-126">Binary</span></span>|<span data-ttu-id="48598-127">El resumen de los archivos antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="48598-127">The file digest prior to encryption.</span></span>|
|<span data-ttu-id="48598-128">fileDigestAlgorithm</span><span class="sxs-lookup"><span data-stu-id="48598-128">fileDigestAlgorithm</span></span>|<span data-ttu-id="48598-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="48598-129">String</span></span>|<span data-ttu-id="48598-130">El algoritmo del resumen de los archivos.</span><span class="sxs-lookup"><span data-stu-id="48598-130">The file digest algorithm.</span></span>|

## <a name="relationships"></a><span data-ttu-id="48598-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="48598-131">Relationships</span></span>
<span data-ttu-id="48598-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="48598-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="48598-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="48598-133">JSON Representation</span></span>
<span data-ttu-id="48598-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="48598-134">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
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



