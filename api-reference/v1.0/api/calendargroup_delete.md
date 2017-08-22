# <a name="delete-calendargroup"></a><span data-ttu-id="cdc19-101">Eliminar calendarGroup</span><span class="sxs-lookup"><span data-stu-id="cdc19-101">Delete calendarGroup</span></span>

<span data-ttu-id="cdc19-102">Elimine un grupo de calendarios que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cdc19-102">Delete a calendar group other than the default calendar group.</span></span>

<span data-ttu-id="cdc19-p101">**Nota** Outlook.com solo admite el grupo de calendarios predeterminado que es accesible mediante el acceso directo /me/calendars. No se puede eliminar ningún grupo de calendarios de Outlook.com.</span><span class="sxs-lookup"><span data-stu-id="cdc19-p101">**Note** Outlook.com supports only the default calendar group which is accessible by the /me/calendars shortcut. You cannot delete any calendar group in Outlook.com.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cdc19-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cdc19-105">Prerequisites</span></span>
<span data-ttu-id="cdc19-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="cdc19-106">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="cdc19-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cdc19-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/calendarGroups/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}
```
## <a name="request-headers"></a><span data-ttu-id="cdc19-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cdc19-108">Request headers</span></span>
| <span data-ttu-id="cdc19-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="cdc19-109">Name</span></span>       | <span data-ttu-id="cdc19-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="cdc19-110">Type</span></span> | <span data-ttu-id="cdc19-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdc19-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="cdc19-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="cdc19-112">Authorization</span></span>  | <span data-ttu-id="cdc19-113">string</span><span class="sxs-lookup"><span data-stu-id="cdc19-113">string</span></span>  | <span data-ttu-id="cdc19-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cdc19-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cdc19-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cdc19-116">Request body</span></span>
<span data-ttu-id="cdc19-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cdc19-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cdc19-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cdc19-118">Response</span></span>

<span data-ttu-id="cdc19-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cdc19-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cdc19-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cdc19-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cdc19-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cdc19-122">Request</span></span>
<span data-ttu-id="cdc19-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cdc19-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_calendargroup"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="cdc19-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cdc19-124">Response</span></span>
<span data-ttu-id="cdc19-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cdc19-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete calendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
