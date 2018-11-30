---
title: Actualizar telecomExpenseManagementPartner
description: Actualice las propiedades de un objeto telecomExpenseManagementPartner.
ms.openlocfilehash: 600ceb9fc5f7ec00659438516772d37867a8a207
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029019"
---
# <a name="update-telecomexpensemanagementpartner"></a><span data-ttu-id="6fe78-103">Actualizar telecomExpenseManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6fe78-103">Update telecomExpenseManagementPartner</span></span>

> <span data-ttu-id="6fe78-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6fe78-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6fe78-105">Actualice las propiedades de un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="6fe78-105">Update the properties of a [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6fe78-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6fe78-106">Prerequisites</span></span>
<span data-ttu-id="6fe78-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6fe78-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6fe78-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6fe78-109">Permission type</span></span>|<span data-ttu-id="6fe78-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6fe78-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6fe78-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6fe78-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6fe78-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6fe78-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="6fe78-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6fe78-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6fe78-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6fe78-114">Not supported.</span></span>|
|<span data-ttu-id="6fe78-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6fe78-115">Application</span></span>|<span data-ttu-id="6fe78-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6fe78-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6fe78-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6fe78-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/telecomExpenseManagementPartners/{telecomExpenseManagementPartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="6fe78-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6fe78-118">Request headers</span></span>
|<span data-ttu-id="6fe78-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fe78-119">Header</span></span>|<span data-ttu-id="6fe78-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6fe78-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6fe78-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6fe78-121">Authorization</span></span>|<span data-ttu-id="6fe78-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6fe78-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6fe78-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6fe78-123">Accept</span></span>|<span data-ttu-id="6fe78-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6fe78-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6fe78-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6fe78-125">Request body</span></span>
<span data-ttu-id="6fe78-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="6fe78-126">In the request body, supply a JSON representation for the [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object.</span></span>

<span data-ttu-id="6fe78-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="6fe78-127">The following table shows the properties that are required when you create the [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span></span>

|<span data-ttu-id="6fe78-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6fe78-128">Property</span></span>|<span data-ttu-id="6fe78-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6fe78-129">Type</span></span>|<span data-ttu-id="6fe78-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fe78-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6fe78-131">id</span><span class="sxs-lookup"><span data-stu-id="6fe78-131">id</span></span>|<span data-ttu-id="6fe78-132">String</span><span class="sxs-lookup"><span data-stu-id="6fe78-132">String</span></span>|<span data-ttu-id="6fe78-133">Identificador único del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="6fe78-133">Unique identifier of the TEM partner.</span></span>|
|<span data-ttu-id="6fe78-134">displayName</span><span class="sxs-lookup"><span data-stu-id="6fe78-134">displayName</span></span>|<span data-ttu-id="6fe78-135">String</span><span class="sxs-lookup"><span data-stu-id="6fe78-135">String</span></span>|<span data-ttu-id="6fe78-136">Nombre para mostrar del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="6fe78-136">Display name of the TEM partner.</span></span>|
|<span data-ttu-id="6fe78-137">url</span><span class="sxs-lookup"><span data-stu-id="6fe78-137">url</span></span>|<span data-ttu-id="6fe78-138">String</span><span class="sxs-lookup"><span data-stu-id="6fe78-138">String</span></span>|<span data-ttu-id="6fe78-139">Dirección URL del panel de control administrativo del partner de TEM, donde un administrador puede configurar el servicio de su TEM.</span><span class="sxs-lookup"><span data-stu-id="6fe78-139">URL of the TEM partner's administrative control panel, where an administrator can configure their TEM service.</span></span>|
|<span data-ttu-id="6fe78-140">appAuthorized</span><span class="sxs-lookup"><span data-stu-id="6fe78-140">appAuthorized</span></span>|<span data-ttu-id="6fe78-141">Booleano</span><span class="sxs-lookup"><span data-stu-id="6fe78-141">Boolean</span></span>|<span data-ttu-id="6fe78-142">Si se ha autorizado a la aplicación de AAD del partner para que obtenga acceso a Intune.</span><span class="sxs-lookup"><span data-stu-id="6fe78-142">Whether the partner's AAD app has been authorized to access Intune.</span></span>|
|<span data-ttu-id="6fe78-143">enabled</span><span class="sxs-lookup"><span data-stu-id="6fe78-143">enabled</span></span>|<span data-ttu-id="6fe78-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="6fe78-144">Boolean</span></span>|<span data-ttu-id="6fe78-145">Si la conexión de Intune al servicio de TEM está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="6fe78-145">Whether Intune's connection to the TEM service is currently enabled or disabled.</span></span>|
|<span data-ttu-id="6fe78-146">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="6fe78-146">lastConnectionDateTime</span></span>|<span data-ttu-id="6fe78-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6fe78-147">DateTimeOffset</span></span>|<span data-ttu-id="6fe78-148">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="6fe78-148">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="6fe78-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6fe78-149">Response</span></span>
<span data-ttu-id="6fe78-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fe78-150">If successful, this method returns a `200 OK` response code and an updated [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6fe78-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fe78-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="6fe78-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6fe78-152">Request</span></span>
<span data-ttu-id="6fe78-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6fe78-153">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/telecomExpenseManagementPartners/{telecomExpenseManagementPartnerId}
Content-type: application/json
Content-length: 248

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```

### <a name="response"></a><span data-ttu-id="6fe78-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6fe78-154">Response</span></span>
<span data-ttu-id="6fe78-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6fe78-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 297

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "id": "47a3b399-b399-47a3-99b3-a34799b3a347",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```


