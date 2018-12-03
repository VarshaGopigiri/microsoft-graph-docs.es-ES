---
title: Obtener auditEvent
description: Lea las propiedades y las relaciones del objeto auditEvent.
ms.openlocfilehash: dbfa908d57c65c024f253cbc4b7d5e7071443180
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090988"
---
# <a name="get-auditevent"></a><span data-ttu-id="f1014-103">Obtener auditEvent</span><span class="sxs-lookup"><span data-stu-id="f1014-103">Get auditEvent</span></span>

> <span data-ttu-id="f1014-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f1014-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f1014-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f1014-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f1014-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f1014-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f1014-107">Lea las propiedades y las relaciones del objeto [auditEvent](../resources/intune-auditing-auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="f1014-107">Read properties and relationships of the [auditEvent](../resources/intune-auditing-auditevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f1014-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f1014-108">Prerequisites</span></span>
<span data-ttu-id="f1014-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f1014-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f1014-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f1014-111">Permission type</span></span>|<span data-ttu-id="f1014-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f1014-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f1014-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f1014-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f1014-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="f1014-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="f1014-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f1014-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f1014-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1014-116">Not supported.</span></span>|
|<span data-ttu-id="f1014-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f1014-117">Application</span></span>|<span data-ttu-id="f1014-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1014-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f1014-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f1014-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/auditEvents/{auditEventId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f1014-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f1014-120">Optional query parameters</span></span>
<span data-ttu-id="f1014-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1014-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f1014-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f1014-122">Request headers</span></span>
|<span data-ttu-id="f1014-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1014-123">Header</span></span>|<span data-ttu-id="f1014-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f1014-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f1014-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="f1014-125">Authorization</span></span>|<span data-ttu-id="f1014-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f1014-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f1014-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f1014-127">Accept</span></span>|<span data-ttu-id="f1014-128">application/json</span><span class="sxs-lookup"><span data-stu-id="f1014-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f1014-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f1014-129">Request body</span></span>
<span data-ttu-id="f1014-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f1014-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f1014-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1014-131">Response</span></span>
<span data-ttu-id="f1014-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de [auditEvent](../resources/intune-auditing-auditevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1014-132">If successful, this method returns a `200 OK` response code and [auditEvent](../resources/intune-auditing-auditevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f1014-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1014-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="f1014-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f1014-134">Request</span></span>
<span data-ttu-id="f1014-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1014-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/auditEvents/{auditEventId}
```

### <a name="response"></a><span data-ttu-id="f1014-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1014-136">Response</span></span>
<span data-ttu-id="f1014-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f1014-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1538

{
  "value": {
    "@odata.type": "#microsoft.graph.auditEvent",
    "id": "59653ce8-3ce8-5965-e83c-6559e83c6559",
    "displayName": "Display Name value",
    "componentName": "Component Name value",
    "actor": {
      "@odata.type": "microsoft.graph.auditActor",
      "type": "Type value",
      "userPermissions": [
        "User Permissions value"
      ],
      "applicationId": "Application Id value",
      "applicationDisplayName": "Application Display Name value",
      "userPrincipalName": "User Principal Name value",
      "servicePrincipalName": "Service Principal Name value",
      "ipAddress": "Ip Address value",
      "userId": "User Id value"
    },
    "activity": "Activity value",
    "activityDateTime": "2016-12-31T23:59:51.6363086-08:00",
    "activityType": "Activity Type value",
    "activityOperationType": "Activity Operation Type value",
    "activityResult": "Activity Result value",
    "correlationId": "52effe71-fe71-52ef-71fe-ef5271feef52",
    "resources": [
      {
        "@odata.type": "microsoft.graph.auditResource",
        "displayName": "Display Name value",
        "modifiedProperties": [
          {
            "@odata.type": "microsoft.graph.auditProperty",
            "displayName": "Display Name value",
            "oldValue": "Old Value value",
            "newValue": "New Value value"
          }
        ],
        "type": "Type value",
        "resourceId": "Resource Id value"
      }
    ],
    "category": "Category value"
  }
}
```




