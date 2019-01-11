---
title: tipo de recurso symantecCodeSigningCertificate
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a2e4f53e0ca7329f163b507677e2b91a4c02fe12
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845013"
---
# <a name="symanteccodesigningcertificate-resource-type"></a><span data-ttu-id="87294-103">tipo de recurso symantecCodeSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="87294-103">symantecCodeSigningCertificate resource type</span></span>

> <span data-ttu-id="87294-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="87294-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="87294-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="87294-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="87294-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="87294-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="87294-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="87294-107">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="87294-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="87294-108">Methods</span></span>
|<span data-ttu-id="87294-109">Método</span><span class="sxs-lookup"><span data-stu-id="87294-109">Method</span></span>|<span data-ttu-id="87294-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87294-110">Return Type</span></span>|<span data-ttu-id="87294-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="87294-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="87294-112">Obtener symantecCodeSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="87294-112">Get symantecCodeSigningCertificate</span></span>](../api/intune-apps-symanteccodesigningcertificate-get.md)|[<span data-ttu-id="87294-113">symantecCodeSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="87294-113">symantecCodeSigningCertificate</span></span>](../resources/intune-apps-symanteccodesigningcertificate.md)|<span data-ttu-id="87294-114">Leer las propiedades y las relaciones del objeto [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="87294-114">Read properties and relationships of the [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) object.</span></span>|
|[<span data-ttu-id="87294-115">Actualizar symantecCodeSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="87294-115">Update symantecCodeSigningCertificate</span></span>](../api/intune-apps-symanteccodesigningcertificate-update.md)|[<span data-ttu-id="87294-116">symantecCodeSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="87294-116">symantecCodeSigningCertificate</span></span>](../resources/intune-apps-symanteccodesigningcertificate.md)|<span data-ttu-id="87294-117">Actualizar las propiedades de un objeto [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="87294-117">Update the properties of a [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="87294-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="87294-118">Properties</span></span>
|<span data-ttu-id="87294-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="87294-119">Property</span></span>|<span data-ttu-id="87294-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="87294-120">Type</span></span>|<span data-ttu-id="87294-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="87294-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="87294-122">id</span><span class="sxs-lookup"><span data-stu-id="87294-122">id</span></span>|<span data-ttu-id="87294-123">String</span><span class="sxs-lookup"><span data-stu-id="87294-123">String</span></span>|<span data-ttu-id="87294-124">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="87294-124">The key of the entity.</span></span>|
|<span data-ttu-id="87294-125">content</span><span class="sxs-lookup"><span data-stu-id="87294-125">content</span></span>|<span data-ttu-id="87294-126">Binario</span><span class="sxs-lookup"><span data-stu-id="87294-126">Binary</span></span>|<span data-ttu-id="87294-127">El certificado de firma de código de Symantec de Windows en el formato de datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="87294-127">The Windows Symantec Code-Signing Certificate in the raw data format.</span></span>|
|<span data-ttu-id="87294-128">status</span><span class="sxs-lookup"><span data-stu-id="87294-128">status</span></span>|[<span data-ttu-id="87294-129">certificateStatus</span><span class="sxs-lookup"><span data-stu-id="87294-129">certificateStatus</span></span>](../resources/intune-apps-certificatestatus.md)|<span data-ttu-id="87294-130">El estado de Cert aprovisiona o no configurado.</span><span class="sxs-lookup"><span data-stu-id="87294-130">The Cert Status Provisioned or not Provisioned.</span></span> <span data-ttu-id="87294-131">Los valores posibles son: `notProvisioned` y `provisioned`.</span><span class="sxs-lookup"><span data-stu-id="87294-131">Possible values are: `notProvisioned`, `provisioned`.</span></span>|
|<span data-ttu-id="87294-132">password</span><span class="sxs-lookup"><span data-stu-id="87294-132">password</span></span>|<span data-ttu-id="87294-133">String</span><span class="sxs-lookup"><span data-stu-id="87294-133">String</span></span>|<span data-ttu-id="87294-134">La contraseña requerida para el archivo .pfx.</span><span class="sxs-lookup"><span data-stu-id="87294-134">The Password required for .pfx file.</span></span>|
|<span data-ttu-id="87294-135">subjectName</span><span class="sxs-lookup"><span data-stu-id="87294-135">subjectName</span></span>|<span data-ttu-id="87294-136">cadena</span><span class="sxs-lookup"><span data-stu-id="87294-136">String</span></span>|<span data-ttu-id="87294-137">El nombre de sujeto para el certificado.</span><span class="sxs-lookup"><span data-stu-id="87294-137">The Subject Name for the cert.</span></span>|
|<span data-ttu-id="87294-138">subject</span><span class="sxs-lookup"><span data-stu-id="87294-138">subject</span></span>|<span data-ttu-id="87294-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="87294-139">String</span></span>|<span data-ttu-id="87294-140">El valor de asunto para el certificado.</span><span class="sxs-lookup"><span data-stu-id="87294-140">The Subject value for the cert.</span></span>|
|<span data-ttu-id="87294-141">issuerName</span><span class="sxs-lookup"><span data-stu-id="87294-141">issuerName</span></span>|<span data-ttu-id="87294-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="87294-142">String</span></span>|<span data-ttu-id="87294-143">El nombre para el certificado del emisor.</span><span class="sxs-lookup"><span data-stu-id="87294-143">The Issuer Name for the cert.</span></span>|
|<span data-ttu-id="87294-144">emisor</span><span class="sxs-lookup"><span data-stu-id="87294-144">issuer</span></span>|<span data-ttu-id="87294-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="87294-145">String</span></span>|<span data-ttu-id="87294-146">El valor de emisor para el certificado.</span><span class="sxs-lookup"><span data-stu-id="87294-146">The Issuer value for the cert.</span></span>|
|<span data-ttu-id="87294-147">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="87294-147">expirationDateTime</span></span>|<span data-ttu-id="87294-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="87294-148">DateTimeOffset</span></span>|<span data-ttu-id="87294-149">La fecha de caducidad del certificado.</span><span class="sxs-lookup"><span data-stu-id="87294-149">The Cert Expiration Date.</span></span>|
|<span data-ttu-id="87294-150">uploadDateTime</span><span class="sxs-lookup"><span data-stu-id="87294-150">uploadDateTime</span></span>|<span data-ttu-id="87294-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="87294-151">DateTimeOffset</span></span>|<span data-ttu-id="87294-152">El tipo del certificado de firma de código como Symantec Cert.</span><span class="sxs-lookup"><span data-stu-id="87294-152">The Type of the CodeSigning Cert as Symantec Cert.</span></span>|

## <a name="relationships"></a><span data-ttu-id="87294-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="87294-153">Relationships</span></span>
<span data-ttu-id="87294-154">Ninguna</span><span class="sxs-lookup"><span data-stu-id="87294-154">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="87294-155">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="87294-155">JSON Representation</span></span>
<span data-ttu-id="87294-156">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="87294-156">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.symantecCodeSigningCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.symantecCodeSigningCertificate",
  "id": "String (identifier)",
  "content": "binary",
  "status": "String",
  "password": "String",
  "subjectName": "String",
  "subject": "String",
  "issuerName": "String",
  "issuer": "String",
  "expirationDateTime": "String (timestamp)",
  "uploadDateTime": "String (timestamp)"
}
```





