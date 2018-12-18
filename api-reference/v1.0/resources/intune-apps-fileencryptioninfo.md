---
title: Tipo de recurso fileEncryptionInfo
description: Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.
author: tfitzmac
ms.openlocfilehash: c58865e746afcde8167c8d905c3b4064d8690a95
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309189"
---
# <a name="fileencryptioninfo-resource-type"></a><span data-ttu-id="fb9ad-103">Tipo de recurso fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="fb9ad-103">fileEncryptionInfo resource type</span></span>

> <span data-ttu-id="fb9ad-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fb9ad-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fb9ad-105">Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="fb9ad-105">Contains properties for file encryption information for the content version of a line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="fb9ad-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb9ad-106">Properties</span></span>
|<span data-ttu-id="fb9ad-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb9ad-107">Property</span></span>|<span data-ttu-id="fb9ad-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb9ad-108">Type</span></span>|<span data-ttu-id="fb9ad-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb9ad-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fb9ad-110">encryptionKey</span><span class="sxs-lookup"><span data-stu-id="fb9ad-110">encryptionKey</span></span>|<span data-ttu-id="fb9ad-111">Binario</span><span class="sxs-lookup"><span data-stu-id="fb9ad-111">Binary</span></span>|<span data-ttu-id="fb9ad-112">La clave que se usa para cifrar el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="fb9ad-112">The key used to encrypt the file content.</span></span>|
|<span data-ttu-id="fb9ad-113">initializationVector</span><span class="sxs-lookup"><span data-stu-id="fb9ad-113">initializationVector</span></span>|<span data-ttu-id="fb9ad-114">Binario</span><span class="sxs-lookup"><span data-stu-id="fb9ad-114">Binary</span></span>|<span data-ttu-id="fb9ad-115">El vector de inicialización utilizado para el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="fb9ad-115">The initialization vector used for the encryption algorithm.</span></span>|
|<span data-ttu-id="fb9ad-116">mac</span><span class="sxs-lookup"><span data-stu-id="fb9ad-116">mac</span></span>|<span data-ttu-id="fb9ad-117">Binario</span><span class="sxs-lookup"><span data-stu-id="fb9ad-117">Binary</span></span>|<span data-ttu-id="fb9ad-118">El hash del contenido del archivo cifrado + IV (hash de contenido).</span><span class="sxs-lookup"><span data-stu-id="fb9ad-118">The hash of the encrypted file content + IV (content hash).</span></span>|
|<span data-ttu-id="fb9ad-119">macKey</span><span class="sxs-lookup"><span data-stu-id="fb9ad-119">macKey</span></span>|<span data-ttu-id="fb9ad-120">Binario</span><span class="sxs-lookup"><span data-stu-id="fb9ad-120">Binary</span></span>|<span data-ttu-id="fb9ad-121">La clave utilizada para obtener el MAC.</span><span class="sxs-lookup"><span data-stu-id="fb9ad-121">The key used to get mac.</span></span>|
|<span data-ttu-id="fb9ad-122">profileIdentifier</span><span class="sxs-lookup"><span data-stu-id="fb9ad-122">profileIdentifier</span></span>|<span data-ttu-id="fb9ad-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="fb9ad-123">String</span></span>|<span data-ttu-id="fb9ad-124">El identificador del perfil.</span><span class="sxs-lookup"><span data-stu-id="fb9ad-124">The the profile identifier.</span></span>|
|<span data-ttu-id="fb9ad-125">fileDigest</span><span class="sxs-lookup"><span data-stu-id="fb9ad-125">fileDigest</span></span>|<span data-ttu-id="fb9ad-126">Binario</span><span class="sxs-lookup"><span data-stu-id="fb9ad-126">Binary</span></span>|<span data-ttu-id="fb9ad-127">El resumen de los archivos antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="fb9ad-127">The file digest prior to encryption.</span></span>|
|<span data-ttu-id="fb9ad-128">fileDigestAlgorithm</span><span class="sxs-lookup"><span data-stu-id="fb9ad-128">fileDigestAlgorithm</span></span>|<span data-ttu-id="fb9ad-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="fb9ad-129">String</span></span>|<span data-ttu-id="fb9ad-130">El algoritmo del resumen de los archivos.</span><span class="sxs-lookup"><span data-stu-id="fb9ad-130">The file digest algorithm.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fb9ad-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fb9ad-131">Relationships</span></span>
<span data-ttu-id="fb9ad-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fb9ad-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fb9ad-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fb9ad-133">JSON Representation</span></span>
<span data-ttu-id="fb9ad-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fb9ad-134">Here is a JSON representation of the resource.</span></span>
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



