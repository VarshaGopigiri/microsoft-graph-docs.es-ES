---
title: Eliminar deviceCategory
description: Elimina un deviceCategory.
ms.openlocfilehash: a85190a47bca7ec58d899be3618ae59229ecef06
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032643"
---
# <a name="delete-devicecategory"></a><span data-ttu-id="08946-103">Eliminar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="08946-103">Delete deviceCategory</span></span>

> <span data-ttu-id="08946-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="08946-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="08946-105">Elimina un [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="08946-105">Deletes a [deviceCategory](../resources/intune-shared-devicecategory.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="08946-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="08946-106">Prerequisites</span></span>
<span data-ttu-id="08946-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="08946-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="08946-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="08946-109">Permission type</span></span>|<span data-ttu-id="08946-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="08946-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="08946-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="08946-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="08946-112">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="08946-112">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="08946-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="08946-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="08946-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="08946-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="08946-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08946-115">Not supported.</span></span>|
|<span data-ttu-id="08946-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="08946-116">Application</span></span>|<span data-ttu-id="08946-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08946-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="08946-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08946-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceCategories/{deviceCategoryId}
```

## <a name="request-headers"></a><span data-ttu-id="08946-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08946-119">Request headers</span></span>
|<span data-ttu-id="08946-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08946-120">Header</span></span>|<span data-ttu-id="08946-121">Valor</span><span class="sxs-lookup"><span data-stu-id="08946-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="08946-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="08946-122">Authorization</span></span>|<span data-ttu-id="08946-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="08946-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="08946-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="08946-124">Accept</span></span>|<span data-ttu-id="08946-125">application/json</span><span class="sxs-lookup"><span data-stu-id="08946-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="08946-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08946-126">Request body</span></span>
<span data-ttu-id="08946-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="08946-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="08946-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08946-128">Response</span></span>
<span data-ttu-id="08946-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="08946-129">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="08946-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08946-130">Example</span></span>
### <a name="request"></a><span data-ttu-id="08946-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08946-131">Request</span></span>
<span data-ttu-id="08946-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08946-132">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories/{deviceCategoryId}
```

### <a name="response"></a><span data-ttu-id="08946-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08946-133">Response</span></span>
<span data-ttu-id="08946-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="08946-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



