---
title: Actualizar iosVppAppAssignedUserLicense
description: Actualizar las propiedades de un objeto iosVppAppAssignedUserLicense.
ms.openlocfilehash: 4374a2288c633da47773c827fc47a6e3ef0ee1d1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090994"
---
# <a name="update-iosvppappassigneduserlicense"></a><span data-ttu-id="1e528-103">Actualizar iosVppAppAssignedUserLicense</span><span class="sxs-lookup"><span data-stu-id="1e528-103">Update iosVppAppAssignedUserLicense</span></span>

> <span data-ttu-id="1e528-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1e528-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1e528-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1e528-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1e528-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1e528-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1e528-107">Actualizar las propiedades de un objeto [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="1e528-107">Update the properties of a [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1e528-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1e528-108">Prerequisites</span></span>
<span data-ttu-id="1e528-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1e528-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1e528-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1e528-111">Permission type</span></span>|<span data-ttu-id="1e528-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1e528-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1e528-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1e528-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1e528-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1e528-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1e528-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1e528-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1e528-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e528-116">Not supported.</span></span>|
|<span data-ttu-id="1e528-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1e528-117">Application</span></span>|<span data-ttu-id="1e528-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e528-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1e528-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1e528-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses/{iosVppAppAssignedLicenseId}
```

## <a name="request-headers"></a><span data-ttu-id="1e528-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1e528-120">Request headers</span></span>
|<span data-ttu-id="1e528-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e528-121">Header</span></span>|<span data-ttu-id="1e528-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1e528-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1e528-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1e528-123">Authorization</span></span>|<span data-ttu-id="1e528-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1e528-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1e528-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1e528-125">Accept</span></span>|<span data-ttu-id="1e528-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1e528-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1e528-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1e528-127">Request body</span></span>
<span data-ttu-id="1e528-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="1e528-128">In the request body, supply a JSON representation for the [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object.</span></span>

<span data-ttu-id="1e528-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md).</span><span class="sxs-lookup"><span data-stu-id="1e528-129">The following table shows the properties that are required when you create the [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md).</span></span>

|<span data-ttu-id="1e528-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e528-130">Property</span></span>|<span data-ttu-id="1e528-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e528-131">Type</span></span>|<span data-ttu-id="1e528-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e528-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1e528-133">id</span><span class="sxs-lookup"><span data-stu-id="1e528-133">id</span></span>|<span data-ttu-id="1e528-134">String</span><span class="sxs-lookup"><span data-stu-id="1e528-134">String</span></span>|<span data-ttu-id="1e528-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1e528-135">Key of the entity.</span></span> <span data-ttu-id="1e528-136">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="1e528-136">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="1e528-137">userEmailAddress</span><span class="sxs-lookup"><span data-stu-id="1e528-137">userEmailAddress</span></span>|<span data-ttu-id="1e528-138">String</span><span class="sxs-lookup"><span data-stu-id="1e528-138">String</span></span>|<span data-ttu-id="1e528-139">La dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="1e528-139">The user email address.</span></span> <span data-ttu-id="1e528-140">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="1e528-140">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="1e528-141">userId</span><span class="sxs-lookup"><span data-stu-id="1e528-141">userId</span></span>|<span data-ttu-id="1e528-142">String</span><span class="sxs-lookup"><span data-stu-id="1e528-142">String</span></span>|<span data-ttu-id="1e528-143">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="1e528-143">The user ID.</span></span> <span data-ttu-id="1e528-144">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="1e528-144">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="1e528-145">userName</span><span class="sxs-lookup"><span data-stu-id="1e528-145">userName</span></span>|<span data-ttu-id="1e528-146">String</span><span class="sxs-lookup"><span data-stu-id="1e528-146">String</span></span>|<span data-ttu-id="1e528-147">El nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="1e528-147">The user name.</span></span> <span data-ttu-id="1e528-148">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="1e528-148">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="1e528-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1e528-149">userPrincipalName</span></span>|<span data-ttu-id="1e528-150">String</span><span class="sxs-lookup"><span data-stu-id="1e528-150">String</span></span>|<span data-ttu-id="1e528-151">El nombre principal de usuario.</span><span class="sxs-lookup"><span data-stu-id="1e528-151">The user principal name.</span></span> <span data-ttu-id="1e528-152">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="1e528-152">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|



## <a name="response"></a><span data-ttu-id="1e528-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e528-153">Response</span></span>
<span data-ttu-id="1e528-154">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e528-154">If successful, this method returns a `200 OK` response code and an updated [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1e528-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e528-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="1e528-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1e528-156">Request</span></span>
<span data-ttu-id="1e528-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1e528-157">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="1e528-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e528-158">Response</span></span>
<span data-ttu-id="1e528-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1e528-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 287

{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedUserLicense",
  "id": "fedc747d-747d-fedc-7d74-dcfe7d74dcfe",
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value"
}
```




