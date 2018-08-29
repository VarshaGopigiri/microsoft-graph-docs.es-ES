# <a name="list-auditevents"></a><span data-ttu-id="c35f3-101">Enumerar auditEvents</span><span class="sxs-lookup"><span data-stu-id="c35f3-101">List auditEvents</span></span>

> <span data-ttu-id="c35f3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c35f3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c35f3-103">Enumere las propiedades y las relaciones de los objetos [auditEvent](../resources/intune_auditing_auditevent.md).</span><span class="sxs-lookup"><span data-stu-id="c35f3-103">List properties and relationships of the [auditEvent](../resources/intune_auditing_auditevent.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c35f3-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c35f3-104">Prerequisites</span></span>
<span data-ttu-id="c35f3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c35f3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c35f3-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c35f3-107">Permission type</span></span>|<span data-ttu-id="c35f3-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c35f3-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c35f3-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c35f3-109">Delegated (work or school account)</span></span>|<span data-ttu-id="c35f3-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="c35f3-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="c35f3-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c35f3-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c35f3-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c35f3-112">Not supported.</span></span>|
|<span data-ttu-id="c35f3-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c35f3-113">Application</span></span>|<span data-ttu-id="c35f3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c35f3-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c35f3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c35f3-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/auditEvents
```

## <a name="request-headers"></a><span data-ttu-id="c35f3-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c35f3-116">Request headers</span></span>
|<span data-ttu-id="c35f3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c35f3-117">Header</span></span>|<span data-ttu-id="c35f3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c35f3-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c35f3-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="c35f3-119">Authorization</span></span>|<span data-ttu-id="c35f3-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c35f3-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c35f3-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c35f3-121">Accept</span></span>|<span data-ttu-id="c35f3-122">application/json</span><span class="sxs-lookup"><span data-stu-id="c35f3-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c35f3-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c35f3-123">Request body</span></span>
<span data-ttu-id="c35f3-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c35f3-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c35f3-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c35f3-125">Response</span></span>
<span data-ttu-id="c35f3-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [auditEvent](../resources/intune_auditing_auditevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c35f3-126">If successful, this method returns a `200 OK` response code and a collection of [auditEvent](../resources/intune_auditing_auditevent.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c35f3-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c35f3-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="c35f3-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c35f3-128">Request</span></span>
<span data-ttu-id="c35f3-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c35f3-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/auditEvents
```

### <a name="response"></a><span data-ttu-id="c35f3-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c35f3-130">Response</span></span>
<span data-ttu-id="c35f3-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c35f3-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1629

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
      "correlationId": "79199ed9-e50b-4257-8de4-70b9c8685061",
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



