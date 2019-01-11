---
title: Eliminar iosPkcsCertificateProfile
description: Elimina un iosPkcsCertificateProfile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 854cb6295be9b1f2d8283baef7afa90d98bf8c88
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813002"
---
# <a name="delete-iospkcscertificateprofile"></a><span data-ttu-id="a17aa-103">Eliminar iosPkcsCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="a17aa-103">Delete iosPkcsCertificateProfile</span></span>

> <span data-ttu-id="a17aa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a17aa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a17aa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a17aa-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a17aa-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a17aa-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a17aa-107">Elimina un [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="a17aa-107">Deletes a [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a17aa-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a17aa-108">Prerequisites</span></span>
<span data-ttu-id="a17aa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a17aa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a17aa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a17aa-111">Permission type</span></span>|<span data-ttu-id="a17aa-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a17aa-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a17aa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a17aa-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a17aa-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a17aa-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a17aa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a17aa-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a17aa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a17aa-116">Not supported.</span></span>|
|<span data-ttu-id="a17aa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a17aa-117">Application</span></span>|<span data-ttu-id="a17aa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a17aa-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a17aa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a17aa-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="a17aa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a17aa-120">Request headers</span></span>
|<span data-ttu-id="a17aa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a17aa-121">Header</span></span>|<span data-ttu-id="a17aa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a17aa-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a17aa-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a17aa-123">Authorization</span></span>|<span data-ttu-id="a17aa-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a17aa-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a17aa-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a17aa-125">Accept</span></span>|<span data-ttu-id="a17aa-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a17aa-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a17aa-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a17aa-127">Request body</span></span>
<span data-ttu-id="a17aa-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a17aa-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a17aa-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a17aa-129">Response</span></span>
<span data-ttu-id="a17aa-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a17aa-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="a17aa-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a17aa-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="a17aa-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a17aa-132">Request</span></span>
<span data-ttu-id="a17aa-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a17aa-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="a17aa-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a17aa-134">Response</span></span>
<span data-ttu-id="a17aa-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a17aa-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





