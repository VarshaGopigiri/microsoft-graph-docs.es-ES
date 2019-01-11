---
title: Eliminar detectedApp
description: Elimina un detectedApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5813194fe3b24f115525bd7be9463a343e21f8eb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809320"
---
# <a name="delete-detectedapp"></a><span data-ttu-id="42564-103">Eliminar detectedApp</span><span class="sxs-lookup"><span data-stu-id="42564-103">Delete detectedApp</span></span>

> <span data-ttu-id="42564-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="42564-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="42564-105">Elimina un [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="42564-105">Deletes a [detectedApp](../resources/intune-devices-detectedapp.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="42564-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="42564-106">Prerequisites</span></span>
<span data-ttu-id="42564-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="42564-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="42564-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="42564-109">Permission type</span></span>|<span data-ttu-id="42564-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="42564-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="42564-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="42564-111">Delegated (work or school account)</span></span>|<span data-ttu-id="42564-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="42564-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="42564-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="42564-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="42564-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42564-114">Not supported.</span></span>|
|<span data-ttu-id="42564-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="42564-115">Application</span></span>|<span data-ttu-id="42564-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42564-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="42564-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="42564-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/detectedApps/{detectedAppId}
```

## <a name="request-headers"></a><span data-ttu-id="42564-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="42564-118">Request headers</span></span>
|<span data-ttu-id="42564-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42564-119">Header</span></span>|<span data-ttu-id="42564-120">Valor</span><span class="sxs-lookup"><span data-stu-id="42564-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="42564-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="42564-121">Authorization</span></span>|<span data-ttu-id="42564-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="42564-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="42564-123">Accept</span><span class="sxs-lookup"><span data-stu-id="42564-123">Accept</span></span>|<span data-ttu-id="42564-124">application/json</span><span class="sxs-lookup"><span data-stu-id="42564-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="42564-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="42564-125">Request body</span></span>
<span data-ttu-id="42564-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="42564-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="42564-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42564-127">Response</span></span>
<span data-ttu-id="42564-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="42564-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="42564-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="42564-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="42564-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="42564-130">Request</span></span>
<span data-ttu-id="42564-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42564-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/detectedApps/{detectedAppId}
```

### <a name="response"></a><span data-ttu-id="42564-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42564-132">Response</span></span>
<span data-ttu-id="42564-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="42564-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



