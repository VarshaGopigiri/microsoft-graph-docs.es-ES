---
title: Actualizar reportRoot
description: Actualice las propiedades de un objeto reportRoot.
author: tfitzmac
ms.openlocfilehash: 4f3d0e297a9b7d122e9b21afd7555c1af307d2d9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349535"
---
# <a name="update-reportroot"></a><span data-ttu-id="8e34f-103">Actualizar reportRoot</span><span class="sxs-lookup"><span data-stu-id="8e34f-103">Update reportRoot</span></span>

> <span data-ttu-id="8e34f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8e34f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8e34f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8e34f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8e34f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8e34f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8e34f-107">Actualice las propiedades de un objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="8e34f-107">Update the properties of a [reportRoot](../resources/intune-shared-reportroot.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8e34f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8e34f-108">Prerequisites</span></span>
<span data-ttu-id="8e34f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8e34f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8e34f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8e34f-111">Permission type</span></span>|<span data-ttu-id="8e34f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8e34f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8e34f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8e34f-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="8e34f-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="8e34f-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="8e34f-115">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8e34f-115">DeviceManagementConfiguration.ReadWrite.All</span></span>|
| <span data-ttu-id="8e34f-116">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="8e34f-116">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="8e34f-117">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8e34f-117">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="8e34f-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8e34f-118">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8e34f-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8e34f-119">Not supported.</span></span>|
|<span data-ttu-id="8e34f-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8e34f-120">Application</span></span>|<span data-ttu-id="8e34f-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8e34f-121">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8e34f-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8e34f-122">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /reports
```

## <a name="request-headers"></a><span data-ttu-id="8e34f-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8e34f-123">Request headers</span></span>
|<span data-ttu-id="8e34f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e34f-124">Header</span></span>|<span data-ttu-id="8e34f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8e34f-125">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8e34f-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="8e34f-126">Authorization</span></span>|<span data-ttu-id="8e34f-127">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8e34f-127">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8e34f-128">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8e34f-128">Accept</span></span>|<span data-ttu-id="8e34f-129">application/json</span><span class="sxs-lookup"><span data-stu-id="8e34f-129">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8e34f-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8e34f-130">Request body</span></span>
<span data-ttu-id="8e34f-131">En el cuerpo de la solicitud, especifique una representación JSON del objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="8e34f-131">In the request body, supply a JSON representation for the [reportRoot](../resources/intune-shared-reportroot.md) object.</span></span>

<span data-ttu-id="8e34f-132">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="8e34f-132">The following table shows the properties that are required when you create the [reportRoot](../resources/intune-shared-reportroot.md).</span></span>

|<span data-ttu-id="8e34f-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8e34f-133">Property</span></span>|<span data-ttu-id="8e34f-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e34f-134">Type</span></span>|<span data-ttu-id="8e34f-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e34f-135">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8e34f-136">id</span><span class="sxs-lookup"><span data-stu-id="8e34f-136">id</span></span>|<span data-ttu-id="8e34f-137">String</span><span class="sxs-lookup"><span data-stu-id="8e34f-137">String</span></span>|<span data-ttu-id="8e34f-138">El identificador único de esta entidad.</span><span class="sxs-lookup"><span data-stu-id="8e34f-138">The unique identifier for this entity.</span></span>|



## <a name="response"></a><span data-ttu-id="8e34f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8e34f-139">Response</span></span>
<span data-ttu-id="8e34f-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [reportRoot](../resources/intune-shared-reportroot.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e34f-140">If successful, this method returns a `200 OK` response code and an updated [reportRoot](../resources/intune-shared-reportroot.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8e34f-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8e34f-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="8e34f-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8e34f-142">Request</span></span>
<span data-ttu-id="8e34f-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8e34f-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/reports
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="8e34f-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8e34f-144">Response</span></span>
<span data-ttu-id="8e34f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8e34f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 101

{
  "@odata.type": "#microsoft.graph.reportRoot",
  "id": "9ab6b3dd-b3dd-9ab6-ddb3-b69addb3b69a"
}
```



