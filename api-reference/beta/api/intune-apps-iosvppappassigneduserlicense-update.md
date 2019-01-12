---
title: Actualizar iosVppAppAssignedUserLicense
description: Actualizar las propiedades de un objeto iosVppAppAssignedUserLicense.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 87a5ad2ba2612f4c0d0dbe799dd40e1f8185521e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959779"
---
# <a name="update-iosvppappassigneduserlicense"></a><span data-ttu-id="4bf8d-103">Actualizar iosVppAppAssignedUserLicense</span><span class="sxs-lookup"><span data-stu-id="4bf8d-103">Update iosVppAppAssignedUserLicense</span></span>

> <span data-ttu-id="4bf8d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4bf8d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4bf8d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4bf8d-107">Actualizar las propiedades de un objeto [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="4bf8d-107">Update the properties of a [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4bf8d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4bf8d-108">Prerequisites</span></span>
<span data-ttu-id="4bf8d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4bf8d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4bf8d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4bf8d-111">Permission type</span></span>|<span data-ttu-id="4bf8d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4bf8d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4bf8d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4bf8d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4bf8d-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4bf8d-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="4bf8d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4bf8d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4bf8d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-116">Not supported.</span></span>|
|<span data-ttu-id="4bf8d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4bf8d-117">Application</span></span>|<span data-ttu-id="4bf8d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4bf8d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4bf8d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses/{iosVppAppAssignedLicenseId}
```

## <a name="request-headers"></a><span data-ttu-id="4bf8d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4bf8d-120">Request headers</span></span>
|<span data-ttu-id="4bf8d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bf8d-121">Header</span></span>|<span data-ttu-id="4bf8d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4bf8d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4bf8d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="4bf8d-123">Authorization</span></span>|<span data-ttu-id="4bf8d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4bf8d-125">Accept</span><span class="sxs-lookup"><span data-stu-id="4bf8d-125">Accept</span></span>|<span data-ttu-id="4bf8d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4bf8d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4bf8d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4bf8d-127">Request body</span></span>
<span data-ttu-id="4bf8d-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="4bf8d-128">In the request body, supply a JSON representation for the [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object.</span></span>

<span data-ttu-id="4bf8d-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md).</span><span class="sxs-lookup"><span data-stu-id="4bf8d-129">The following table shows the properties that are required when you create the [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md).</span></span>

|<span data-ttu-id="4bf8d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4bf8d-130">Property</span></span>|<span data-ttu-id="4bf8d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4bf8d-131">Type</span></span>|<span data-ttu-id="4bf8d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bf8d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4bf8d-133">id</span><span class="sxs-lookup"><span data-stu-id="4bf8d-133">id</span></span>|<span data-ttu-id="4bf8d-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bf8d-134">String</span></span>|<span data-ttu-id="4bf8d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-135">Key of the entity.</span></span> <span data-ttu-id="4bf8d-136">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="4bf8d-136">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="4bf8d-137">userEmailAddress</span><span class="sxs-lookup"><span data-stu-id="4bf8d-137">userEmailAddress</span></span>|<span data-ttu-id="4bf8d-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bf8d-138">String</span></span>|<span data-ttu-id="4bf8d-139">La dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-139">The user email address.</span></span> <span data-ttu-id="4bf8d-140">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="4bf8d-140">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="4bf8d-141">userId</span><span class="sxs-lookup"><span data-stu-id="4bf8d-141">userId</span></span>|<span data-ttu-id="4bf8d-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bf8d-142">String</span></span>|<span data-ttu-id="4bf8d-143">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-143">The user ID.</span></span> <span data-ttu-id="4bf8d-144">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="4bf8d-144">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="4bf8d-145">userName</span><span class="sxs-lookup"><span data-stu-id="4bf8d-145">userName</span></span>|<span data-ttu-id="4bf8d-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bf8d-146">String</span></span>|<span data-ttu-id="4bf8d-147">El nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-147">The user name.</span></span> <span data-ttu-id="4bf8d-148">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="4bf8d-148">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="4bf8d-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4bf8d-149">userPrincipalName</span></span>|<span data-ttu-id="4bf8d-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bf8d-150">String</span></span>|<span data-ttu-id="4bf8d-151">El nombre principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-151">The user principal name.</span></span> <span data-ttu-id="4bf8d-152">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="4bf8d-152">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|



## <a name="response"></a><span data-ttu-id="4bf8d-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bf8d-153">Response</span></span>
<span data-ttu-id="4bf8d-154">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-154">If successful, this method returns a `200 OK` response code and an updated [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4bf8d-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4bf8d-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="4bf8d-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4bf8d-156">Request</span></span>
<span data-ttu-id="4bf8d-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-157">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="4bf8d-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bf8d-158">Response</span></span>
<span data-ttu-id="4bf8d-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4bf8d-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





