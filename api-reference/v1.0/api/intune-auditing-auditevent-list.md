---
title: Enumerar auditEvents
description: Enumere las propiedades y las relaciones de los objetos auditEvent.
author: tfitzmac
ms.openlocfilehash: b4ef3d3993884c045428134c03b5097643b3b171
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309512"
---
# <a name="list-auditevents"></a><span data-ttu-id="54c4c-103">Enumerar auditEvents</span><span class="sxs-lookup"><span data-stu-id="54c4c-103">List auditEvents</span></span>

> <span data-ttu-id="54c4c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54c4c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="54c4c-105">Enumere las propiedades y las relaciones de los objetos [auditEvent](../resources/intune-auditing-auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="54c4c-105">List properties and relationships of the [auditEvent](../resources/intune-auditing-auditevent.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="54c4c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54c4c-106">Prerequisites</span></span>
<span data-ttu-id="54c4c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="54c4c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="54c4c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54c4c-109">Permission type</span></span>|<span data-ttu-id="54c4c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54c4c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="54c4c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54c4c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="54c4c-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="54c4c-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="54c4c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54c4c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="54c4c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54c4c-114">Not supported.</span></span>|
|<span data-ttu-id="54c4c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54c4c-115">Application</span></span>|<span data-ttu-id="54c4c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54c4c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="54c4c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54c4c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/auditEvents
```

## <a name="request-headers"></a><span data-ttu-id="54c4c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54c4c-118">Request headers</span></span>
|<span data-ttu-id="54c4c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54c4c-119">Header</span></span>|<span data-ttu-id="54c4c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="54c4c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="54c4c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="54c4c-121">Authorization</span></span>|<span data-ttu-id="54c4c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="54c4c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="54c4c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="54c4c-123">Accept</span></span>|<span data-ttu-id="54c4c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="54c4c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="54c4c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54c4c-125">Request body</span></span>
<span data-ttu-id="54c4c-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="54c4c-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="54c4c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54c4c-127">Response</span></span>
<span data-ttu-id="54c4c-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [auditEvent](../resources/intune-auditing-auditevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54c4c-128">If successful, this method returns a `200 OK` response code and a collection of [auditEvent](../resources/intune-auditing-auditevent.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54c4c-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54c4c-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="54c4c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54c4c-130">Request</span></span>
<span data-ttu-id="54c4c-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54c4c-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/auditEvents
```

### <a name="response"></a><span data-ttu-id="54c4c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54c4c-132">Response</span></span>
<span data-ttu-id="54c4c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54c4c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1632

{
  "value": [
    {
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
  ]
}
```



