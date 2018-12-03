---
title: Actualizar windowsManagementApp
description: Actualizar las propiedades de un objeto windowsManagementApp.
ms.openlocfilehash: 88a0511a06c94a4c5298fc53fa19b512f723177d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084790"
---
# <a name="update-windowsmanagementapp"></a><span data-ttu-id="2cf96-103">Actualizar windowsManagementApp</span><span class="sxs-lookup"><span data-stu-id="2cf96-103">Update windowsManagementApp</span></span>

> <span data-ttu-id="2cf96-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2cf96-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2cf96-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2cf96-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2cf96-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2cf96-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2cf96-107">Actualizar las propiedades de un objeto [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) .</span><span class="sxs-lookup"><span data-stu-id="2cf96-107">Update the properties of a [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2cf96-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2cf96-108">Prerequisites</span></span>
<span data-ttu-id="2cf96-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2cf96-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2cf96-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2cf96-111">Permission type</span></span>|<span data-ttu-id="2cf96-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2cf96-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2cf96-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2cf96-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2cf96-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cf96-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="2cf96-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2cf96-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2cf96-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2cf96-116">Not supported.</span></span>|
|<span data-ttu-id="2cf96-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2cf96-117">Application</span></span>|<span data-ttu-id="2cf96-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2cf96-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2cf96-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2cf96-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/windowsManagementApp
```

## <a name="request-headers"></a><span data-ttu-id="2cf96-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2cf96-120">Request headers</span></span>
|<span data-ttu-id="2cf96-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cf96-121">Header</span></span>|<span data-ttu-id="2cf96-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2cf96-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2cf96-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="2cf96-123">Authorization</span></span>|<span data-ttu-id="2cf96-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2cf96-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2cf96-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2cf96-125">Accept</span></span>|<span data-ttu-id="2cf96-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2cf96-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2cf96-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2cf96-127">Request body</span></span>
<span data-ttu-id="2cf96-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) .</span><span class="sxs-lookup"><span data-stu-id="2cf96-128">In the request body, supply a JSON representation for the [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) object.</span></span>

<span data-ttu-id="2cf96-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md).</span><span class="sxs-lookup"><span data-stu-id="2cf96-129">The following table shows the properties that are required when you create the [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md).</span></span>

|<span data-ttu-id="2cf96-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2cf96-130">Property</span></span>|<span data-ttu-id="2cf96-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2cf96-131">Type</span></span>|<span data-ttu-id="2cf96-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cf96-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2cf96-133">id</span><span class="sxs-lookup"><span data-stu-id="2cf96-133">id</span></span>|<span data-ttu-id="2cf96-134">String</span><span class="sxs-lookup"><span data-stu-id="2cf96-134">String</span></span>|<span data-ttu-id="2cf96-135">Identificador único para la aplicación de administración de Windows</span><span class="sxs-lookup"><span data-stu-id="2cf96-135">Unique Identifier for the Windows management app</span></span>|
|<span data-ttu-id="2cf96-136">availableVersion</span><span class="sxs-lookup"><span data-stu-id="2cf96-136">availableVersion</span></span>|<span data-ttu-id="2cf96-137">String</span><span class="sxs-lookup"><span data-stu-id="2cf96-137">String</span></span>|<span data-ttu-id="2cf96-138">Versión disponible de Windows management app.</span><span class="sxs-lookup"><span data-stu-id="2cf96-138">Windows management app available version.</span></span>|



## <a name="response"></a><span data-ttu-id="2cf96-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cf96-139">Response</span></span>
<span data-ttu-id="2cf96-140">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cf96-140">If successful, this method returns a `200 OK` response code and an updated [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2cf96-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cf96-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="2cf96-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2cf96-142">Request</span></span>
<span data-ttu-id="2cf96-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2cf96-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/windowsManagementApp
Content-type: application/json
Content-length: 53

{
  "availableVersion": "Available Version value"
}
```

### <a name="response"></a><span data-ttu-id="2cf96-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cf96-144">Response</span></span>
<span data-ttu-id="2cf96-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2cf96-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 161

{
  "@odata.type": "#microsoft.graph.windowsManagementApp",
  "id": "5facc79c-c79c-5fac-9cc7-ac5f9cc7ac5f",
  "availableVersion": "Available Version value"
}
```




