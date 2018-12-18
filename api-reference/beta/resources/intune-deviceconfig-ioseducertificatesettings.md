---
title: tipo de recurso iosEduCertificateSettings
description: Confianza certificados raíz y PFX para iOS EDU.
author: tfitzmac
ms.openlocfilehash: 8e373a7c878dd06870b13a32c428f837d741964c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332329"
---
# <a name="ioseducertificatesettings-resource-type"></a><span data-ttu-id="466cc-103">tipo de recurso iosEduCertificateSettings</span><span class="sxs-lookup"><span data-stu-id="466cc-103">iosEduCertificateSettings resource type</span></span>

> <span data-ttu-id="466cc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="466cc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="466cc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="466cc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="466cc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="466cc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="466cc-107">Confianza certificados raíz y PFX para iOS EDU.</span><span class="sxs-lookup"><span data-stu-id="466cc-107">Trusted Root and PFX certificates for iOS EDU.</span></span>
## <a name="properties"></a><span data-ttu-id="466cc-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="466cc-108">Properties</span></span>
|<span data-ttu-id="466cc-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="466cc-109">Property</span></span>|<span data-ttu-id="466cc-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="466cc-110">Type</span></span>|<span data-ttu-id="466cc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="466cc-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="466cc-112">trustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="466cc-112">trustedRootCertificate</span></span>|<span data-ttu-id="466cc-113">Binario</span><span class="sxs-lookup"><span data-stu-id="466cc-113">Binary</span></span>|<span data-ttu-id="466cc-114">Certificado raíz de confianza.</span><span class="sxs-lookup"><span data-stu-id="466cc-114">Trusted Root Certificate.</span></span>|
|<span data-ttu-id="466cc-115">certFileName</span><span class="sxs-lookup"><span data-stu-id="466cc-115">certFileName</span></span>|<span data-ttu-id="466cc-116">String</span><span class="sxs-lookup"><span data-stu-id="466cc-116">String</span></span>|<span data-ttu-id="466cc-117">Nombre de archivo para mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="466cc-117">File name to display in UI.</span></span>|
|<span data-ttu-id="466cc-118">certificationAuthority</span><span class="sxs-lookup"><span data-stu-id="466cc-118">certificationAuthority</span></span>|<span data-ttu-id="466cc-119">String</span><span class="sxs-lookup"><span data-stu-id="466cc-119">String</span></span>|<span data-ttu-id="466cc-120">Entidad de certificación PKCS.</span><span class="sxs-lookup"><span data-stu-id="466cc-120">PKCS Certification Authority.</span></span>|
|<span data-ttu-id="466cc-121">certificationAuthorityName</span><span class="sxs-lookup"><span data-stu-id="466cc-121">certificationAuthorityName</span></span>|<span data-ttu-id="466cc-122">String</span><span class="sxs-lookup"><span data-stu-id="466cc-122">String</span></span>|<span data-ttu-id="466cc-123">Nombre de la autoridad de certificación PKCS.</span><span class="sxs-lookup"><span data-stu-id="466cc-123">PKCS Certification Authority Name.</span></span>|
|<span data-ttu-id="466cc-124">certificateTemplateName</span><span class="sxs-lookup"><span data-stu-id="466cc-124">certificateTemplateName</span></span>|<span data-ttu-id="466cc-125">String</span><span class="sxs-lookup"><span data-stu-id="466cc-125">String</span></span>|<span data-ttu-id="466cc-126">Nombre de la plantilla de certificado PKCS.</span><span class="sxs-lookup"><span data-stu-id="466cc-126">PKCS Certificate Template Name.</span></span>|
|<span data-ttu-id="466cc-127">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="466cc-127">renewalThresholdPercentage</span></span>|<span data-ttu-id="466cc-128">Int32</span><span class="sxs-lookup"><span data-stu-id="466cc-128">Int32</span></span>|<span data-ttu-id="466cc-129">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="466cc-129">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="466cc-130">Valores válidos de 1 a 99</span><span class="sxs-lookup"><span data-stu-id="466cc-130">Valid values 1 to 99</span></span>|
|<span data-ttu-id="466cc-131">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="466cc-131">certificateValidityPeriodValue</span></span>|<span data-ttu-id="466cc-132">Int32</span><span class="sxs-lookup"><span data-stu-id="466cc-132">Int32</span></span>|<span data-ttu-id="466cc-133">Valor para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="466cc-133">Value for the Certificate Validity Period.</span></span>|
|<span data-ttu-id="466cc-134">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="466cc-134">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="466cc-135">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="466cc-135">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="466cc-136">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="466cc-136">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="466cc-137">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="466cc-137">Possible values are: `days`, `months`, `years`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="466cc-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="466cc-138">Relationships</span></span>
<span data-ttu-id="466cc-139">Ninguna</span><span class="sxs-lookup"><span data-stu-id="466cc-139">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="466cc-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="466cc-140">JSON Representation</span></span>
<span data-ttu-id="466cc-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="466cc-141">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosEduCertificateSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosEduCertificateSettings",
  "trustedRootCertificate": "binary",
  "certFileName": "String",
  "certificationAuthority": "String",
  "certificationAuthorityName": "String",
  "certificateTemplateName": "String",
  "renewalThresholdPercentage": 1024,
  "certificateValidityPeriodValue": 1024,
  "certificateValidityPeriodScale": "String"
}
```





