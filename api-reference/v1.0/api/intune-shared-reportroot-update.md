---
title: Actualizar reportRoot
description: Actualice las propiedades de un objeto reportRoot.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ba6c192b69975eef2f60b09f5bb2fc43e43d51b7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885193"
---
# <a name="update-reportroot"></a><span data-ttu-id="72261-103">Actualizar reportRoot</span><span class="sxs-lookup"><span data-stu-id="72261-103">Update reportRoot</span></span>

> <span data-ttu-id="72261-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="72261-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="72261-105">Actualice las propiedades de un objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="72261-105">Update the properties of a [reportRoot](../resources/intune-shared-reportroot.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="72261-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="72261-106">Prerequisites</span></span>
<span data-ttu-id="72261-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="72261-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="72261-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="72261-109">Permission type</span></span>|<span data-ttu-id="72261-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="72261-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="72261-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="72261-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="72261-112">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="72261-112">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="72261-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="72261-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
| <span data-ttu-id="72261-114">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="72261-114">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="72261-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="72261-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="72261-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="72261-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="72261-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="72261-117">Not supported.</span></span>|
|<span data-ttu-id="72261-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="72261-118">Application</span></span>|<span data-ttu-id="72261-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="72261-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="72261-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="72261-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /reports
```

## <a name="request-headers"></a><span data-ttu-id="72261-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="72261-121">Request headers</span></span>
|<span data-ttu-id="72261-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72261-122">Header</span></span>|<span data-ttu-id="72261-123">Valor</span><span class="sxs-lookup"><span data-stu-id="72261-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="72261-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="72261-124">Authorization</span></span>|<span data-ttu-id="72261-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="72261-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="72261-126">Accept</span><span class="sxs-lookup"><span data-stu-id="72261-126">Accept</span></span>|<span data-ttu-id="72261-127">application/json</span><span class="sxs-lookup"><span data-stu-id="72261-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="72261-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="72261-128">Request body</span></span>
<span data-ttu-id="72261-129">En el cuerpo de la solicitud, especifique una representación JSON del objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="72261-129">In the request body, supply a JSON representation for the [reportRoot](../resources/intune-shared-reportroot.md) object.</span></span>

<span data-ttu-id="72261-130">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="72261-130">The following table shows the properties that are required when you create the [reportRoot](../resources/intune-shared-reportroot.md).</span></span>

|<span data-ttu-id="72261-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72261-131">Property</span></span>|<span data-ttu-id="72261-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="72261-132">Type</span></span>|<span data-ttu-id="72261-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="72261-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="72261-134">id</span><span class="sxs-lookup"><span data-stu-id="72261-134">id</span></span>|<span data-ttu-id="72261-135">String</span><span class="sxs-lookup"><span data-stu-id="72261-135">String</span></span>|<span data-ttu-id="72261-136">El identificador único de esta entidad.</span><span class="sxs-lookup"><span data-stu-id="72261-136">The unique identifier for this entity.</span></span>|



## <a name="response"></a><span data-ttu-id="72261-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72261-137">Response</span></span>
<span data-ttu-id="72261-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [reportRoot](../resources/intune-shared-reportroot.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72261-138">If successful, this method returns a `200 OK` response code and an updated [reportRoot](../resources/intune-shared-reportroot.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="72261-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72261-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="72261-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="72261-140">Request</span></span>
<span data-ttu-id="72261-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="72261-141">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/reports
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="72261-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72261-142">Response</span></span>
<span data-ttu-id="72261-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="72261-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 101

{
  "@odata.type": "#microsoft.graph.reportRoot",
  "id": "9ab6b3dd-b3dd-9ab6-ddb3-b69addb3b69a"
}
```








