---
title: tipo de recurso bitLockerSystemDrivePolicy
description: Directivas de Base de cifrado BitLocker.
ms.openlocfilehash: 60388f020750ebd7f187b07777440b013ae5f02a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085582"
---
# <a name="bitlockersystemdrivepolicy-resource-type"></a><span data-ttu-id="fc61c-103">tipo de recurso bitLockerSystemDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="fc61c-103">bitLockerSystemDrivePolicy resource type</span></span>

> <span data-ttu-id="fc61c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fc61c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fc61c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fc61c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fc61c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fc61c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fc61c-107">Directivas de Base de cifrado BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fc61c-107">BitLocker Encryption Base Policies.</span></span>
## <a name="properties"></a><span data-ttu-id="fc61c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc61c-108">Properties</span></span>
|<span data-ttu-id="fc61c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc61c-109">Property</span></span>|<span data-ttu-id="fc61c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc61c-110">Type</span></span>|<span data-ttu-id="fc61c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc61c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fc61c-112">encryptionMethod</span><span class="sxs-lookup"><span data-stu-id="fc61c-112">encryptionMethod</span></span>|[<span data-ttu-id="fc61c-113">bitLockerEncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="fc61c-113">bitLockerEncryptionMethod</span></span>](../resources/intune-deviceconfig-bitlockerencryptionmethod.md)|<span data-ttu-id="fc61c-114">Seleccione el método de cifrado para unidades de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc61c-114">Select the encryption method for operating system drives.</span></span> <span data-ttu-id="fc61c-115">Los valores posibles son: `aesCbc128`, `aesCbc256`, `xtsAes128` y `xtsAes256`.</span><span class="sxs-lookup"><span data-stu-id="fc61c-115">Possible values are: `aesCbc128`, `aesCbc256`, `xtsAes128`, `xtsAes256`.</span></span>|
|<span data-ttu-id="fc61c-116">startupAuthenticationRequired</span><span class="sxs-lookup"><span data-stu-id="fc61c-116">startupAuthenticationRequired</span></span>|<span data-ttu-id="fc61c-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="fc61c-117">Boolean</span></span>|<span data-ttu-id="fc61c-118">Requerir autenticación adicional al inicio.</span><span class="sxs-lookup"><span data-stu-id="fc61c-118">Require additional authentication at startup.</span></span>|
|<span data-ttu-id="fc61c-119">startupAuthenticationBlockWithoutTpmChip</span><span class="sxs-lookup"><span data-stu-id="fc61c-119">startupAuthenticationBlockWithoutTpmChip</span></span>|<span data-ttu-id="fc61c-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="fc61c-120">Boolean</span></span>|<span data-ttu-id="fc61c-121">Indica si se debe permitir BitLocker sin un TPM compatible (se requiere una contraseña o una clave de inicio en una unidad flash USB).</span><span class="sxs-lookup"><span data-stu-id="fc61c-121">Indicates whether to allow BitLocker without a compatible TPM (requires a password or a startup key on a USB flash drive).</span></span>|
|<span data-ttu-id="fc61c-122">startupAuthenticationTpmUsage</span><span class="sxs-lookup"><span data-stu-id="fc61c-122">startupAuthenticationTpmUsage</span></span>|[<span data-ttu-id="fc61c-123">configurationUsage</span><span class="sxs-lookup"><span data-stu-id="fc61c-123">configurationUsage</span></span>](../resources/intune-deviceconfig-configurationusage.md)|<span data-ttu-id="fc61c-124">Indica si el inicio TPM es permitido o necesario o desactivarse.</span><span class="sxs-lookup"><span data-stu-id="fc61c-124">Indicates if TPM startup is allowed/required/disallowed.</span></span> <span data-ttu-id="fc61c-125">Los valores posibles son: `blocked`, `required` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="fc61c-125">Possible values are: `blocked`, `required`, `allowed`.</span></span>|
|<span data-ttu-id="fc61c-126">startupAuthenticationTpmPinUsage</span><span class="sxs-lookup"><span data-stu-id="fc61c-126">startupAuthenticationTpmPinUsage</span></span>|[<span data-ttu-id="fc61c-127">configurationUsage</span><span class="sxs-lookup"><span data-stu-id="fc61c-127">configurationUsage</span></span>](../resources/intune-deviceconfig-configurationusage.md)|<span data-ttu-id="fc61c-128">Indica si el pin de inicio TPM es permitido o necesario o desactivarse.</span><span class="sxs-lookup"><span data-stu-id="fc61c-128">Indicates if TPM startup pin is allowed/required/disallowed.</span></span> <span data-ttu-id="fc61c-129">Los valores posibles son: `blocked`, `required` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="fc61c-129">Possible values are: `blocked`, `required`, `allowed`.</span></span>|
|<span data-ttu-id="fc61c-130">startupAuthenticationTpmKeyUsage</span><span class="sxs-lookup"><span data-stu-id="fc61c-130">startupAuthenticationTpmKeyUsage</span></span>|[<span data-ttu-id="fc61c-131">configurationUsage</span><span class="sxs-lookup"><span data-stu-id="fc61c-131">configurationUsage</span></span>](../resources/intune-deviceconfig-configurationusage.md)|<span data-ttu-id="fc61c-132">Indica si la clave de inicio TPM es permitido o necesario o desactivarse.</span><span class="sxs-lookup"><span data-stu-id="fc61c-132">Indicates if TPM startup key is allowed/required/disallowed.</span></span> <span data-ttu-id="fc61c-133">Los valores posibles son: `blocked`, `required` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="fc61c-133">Possible values are: `blocked`, `required`, `allowed`.</span></span>|
|<span data-ttu-id="fc61c-134">startupAuthenticationTpmPinAndKeyUsage</span><span class="sxs-lookup"><span data-stu-id="fc61c-134">startupAuthenticationTpmPinAndKeyUsage</span></span>|[<span data-ttu-id="fc61c-135">configurationUsage</span><span class="sxs-lookup"><span data-stu-id="fc61c-135">configurationUsage</span></span>](../resources/intune-deviceconfig-configurationusage.md)|<span data-ttu-id="fc61c-136">Indica si el inicio TPM fijar claves y son permitidos o necesario o desactivarse.</span><span class="sxs-lookup"><span data-stu-id="fc61c-136">Indicates if TPM startup pin key and key are allowed/required/disallowed.</span></span> <span data-ttu-id="fc61c-137">Los valores posibles son: `blocked`, `required` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="fc61c-137">Possible values are: `blocked`, `required`, `allowed`.</span></span>|
|<span data-ttu-id="fc61c-138">minimumPinLength</span><span class="sxs-lookup"><span data-stu-id="fc61c-138">minimumPinLength</span></span>|<span data-ttu-id="fc61c-139">Int32</span><span class="sxs-lookup"><span data-stu-id="fc61c-139">Int32</span></span>|<span data-ttu-id="fc61c-140">Indica la longitud mínima de pin de inicio.</span><span class="sxs-lookup"><span data-stu-id="fc61c-140">Indicates the minimum length of startup pin.</span></span> <span data-ttu-id="fc61c-141">Valores válidos de 4 a 20</span><span class="sxs-lookup"><span data-stu-id="fc61c-141">Valid values 4 to 20</span></span>|
|<span data-ttu-id="fc61c-142">recoveryOptions</span><span class="sxs-lookup"><span data-stu-id="fc61c-142">recoveryOptions</span></span>|[<span data-ttu-id="fc61c-143">bitLockerRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="fc61c-143">bitLockerRecoveryOptions</span></span>](../resources/intune-deviceconfig-bitlockerrecoveryoptions.md)|<span data-ttu-id="fc61c-144">Permite recuperar unidades de sistema operativo de BitLocker cifrada en ausencia de la información de clave de inicio requerido.</span><span class="sxs-lookup"><span data-stu-id="fc61c-144">Allows to recover BitLocker encrypted operating system drives in the absence of the required startup key information.</span></span> <span data-ttu-id="fc61c-145">Esta configuración de directiva se aplica al activar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fc61c-145">This policy setting is applied when you turn on BitLocker.</span></span>|
|<span data-ttu-id="fc61c-146">prebootRecoveryEnableMessageAndUrl</span><span class="sxs-lookup"><span data-stu-id="fc61c-146">prebootRecoveryEnableMessageAndUrl</span></span>|<span data-ttu-id="fc61c-147">Booleano</span><span class="sxs-lookup"><span data-stu-id="fc61c-147">Boolean</span></span>|<span data-ttu-id="fc61c-148">Habilitar el mensaje de arranque previo a la recuperación y la dirección Url.</span><span class="sxs-lookup"><span data-stu-id="fc61c-148">Enable pre-boot recovery message and Url.</span></span> <span data-ttu-id="fc61c-149">Si requireStartupAuthentication es false, no afecta este valor.</span><span class="sxs-lookup"><span data-stu-id="fc61c-149">If requireStartupAuthentication is false, this value does not affect.</span></span>|
|<span data-ttu-id="fc61c-150">prebootRecoveryMessage</span><span class="sxs-lookup"><span data-stu-id="fc61c-150">prebootRecoveryMessage</span></span>|<span data-ttu-id="fc61c-151">String</span><span class="sxs-lookup"><span data-stu-id="fc61c-151">String</span></span>|<span data-ttu-id="fc61c-152">Define un mensaje de recuperación personalizada.</span><span class="sxs-lookup"><span data-stu-id="fc61c-152">Defines a custom recovery message.</span></span>|
|<span data-ttu-id="fc61c-153">prebootRecoveryUrl</span><span class="sxs-lookup"><span data-stu-id="fc61c-153">prebootRecoveryUrl</span></span>|<span data-ttu-id="fc61c-154">String</span><span class="sxs-lookup"><span data-stu-id="fc61c-154">String</span></span>|<span data-ttu-id="fc61c-155">Define una dirección URL de recuperación personalizada.</span><span class="sxs-lookup"><span data-stu-id="fc61c-155">Defines a custom recovery URL.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fc61c-156">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fc61c-156">Relationships</span></span>
<span data-ttu-id="fc61c-157">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fc61c-157">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fc61c-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fc61c-158">JSON Representation</span></span>
<span data-ttu-id="fc61c-159">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fc61c-159">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerSystemDrivePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerSystemDrivePolicy",
  "encryptionMethod": "String",
  "startupAuthenticationRequired": true,
  "startupAuthenticationBlockWithoutTpmChip": true,
  "startupAuthenticationTpmUsage": "String",
  "startupAuthenticationTpmPinUsage": "String",
  "startupAuthenticationTpmKeyUsage": "String",
  "startupAuthenticationTpmPinAndKeyUsage": "String",
  "minimumPinLength": 1024,
  "recoveryOptions": {
    "@odata.type": "microsoft.graph.bitLockerRecoveryOptions",
    "blockDataRecoveryAgent": true,
    "recoveryPasswordUsage": "String",
    "recoveryKeyUsage": "String",
    "hideRecoveryOptions": true,
    "enableRecoveryInformationSaveToStore": true,
    "recoveryInformationToStore": "String",
    "enableBitLockerAfterRecoveryInformationToStore": true
  },
  "prebootRecoveryEnableMessageAndUrl": true,
  "prebootRecoveryMessage": "String",
  "prebootRecoveryUrl": "String"
}
```





