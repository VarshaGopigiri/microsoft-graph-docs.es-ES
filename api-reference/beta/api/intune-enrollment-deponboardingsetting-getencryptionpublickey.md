---
title: getEncryptionPublicKey (función)
description: Obtener una clave pública se utiliza para cifrar el programa de inscripción de dispositivos de Apple símbolo (token)
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: eb373b862dc39d9636e59bf32ba00b84b7bf5563
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807633"
---
# <a name="getencryptionpublickey-function"></a><span data-ttu-id="e979a-103">getEncryptionPublicKey (función)</span><span class="sxs-lookup"><span data-stu-id="e979a-103">getEncryptionPublicKey function</span></span>

> <span data-ttu-id="e979a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e979a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e979a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e979a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e979a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e979a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e979a-107">Obtener una clave pública se utiliza para cifrar el programa de inscripción de dispositivos de Apple símbolo (token)</span><span class="sxs-lookup"><span data-stu-id="e979a-107">Get a public key to use to encrypt the Apple device enrollment program token</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e979a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e979a-108">Prerequisites</span></span>
<span data-ttu-id="e979a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e979a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e979a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e979a-111">Permission type</span></span>|<span data-ttu-id="e979a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e979a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e979a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e979a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e979a-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="e979a-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="e979a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e979a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e979a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e979a-116">Not supported.</span></span>|
|<span data-ttu-id="e979a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e979a-117">Application</span></span>|<span data-ttu-id="e979a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e979a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e979a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e979a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/getEncryptionPublicKey
```

## <a name="request-headers"></a><span data-ttu-id="e979a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e979a-120">Request headers</span></span>
|<span data-ttu-id="e979a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e979a-121">Header</span></span>|<span data-ttu-id="e979a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e979a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e979a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e979a-123">Authorization</span></span>|<span data-ttu-id="e979a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e979a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e979a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e979a-125">Accept</span></span>|<span data-ttu-id="e979a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e979a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e979a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e979a-127">Request body</span></span>
<span data-ttu-id="e979a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e979a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e979a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e979a-129">Response</span></span>
<span data-ttu-id="e979a-130">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un objeto String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e979a-130">If successful, this function returns a `200 OK` response code and a String in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e979a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e979a-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="e979a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e979a-132">Request</span></span>
<span data-ttu-id="e979a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e979a-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/getEncryptionPublicKey
```

### <a name="response"></a><span data-ttu-id="e979a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e979a-134">Response</span></span>
<span data-ttu-id="e979a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e979a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 50

{
  "value": "Get Encryption Public Key value"
}
```





