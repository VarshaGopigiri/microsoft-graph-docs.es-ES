---
title: Tipo de recurso fileEncryptionInfo
description: Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 18ff7b9d64473048b6d1d45069ab19549c83e0df
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960122"
---
# <a name="fileencryptioninfo-resource-type"></a><span data-ttu-id="f60e7-103">Tipo de recurso fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="f60e7-103">fileEncryptionInfo resource type</span></span>

> <span data-ttu-id="f60e7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f60e7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f60e7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f60e7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f60e7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f60e7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f60e7-107">Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="f60e7-107">Contains properties for file encryption information for the content version of a line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="f60e7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f60e7-108">Properties</span></span>
|<span data-ttu-id="f60e7-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f60e7-109">Property</span></span>|<span data-ttu-id="f60e7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f60e7-110">Type</span></span>|<span data-ttu-id="f60e7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f60e7-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f60e7-112">encryptionKey</span><span class="sxs-lookup"><span data-stu-id="f60e7-112">encryptionKey</span></span>|<span data-ttu-id="f60e7-113">Binario</span><span class="sxs-lookup"><span data-stu-id="f60e7-113">Binary</span></span>|<span data-ttu-id="f60e7-114">La clave que se usa para cifrar el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="f60e7-114">The key used to encrypt the file content.</span></span>|
|<span data-ttu-id="f60e7-115">initializationVector</span><span class="sxs-lookup"><span data-stu-id="f60e7-115">initializationVector</span></span>|<span data-ttu-id="f60e7-116">Binario</span><span class="sxs-lookup"><span data-stu-id="f60e7-116">Binary</span></span>|<span data-ttu-id="f60e7-117">El vector de inicialización utilizado para el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="f60e7-117">The initialization vector used for the encryption algorithm.</span></span>|
|<span data-ttu-id="f60e7-118">mac</span><span class="sxs-lookup"><span data-stu-id="f60e7-118">mac</span></span>|<span data-ttu-id="f60e7-119">Binario</span><span class="sxs-lookup"><span data-stu-id="f60e7-119">Binary</span></span>|<span data-ttu-id="f60e7-120">El hash del contenido del archivo cifrado + IV (hash de contenido).</span><span class="sxs-lookup"><span data-stu-id="f60e7-120">The hash of the encrypted file content + IV (content hash).</span></span>|
|<span data-ttu-id="f60e7-121">macKey</span><span class="sxs-lookup"><span data-stu-id="f60e7-121">macKey</span></span>|<span data-ttu-id="f60e7-122">Binario</span><span class="sxs-lookup"><span data-stu-id="f60e7-122">Binary</span></span>|<span data-ttu-id="f60e7-123">La clave utilizada para obtener el MAC.</span><span class="sxs-lookup"><span data-stu-id="f60e7-123">The key used to get mac.</span></span>|
|<span data-ttu-id="f60e7-124">profileIdentifier</span><span class="sxs-lookup"><span data-stu-id="f60e7-124">profileIdentifier</span></span>|<span data-ttu-id="f60e7-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="f60e7-125">String</span></span>|<span data-ttu-id="f60e7-126">El identificador del perfil.</span><span class="sxs-lookup"><span data-stu-id="f60e7-126">The the profile identifier.</span></span>|
|<span data-ttu-id="f60e7-127">fileDigest</span><span class="sxs-lookup"><span data-stu-id="f60e7-127">fileDigest</span></span>|<span data-ttu-id="f60e7-128">Binario</span><span class="sxs-lookup"><span data-stu-id="f60e7-128">Binary</span></span>|<span data-ttu-id="f60e7-129">El resumen de los archivos antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="f60e7-129">The file digest prior to encryption.</span></span>|
|<span data-ttu-id="f60e7-130">fileDigestAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f60e7-130">fileDigestAlgorithm</span></span>|<span data-ttu-id="f60e7-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="f60e7-131">String</span></span>|<span data-ttu-id="f60e7-132">El algoritmo del resumen de los archivos.</span><span class="sxs-lookup"><span data-stu-id="f60e7-132">The file digest algorithm.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f60e7-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f60e7-133">Relationships</span></span>
<span data-ttu-id="f60e7-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f60e7-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f60e7-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f60e7-135">JSON Representation</span></span>
<span data-ttu-id="f60e7-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f60e7-136">Here is a JSON representation of the resource.</span></span>
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





