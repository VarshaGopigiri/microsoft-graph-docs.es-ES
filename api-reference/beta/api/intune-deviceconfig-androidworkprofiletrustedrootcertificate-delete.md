---
title: Eliminar androidWorkProfileTrustedRootCertificate
description: Elimina un androidWorkProfileTrustedRootCertificate.
author: tfitzmac
ms.openlocfilehash: 8d597c8a852a6069e12c952ab00f304457b1e847
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344929"
---
# <a name="delete-androidworkprofiletrustedrootcertificate"></a><span data-ttu-id="477b4-103">Eliminar androidWorkProfileTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="477b4-103">Delete androidWorkProfileTrustedRootCertificate</span></span>

> <span data-ttu-id="477b4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="477b4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="477b4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="477b4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="477b4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="477b4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="477b4-107">Elimina un [androidWorkProfileTrustedRootCertificate](../resources/intune-deviceconfig-androidworkprofiletrustedrootcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="477b4-107">Deletes a [androidWorkProfileTrustedRootCertificate](../resources/intune-deviceconfig-androidworkprofiletrustedrootcertificate.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="477b4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="477b4-108">Prerequisites</span></span>
<span data-ttu-id="477b4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="477b4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="477b4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="477b4-111">Permission type</span></span>|<span data-ttu-id="477b4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="477b4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="477b4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="477b4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="477b4-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="477b4-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="477b4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="477b4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="477b4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="477b4-116">Not supported.</span></span>|
|<span data-ttu-id="477b4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="477b4-117">Application</span></span>|<span data-ttu-id="477b4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="477b4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="477b4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="477b4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidWorkProfileCertificateProfileBase/rootCertificate
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidWorkProfileEnterpriseWiFiConfiguration/rootCertificateForServerValidation
```

## <a name="request-headers"></a><span data-ttu-id="477b4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="477b4-120">Request headers</span></span>
|<span data-ttu-id="477b4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="477b4-121">Header</span></span>|<span data-ttu-id="477b4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="477b4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="477b4-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="477b4-123">Authorization</span></span>|<span data-ttu-id="477b4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="477b4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="477b4-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="477b4-125">Accept</span></span>|<span data-ttu-id="477b4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="477b4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="477b4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="477b4-127">Request body</span></span>
<span data-ttu-id="477b4-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="477b4-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="477b4-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="477b4-129">Response</span></span>
<span data-ttu-id="477b4-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="477b4-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="477b4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="477b4-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="477b4-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="477b4-132">Request</span></span>
<span data-ttu-id="477b4-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="477b4-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate
```

### <a name="response"></a><span data-ttu-id="477b4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="477b4-134">Response</span></span>
<span data-ttu-id="477b4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="477b4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





