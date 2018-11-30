---
title: Eliminar sharedPCConfiguration
description: Elimina un sharedPCConfiguration.
ms.openlocfilehash: 88612ac179482e7db7d957cc668030467afc88f7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030444"
---
# <a name="delete-sharedpcconfiguration"></a><span data-ttu-id="aa0d8-103">Eliminar sharedPCConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa0d8-103">Delete sharedPCConfiguration</span></span>

> <span data-ttu-id="aa0d8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aa0d8-105">Elimina un [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="aa0d8-105">Deletes a [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="aa0d8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aa0d8-106">Prerequisites</span></span>
<span data-ttu-id="aa0d8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aa0d8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aa0d8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aa0d8-109">Permission type</span></span>|<span data-ttu-id="aa0d8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aa0d8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="aa0d8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aa0d8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="aa0d8-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aa0d8-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="aa0d8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aa0d8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="aa0d8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-114">Not supported.</span></span>|
|<span data-ttu-id="aa0d8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aa0d8-115">Application</span></span>|<span data-ttu-id="aa0d8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="aa0d8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa0d8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="aa0d8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa0d8-118">Request headers</span></span>
|<span data-ttu-id="aa0d8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa0d8-119">Header</span></span>|<span data-ttu-id="aa0d8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="aa0d8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="aa0d8-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="aa0d8-121">Authorization</span></span>|<span data-ttu-id="aa0d8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="aa0d8-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="aa0d8-123">Accept</span></span>|<span data-ttu-id="aa0d8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="aa0d8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="aa0d8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa0d8-125">Request body</span></span>
<span data-ttu-id="aa0d8-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="aa0d8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa0d8-127">Response</span></span>
<span data-ttu-id="aa0d8-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="aa0d8-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa0d8-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="aa0d8-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa0d8-130">Request</span></span>
<span data-ttu-id="aa0d8-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="aa0d8-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa0d8-132">Response</span></span>
<span data-ttu-id="aa0d8-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



