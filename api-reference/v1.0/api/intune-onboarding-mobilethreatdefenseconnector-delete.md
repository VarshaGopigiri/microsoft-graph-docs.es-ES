---
title: Eliminar mobileThreatDefenseConnector
description: Elimina un mobileThreatDefenseConnector.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 24a7f91cb7fe545d0cac9f8c7acacabd0dcb5855
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845573"
---
# <a name="delete-mobilethreatdefenseconnector"></a><span data-ttu-id="30c1f-103">Eliminar mobileThreatDefenseConnector</span><span class="sxs-lookup"><span data-stu-id="30c1f-103">Delete mobileThreatDefenseConnector</span></span>

> <span data-ttu-id="30c1f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="30c1f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="30c1f-105">Elimina un [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="30c1f-105">Deletes a [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="30c1f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="30c1f-106">Prerequisites</span></span>
<span data-ttu-id="30c1f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="30c1f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="30c1f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30c1f-109">Permission type</span></span>|<span data-ttu-id="30c1f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30c1f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="30c1f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30c1f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="30c1f-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="30c1f-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="30c1f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30c1f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="30c1f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30c1f-114">Not supported.</span></span>|
|<span data-ttu-id="30c1f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30c1f-115">Application</span></span>|<span data-ttu-id="30c1f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30c1f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="30c1f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30c1f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="30c1f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30c1f-118">Request headers</span></span>
|<span data-ttu-id="30c1f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30c1f-119">Header</span></span>|<span data-ttu-id="30c1f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="30c1f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="30c1f-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="30c1f-121">Authorization</span></span>|<span data-ttu-id="30c1f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="30c1f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="30c1f-123">Accept</span><span class="sxs-lookup"><span data-stu-id="30c1f-123">Accept</span></span>|<span data-ttu-id="30c1f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="30c1f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="30c1f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30c1f-125">Request body</span></span>
<span data-ttu-id="30c1f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="30c1f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="30c1f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30c1f-127">Response</span></span>
<span data-ttu-id="30c1f-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="30c1f-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="30c1f-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30c1f-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="30c1f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30c1f-130">Request</span></span>
<span data-ttu-id="30c1f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30c1f-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
```

### <a name="response"></a><span data-ttu-id="30c1f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30c1f-132">Response</span></span>
<span data-ttu-id="30c1f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30c1f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



