---
title: Tipo de recurso fileEncryptionInfo
description: Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ed56f695da8dece64702472cd3822603e02dd8b6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840694"
---
# <a name="fileencryptioninfo-resource-type"></a><span data-ttu-id="93092-103">Tipo de recurso fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="93092-103">fileEncryptionInfo resource type</span></span>

> <span data-ttu-id="93092-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="93092-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="93092-105">Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="93092-105">Contains properties for file encryption information for the content version of a line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="93092-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93092-106">Properties</span></span>
|<span data-ttu-id="93092-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="93092-107">Property</span></span>|<span data-ttu-id="93092-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="93092-108">Type</span></span>|<span data-ttu-id="93092-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="93092-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="93092-110">encryptionKey</span><span class="sxs-lookup"><span data-stu-id="93092-110">encryptionKey</span></span>|<span data-ttu-id="93092-111">Binario</span><span class="sxs-lookup"><span data-stu-id="93092-111">Binary</span></span>|<span data-ttu-id="93092-112">La clave que se usa para cifrar el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="93092-112">The key used to encrypt the file content.</span></span>|
|<span data-ttu-id="93092-113">initializationVector</span><span class="sxs-lookup"><span data-stu-id="93092-113">initializationVector</span></span>|<span data-ttu-id="93092-114">Binario</span><span class="sxs-lookup"><span data-stu-id="93092-114">Binary</span></span>|<span data-ttu-id="93092-115">El vector de inicialización utilizado para el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="93092-115">The initialization vector used for the encryption algorithm.</span></span>|
|<span data-ttu-id="93092-116">mac</span><span class="sxs-lookup"><span data-stu-id="93092-116">mac</span></span>|<span data-ttu-id="93092-117">Binario</span><span class="sxs-lookup"><span data-stu-id="93092-117">Binary</span></span>|<span data-ttu-id="93092-118">El hash del contenido del archivo cifrado + IV (hash de contenido).</span><span class="sxs-lookup"><span data-stu-id="93092-118">The hash of the encrypted file content + IV (content hash).</span></span>|
|<span data-ttu-id="93092-119">macKey</span><span class="sxs-lookup"><span data-stu-id="93092-119">macKey</span></span>|<span data-ttu-id="93092-120">Binario</span><span class="sxs-lookup"><span data-stu-id="93092-120">Binary</span></span>|<span data-ttu-id="93092-121">La clave utilizada para obtener el MAC.</span><span class="sxs-lookup"><span data-stu-id="93092-121">The key used to get mac.</span></span>|
|<span data-ttu-id="93092-122">profileIdentifier</span><span class="sxs-lookup"><span data-stu-id="93092-122">profileIdentifier</span></span>|<span data-ttu-id="93092-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="93092-123">String</span></span>|<span data-ttu-id="93092-124">El identificador del perfil.</span><span class="sxs-lookup"><span data-stu-id="93092-124">The the profile identifier.</span></span>|
|<span data-ttu-id="93092-125">fileDigest</span><span class="sxs-lookup"><span data-stu-id="93092-125">fileDigest</span></span>|<span data-ttu-id="93092-126">Binario</span><span class="sxs-lookup"><span data-stu-id="93092-126">Binary</span></span>|<span data-ttu-id="93092-127">El resumen de los archivos antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="93092-127">The file digest prior to encryption.</span></span>|
|<span data-ttu-id="93092-128">fileDigestAlgorithm</span><span class="sxs-lookup"><span data-stu-id="93092-128">fileDigestAlgorithm</span></span>|<span data-ttu-id="93092-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="93092-129">String</span></span>|<span data-ttu-id="93092-130">El algoritmo del resumen de los archivos.</span><span class="sxs-lookup"><span data-stu-id="93092-130">The file digest algorithm.</span></span>|

## <a name="relationships"></a><span data-ttu-id="93092-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="93092-131">Relationships</span></span>
<span data-ttu-id="93092-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="93092-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="93092-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="93092-133">JSON Representation</span></span>
<span data-ttu-id="93092-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="93092-134">Here is a JSON representation of the resource.</span></span>
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



