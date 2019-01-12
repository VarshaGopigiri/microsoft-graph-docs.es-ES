---
title: Crear usuario
description: Crea un objeto de usuario nuevo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 10670accfe99a545cd6adb1532f34de3b229b26c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943189"
---
# <a name="create-user"></a><span data-ttu-id="71df2-103">Crear usuario</span><span class="sxs-lookup"><span data-stu-id="71df2-103">Create user</span></span>

> <span data-ttu-id="71df2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="71df2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="71df2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="71df2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="71df2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="71df2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71df2-107">Cree un objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="71df2-107">Create a new [user](../resources/intune-shared-user.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="71df2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71df2-108">Prerequisites</span></span>

<span data-ttu-id="71df2-109">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="71df2-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="71df2-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="71df2-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="71df2-111">Los permisos específicos necesarios depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="71df2-111">The specific permission required depends on the context.</span></span>

|<span data-ttu-id="71df2-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71df2-112">Permission type</span></span>|<span data-ttu-id="71df2-113">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71df2-113">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="71df2-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71df2-114">Delegated (work or school account)</span></span>||
| <span data-ttu-id="71df2-115">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="71df2-115">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="71df2-116">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71df2-116">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
| <span data-ttu-id="71df2-117">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="71df2-117">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="71df2-118">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71df2-118">DeviceManagementApps.ReadWrite.All</span></span>|
| <span data-ttu-id="71df2-119">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="71df2-119">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="71df2-120">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71df2-120">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
| <span data-ttu-id="71df2-121">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="71df2-121">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="71df2-122">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71df2-122">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="71df2-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71df2-123">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="71df2-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71df2-124">Not supported.</span></span>|
|<span data-ttu-id="71df2-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71df2-125">Application</span></span>|<span data-ttu-id="71df2-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71df2-126">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="71df2-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71df2-127">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users
```

## <a name="request-headers"></a><span data-ttu-id="71df2-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71df2-128">Request headers</span></span>

|<span data-ttu-id="71df2-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71df2-129">Header</span></span>|<span data-ttu-id="71df2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="71df2-130">Value</span></span>|
|:---|:---|
|<span data-ttu-id="71df2-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="71df2-131">Authorization</span></span>|<span data-ttu-id="71df2-132">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="71df2-132">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="71df2-133">Accept</span><span class="sxs-lookup"><span data-stu-id="71df2-133">Accept</span></span>|<span data-ttu-id="71df2-134">application/json</span><span class="sxs-lookup"><span data-stu-id="71df2-134">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="71df2-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71df2-135">Request body</span></span>

<span data-ttu-id="71df2-136">En el cuerpo de la solicitud, especifique una representación JSON del objeto user.</span><span class="sxs-lookup"><span data-stu-id="71df2-136">In the request body, supply a JSON representation for the user object.</span></span>

<span data-ttu-id="71df2-137">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto user.</span><span class="sxs-lookup"><span data-stu-id="71df2-137">The following table shows the properties that are required when you create the user.</span></span>

|<span data-ttu-id="71df2-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="71df2-138">Property</span></span>|<span data-ttu-id="71df2-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="71df2-139">Type</span></span>|<span data-ttu-id="71df2-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="71df2-140">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="71df2-141">id</span><span class="sxs-lookup"><span data-stu-id="71df2-141">id</span></span>|<span data-ttu-id="71df2-142">String</span><span class="sxs-lookup"><span data-stu-id="71df2-142">String</span></span>|<span data-ttu-id="71df2-143">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="71df2-143">Unique identifier of the user.</span></span>|
|<span data-ttu-id="71df2-144">**Incorporación**</span><span class="sxs-lookup"><span data-stu-id="71df2-144">**On-boarding**</span></span>||
|<span data-ttu-id="71df2-145">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="71df2-145">deviceEnrollmentLimit</span></span>|<span data-ttu-id="71df2-146">Int32</span><span class="sxs-lookup"><span data-stu-id="71df2-146">Int32</span></span>|<span data-ttu-id="71df2-147">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="71df2-147">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="71df2-148">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="71df2-148">Allowed values are 5 or 1000.</span></span>|

<span data-ttu-id="71df2-149">Compatibilidad con propiedades de cuerpo de solicitud varía según el contexto.</span><span class="sxs-lookup"><span data-stu-id="71df2-149">Request body property support varies according to context.</span></span>

## <a name="response"></a><span data-ttu-id="71df2-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71df2-150">Response</span></span>

<span data-ttu-id="71df2-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [user](../resources/intune-shared-user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71df2-151">If successful, this method returns a `201 Created` response code and a [user](../resources/intune-shared-user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71df2-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71df2-152">Example</span></span>

### <a name="request"></a><span data-ttu-id="71df2-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71df2-153">Request</span></span>

<span data-ttu-id="71df2-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71df2-154">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/beta/users
Content-type: application/json
Content-length: 46

{
  "@odata.type": "#microsoft.graph.user"
}
```

### <a name="response"></a><span data-ttu-id="71df2-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71df2-155">Response</span></span>

<span data-ttu-id="71df2-156">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71df2-156">Here is an example of the response.</span></span> <span data-ttu-id="71df2-157">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="71df2-157">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="71df2-158">Las propiedades que devuelve una llamada real varían según el contexto.</span><span class="sxs-lookup"><span data-stu-id="71df2-158">Properties returned from an actual call vary according to context.</span></span>

``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



