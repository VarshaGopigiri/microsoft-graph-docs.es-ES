# <a name="create-registeredowner"></a><span data-ttu-id="0a4cb-101">Create registeredOwner</span><span class="sxs-lookup"><span data-stu-id="0a4cb-101">Create registeredOwner</span></span>

<span data-ttu-id="0a4cb-102">Agrega un usuario como propietario registrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a4cb-102">Add a user as a registered owner of the device.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0a4cb-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0a4cb-103">Prerequisites</span></span>
<span data-ttu-id="0a4cb-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="0a4cb-104">One of the following **scopes** is required to execute this API: *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="0a4cb-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a4cb-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices/{id}/registeredOwners

```
## <a name="request-headers"></a><span data-ttu-id="0a4cb-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a4cb-106">Request headers</span></span>
| <span data-ttu-id="0a4cb-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a4cb-107">Name</span></span>       | <span data-ttu-id="0a4cb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a4cb-108">Type</span></span> | <span data-ttu-id="0a4cb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a4cb-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="0a4cb-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="0a4cb-110">Authorization</span></span>  | <span data-ttu-id="0a4cb-111">string</span><span class="sxs-lookup"><span data-stu-id="0a4cb-111">string</span></span>  | <span data-ttu-id="0a4cb-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a4cb-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0a4cb-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a4cb-114">Request body</span></span>
<span data-ttu-id="0a4cb-115">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="0a4cb-115">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="0a4cb-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a4cb-116">Response</span></span>

<span data-ttu-id="0a4cb-117">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a4cb-117">If successful, this method returns `201, Created` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a4cb-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a4cb-118">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0a4cb-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a4cb-119">Request</span></span>
<span data-ttu-id="0a4cb-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a4cb-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_device"
}-->
```http
POST https://graph.microsoft.com/v1.0/devices/{id}/registeredOwners
Content-type: application/json
Content-length: 30

{
  "directoryObject": {
  }
}
```
<span data-ttu-id="0a4cb-121">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="0a4cb-121">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="0a4cb-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a4cb-122">Response</span></span>
<span data-ttu-id="0a4cb-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a4cb-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 51

{
  "directoryObject": {
    "id": "id-value"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create registeredOwner",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->