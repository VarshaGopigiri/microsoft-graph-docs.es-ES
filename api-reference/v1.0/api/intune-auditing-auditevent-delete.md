---
title: Eliminar auditEvent
description: Elimina un auditEvent.
author: tfitzmac
ms.openlocfilehash: 1a0393e46ecd54cadc28a603067f3b8c91366812
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307094"
---
# <a name="delete-auditevent"></a><span data-ttu-id="b5328-103">Eliminar auditEvent</span><span class="sxs-lookup"><span data-stu-id="b5328-103">Delete auditEvent</span></span>

> <span data-ttu-id="b5328-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b5328-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b5328-105">Elimina un [auditEvent](../resources/intune-auditing-auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="b5328-105">Deletes a [auditEvent](../resources/intune-auditing-auditevent.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b5328-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b5328-106">Prerequisites</span></span>
<span data-ttu-id="b5328-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b5328-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b5328-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b5328-109">Permission type</span></span>|<span data-ttu-id="b5328-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b5328-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b5328-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b5328-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b5328-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b5328-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b5328-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b5328-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b5328-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5328-114">Not supported.</span></span>|
|<span data-ttu-id="b5328-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b5328-115">Application</span></span>|<span data-ttu-id="b5328-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5328-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b5328-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b5328-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/auditEvents/{auditEventId}
```

## <a name="request-headers"></a><span data-ttu-id="b5328-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b5328-118">Request headers</span></span>
|<span data-ttu-id="b5328-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5328-119">Header</span></span>|<span data-ttu-id="b5328-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b5328-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b5328-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b5328-121">Authorization</span></span>|<span data-ttu-id="b5328-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b5328-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b5328-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b5328-123">Accept</span></span>|<span data-ttu-id="b5328-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b5328-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b5328-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b5328-125">Request body</span></span>
<span data-ttu-id="b5328-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b5328-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b5328-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5328-127">Response</span></span>
<span data-ttu-id="b5328-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b5328-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b5328-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5328-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="b5328-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b5328-130">Request</span></span>
<span data-ttu-id="b5328-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b5328-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/auditEvents/{auditEventId}
```

### <a name="response"></a><span data-ttu-id="b5328-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5328-132">Response</span></span>
<span data-ttu-id="b5328-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b5328-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



