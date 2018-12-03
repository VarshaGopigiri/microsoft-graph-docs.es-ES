---
title: Tipo de recurso fileEncryptionInfo
description: Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.
ms.openlocfilehash: 17895b0bf081cc249f9081c737a2445683514280
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084193"
---
# <a name="fileencryptioninfo-resource-type"></a><span data-ttu-id="c1712-103">Tipo de recurso fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="c1712-103">fileEncryptionInfo resource type</span></span>

> <span data-ttu-id="c1712-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c1712-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c1712-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c1712-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c1712-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c1712-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c1712-107">Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="c1712-107">Contains properties for file encryption information for the content version of a line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="c1712-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1712-108">Properties</span></span>
|<span data-ttu-id="c1712-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c1712-109">Property</span></span>|<span data-ttu-id="c1712-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1712-110">Type</span></span>|<span data-ttu-id="c1712-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1712-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c1712-112">encryptionKey</span><span class="sxs-lookup"><span data-stu-id="c1712-112">encryptionKey</span></span>|<span data-ttu-id="c1712-113">Binario</span><span class="sxs-lookup"><span data-stu-id="c1712-113">Binary</span></span>|<span data-ttu-id="c1712-114">La clave que se usa para cifrar el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="c1712-114">The key used to encrypt the file content.</span></span>|
|<span data-ttu-id="c1712-115">initializationVector</span><span class="sxs-lookup"><span data-stu-id="c1712-115">initializationVector</span></span>|<span data-ttu-id="c1712-116">Binario</span><span class="sxs-lookup"><span data-stu-id="c1712-116">Binary</span></span>|<span data-ttu-id="c1712-117">El vector de inicialización utilizado para el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="c1712-117">The initialization vector used for the encryption algorithm.</span></span>|
|<span data-ttu-id="c1712-118">mac</span><span class="sxs-lookup"><span data-stu-id="c1712-118">mac</span></span>|<span data-ttu-id="c1712-119">Binario</span><span class="sxs-lookup"><span data-stu-id="c1712-119">Binary</span></span>|<span data-ttu-id="c1712-120">El hash del contenido del archivo cifrado + IV (hash de contenido).</span><span class="sxs-lookup"><span data-stu-id="c1712-120">The hash of the encrypted file content + IV (content hash).</span></span>|
|<span data-ttu-id="c1712-121">macKey</span><span class="sxs-lookup"><span data-stu-id="c1712-121">macKey</span></span>|<span data-ttu-id="c1712-122">Binario</span><span class="sxs-lookup"><span data-stu-id="c1712-122">Binary</span></span>|<span data-ttu-id="c1712-123">La clave utilizada para obtener el MAC.</span><span class="sxs-lookup"><span data-stu-id="c1712-123">The key used to get mac.</span></span>|
|<span data-ttu-id="c1712-124">profileIdentifier</span><span class="sxs-lookup"><span data-stu-id="c1712-124">profileIdentifier</span></span>|<span data-ttu-id="c1712-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="c1712-125">String</span></span>|<span data-ttu-id="c1712-126">El identificador del perfil.</span><span class="sxs-lookup"><span data-stu-id="c1712-126">The the profile identifier.</span></span>|
|<span data-ttu-id="c1712-127">fileDigest</span><span class="sxs-lookup"><span data-stu-id="c1712-127">fileDigest</span></span>|<span data-ttu-id="c1712-128">Binario</span><span class="sxs-lookup"><span data-stu-id="c1712-128">Binary</span></span>|<span data-ttu-id="c1712-129">El resumen de los archivos antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="c1712-129">The file digest prior to encryption.</span></span>|
|<span data-ttu-id="c1712-130">fileDigestAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c1712-130">fileDigestAlgorithm</span></span>|<span data-ttu-id="c1712-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="c1712-131">String</span></span>|<span data-ttu-id="c1712-132">El algoritmo del resumen de los archivos.</span><span class="sxs-lookup"><span data-stu-id="c1712-132">The file digest algorithm.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c1712-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c1712-133">Relationships</span></span>
<span data-ttu-id="c1712-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c1712-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c1712-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c1712-135">JSON Representation</span></span>
<span data-ttu-id="c1712-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c1712-136">Here is a JSON representation of the resource.</span></span>
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




