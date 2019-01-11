---
title: Actualizar iosVppAppAssignedLicense
description: Actualizar las propiedades de un objeto iosVppAppAssignedLicense.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 226a192e5a3da8071b5c31a523f97c60ecec8b09
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879159"
---
# <a name="update-iosvppappassignedlicense"></a><span data-ttu-id="3f27b-103">Actualizar iosVppAppAssignedLicense</span><span class="sxs-lookup"><span data-stu-id="3f27b-103">Update iosVppAppAssignedLicense</span></span>

> <span data-ttu-id="3f27b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f27b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f27b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f27b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3f27b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3f27b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3f27b-107">Actualizar las propiedades de un objeto [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="3f27b-107">Update the properties of a [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3f27b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3f27b-108">Prerequisites</span></span>
<span data-ttu-id="3f27b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f27b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f27b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f27b-111">Permission type</span></span>|<span data-ttu-id="3f27b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f27b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3f27b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f27b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3f27b-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3f27b-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="3f27b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f27b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3f27b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f27b-116">Not supported.</span></span>|
|<span data-ttu-id="3f27b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f27b-117">Application</span></span>|<span data-ttu-id="3f27b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f27b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3f27b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f27b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses/{iosVppAppAssignedLicenseId}
```

## <a name="request-headers"></a><span data-ttu-id="3f27b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f27b-120">Request headers</span></span>
|<span data-ttu-id="3f27b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f27b-121">Header</span></span>|<span data-ttu-id="3f27b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3f27b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3f27b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3f27b-123">Authorization</span></span>|<span data-ttu-id="3f27b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3f27b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3f27b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="3f27b-125">Accept</span></span>|<span data-ttu-id="3f27b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3f27b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3f27b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3f27b-127">Request body</span></span>
<span data-ttu-id="3f27b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="3f27b-128">In the request body, supply a JSON representation for the [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) object.</span></span>

<span data-ttu-id="3f27b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md).</span><span class="sxs-lookup"><span data-stu-id="3f27b-129">The following table shows the properties that are required when you create the [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md).</span></span>

|<span data-ttu-id="3f27b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3f27b-130">Property</span></span>|<span data-ttu-id="3f27b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f27b-131">Type</span></span>|<span data-ttu-id="3f27b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f27b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3f27b-133">id</span><span class="sxs-lookup"><span data-stu-id="3f27b-133">id</span></span>|<span data-ttu-id="3f27b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f27b-134">String</span></span>|<span data-ttu-id="3f27b-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3f27b-135">Key of the entity.</span></span>|
|<span data-ttu-id="3f27b-136">userEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3f27b-136">userEmailAddress</span></span>|<span data-ttu-id="3f27b-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f27b-137">String</span></span>|<span data-ttu-id="3f27b-138">La dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="3f27b-138">The user email address.</span></span>|
|<span data-ttu-id="3f27b-139">userId</span><span class="sxs-lookup"><span data-stu-id="3f27b-139">userId</span></span>|<span data-ttu-id="3f27b-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f27b-140">String</span></span>|<span data-ttu-id="3f27b-141">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="3f27b-141">The user ID.</span></span>|
|<span data-ttu-id="3f27b-142">userName</span><span class="sxs-lookup"><span data-stu-id="3f27b-142">userName</span></span>|<span data-ttu-id="3f27b-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f27b-143">String</span></span>|<span data-ttu-id="3f27b-144">El nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="3f27b-144">The user name.</span></span>|
|<span data-ttu-id="3f27b-145">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3f27b-145">userPrincipalName</span></span>|<span data-ttu-id="3f27b-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="3f27b-146">String</span></span>|<span data-ttu-id="3f27b-147">El nombre principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="3f27b-147">The user principal name.</span></span>|



## <a name="response"></a><span data-ttu-id="3f27b-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f27b-148">Response</span></span>
<span data-ttu-id="3f27b-149">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f27b-149">If successful, this method returns a `200 OK` response code and an updated [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3f27b-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f27b-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="3f27b-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f27b-151">Request</span></span>
<span data-ttu-id="3f27b-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f27b-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses/{iosVppAppAssignedLicenseId}
Content-type: application/json
Content-length: 171

{
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="3f27b-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f27b-153">Response</span></span>
<span data-ttu-id="3f27b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3f27b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 283

{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedLicense",
  "id": "090a8d2e-8d2e-090a-2e8d-0a092e8d0a09",
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value"
}
```





