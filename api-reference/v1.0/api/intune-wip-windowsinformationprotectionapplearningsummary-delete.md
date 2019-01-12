---
title: Eliminar windowsInformationProtectionAppLearningSummary
description: Elimina un windowsInformationProtectionAppLearningSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0bf4b378f756e6f6c634484c24cdc396b734feef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970776"
---
# <a name="delete-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="1e543-103">Eliminar windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="1e543-103">Delete windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="1e543-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1e543-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1e543-105">Elimina un [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="1e543-105">Deletes a [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1e543-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1e543-106">Prerequisites</span></span>
<span data-ttu-id="1e543-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1e543-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1e543-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1e543-109">Permission type</span></span>|<span data-ttu-id="1e543-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1e543-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1e543-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1e543-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1e543-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1e543-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1e543-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1e543-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1e543-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e543-114">Not supported.</span></span>|
|<span data-ttu-id="1e543-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1e543-115">Application</span></span>|<span data-ttu-id="1e543-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e543-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1e543-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1e543-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="1e543-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1e543-118">Request headers</span></span>
|<span data-ttu-id="1e543-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e543-119">Header</span></span>|<span data-ttu-id="1e543-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1e543-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1e543-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1e543-121">Authorization</span></span>|<span data-ttu-id="1e543-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1e543-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1e543-123">Accept</span><span class="sxs-lookup"><span data-stu-id="1e543-123">Accept</span></span>|<span data-ttu-id="1e543-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1e543-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1e543-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1e543-125">Request body</span></span>
<span data-ttu-id="1e543-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1e543-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1e543-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e543-127">Response</span></span>
<span data-ttu-id="1e543-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="1e543-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="1e543-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e543-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="1e543-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1e543-130">Request</span></span>
<span data-ttu-id="1e543-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1e543-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
```

### <a name="response"></a><span data-ttu-id="1e543-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e543-132">Response</span></span>
<span data-ttu-id="1e543-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1e543-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



