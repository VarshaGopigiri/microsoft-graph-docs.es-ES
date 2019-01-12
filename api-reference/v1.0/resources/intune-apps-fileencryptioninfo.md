---
title: Tipo de recurso fileEncryptionInfo
description: Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5642c76e7d09d1113f2fccc68fc7b1db8ba0ffde
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931604"
---
# <a name="fileencryptioninfo-resource-type"></a><span data-ttu-id="daf28-103">Tipo de recurso fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="daf28-103">fileEncryptionInfo resource type</span></span>

> <span data-ttu-id="daf28-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="daf28-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="daf28-105">Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="daf28-105">Contains properties for file encryption information for the content version of a line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="daf28-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="daf28-106">Properties</span></span>
|<span data-ttu-id="daf28-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="daf28-107">Property</span></span>|<span data-ttu-id="daf28-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="daf28-108">Type</span></span>|<span data-ttu-id="daf28-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="daf28-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="daf28-110">encryptionKey</span><span class="sxs-lookup"><span data-stu-id="daf28-110">encryptionKey</span></span>|<span data-ttu-id="daf28-111">Binario</span><span class="sxs-lookup"><span data-stu-id="daf28-111">Binary</span></span>|<span data-ttu-id="daf28-112">La clave que se usa para cifrar el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="daf28-112">The key used to encrypt the file content.</span></span>|
|<span data-ttu-id="daf28-113">initializationVector</span><span class="sxs-lookup"><span data-stu-id="daf28-113">initializationVector</span></span>|<span data-ttu-id="daf28-114">Binario</span><span class="sxs-lookup"><span data-stu-id="daf28-114">Binary</span></span>|<span data-ttu-id="daf28-115">El vector de inicialización utilizado para el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="daf28-115">The initialization vector used for the encryption algorithm.</span></span>|
|<span data-ttu-id="daf28-116">mac</span><span class="sxs-lookup"><span data-stu-id="daf28-116">mac</span></span>|<span data-ttu-id="daf28-117">Binario</span><span class="sxs-lookup"><span data-stu-id="daf28-117">Binary</span></span>|<span data-ttu-id="daf28-118">El hash del contenido del archivo cifrado + IV (hash de contenido).</span><span class="sxs-lookup"><span data-stu-id="daf28-118">The hash of the encrypted file content + IV (content hash).</span></span>|
|<span data-ttu-id="daf28-119">macKey</span><span class="sxs-lookup"><span data-stu-id="daf28-119">macKey</span></span>|<span data-ttu-id="daf28-120">Binario</span><span class="sxs-lookup"><span data-stu-id="daf28-120">Binary</span></span>|<span data-ttu-id="daf28-121">La clave utilizada para obtener el MAC.</span><span class="sxs-lookup"><span data-stu-id="daf28-121">The key used to get mac.</span></span>|
|<span data-ttu-id="daf28-122">profileIdentifier</span><span class="sxs-lookup"><span data-stu-id="daf28-122">profileIdentifier</span></span>|<span data-ttu-id="daf28-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="daf28-123">String</span></span>|<span data-ttu-id="daf28-124">El identificador del perfil.</span><span class="sxs-lookup"><span data-stu-id="daf28-124">The the profile identifier.</span></span>|
|<span data-ttu-id="daf28-125">fileDigest</span><span class="sxs-lookup"><span data-stu-id="daf28-125">fileDigest</span></span>|<span data-ttu-id="daf28-126">Binario</span><span class="sxs-lookup"><span data-stu-id="daf28-126">Binary</span></span>|<span data-ttu-id="daf28-127">El resumen de los archivos antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="daf28-127">The file digest prior to encryption.</span></span>|
|<span data-ttu-id="daf28-128">fileDigestAlgorithm</span><span class="sxs-lookup"><span data-stu-id="daf28-128">fileDigestAlgorithm</span></span>|<span data-ttu-id="daf28-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="daf28-129">String</span></span>|<span data-ttu-id="daf28-130">El algoritmo del resumen de los archivos.</span><span class="sxs-lookup"><span data-stu-id="daf28-130">The file digest algorithm.</span></span>|

## <a name="relationships"></a><span data-ttu-id="daf28-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="daf28-131">Relationships</span></span>
<span data-ttu-id="daf28-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="daf28-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="daf28-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="daf28-133">JSON Representation</span></span>
<span data-ttu-id="daf28-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="daf28-134">Here is a JSON representation of the resource.</span></span>
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



