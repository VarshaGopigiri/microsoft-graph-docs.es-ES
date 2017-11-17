# <a name="delete-calendargroup"></a><span data-ttu-id="423e9-101">Eliminar calendarGroup</span><span class="sxs-lookup"><span data-stu-id="423e9-101">Delete calendarGroup</span></span>

<span data-ttu-id="423e9-102">Elimine un grupo de calendarios que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="423e9-102">Delete a calendar group other than the default calendar group.</span></span>

<span data-ttu-id="423e9-p101">**Nota** Outlook.com solo admite el grupo de calendarios predeterminado que es accesible mediante el acceso directo /me/calendars. No se puede eliminar ningún grupo de calendarios de Outlook.com.</span><span class="sxs-lookup"><span data-stu-id="423e9-p101">**Note** Outlook.com supports only the default calendar group which is accessible by the /me/calendars shortcut. You cannot delete any calendar group in Outlook.com.</span></span>

## <a name="permissions"></a><span data-ttu-id="423e9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="423e9-105">Permissions</span></span>
<span data-ttu-id="423e9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="423e9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="423e9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="423e9-108">Permission type</span></span>      | <span data-ttu-id="423e9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="423e9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="423e9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="423e9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="423e9-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="423e9-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="423e9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="423e9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="423e9-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="423e9-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="423e9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="423e9-114">Application</span></span> | <span data-ttu-id="423e9-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="423e9-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="423e9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="423e9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/calendarGroups/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}
```
## <a name="request-headers"></a><span data-ttu-id="423e9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="423e9-117">Request headers</span></span>
| <span data-ttu-id="423e9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="423e9-118">Name</span></span>       | <span data-ttu-id="423e9-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="423e9-119">Type</span></span> | <span data-ttu-id="423e9-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="423e9-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="423e9-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="423e9-121">Authorization</span></span>  | <span data-ttu-id="423e9-122">string</span><span class="sxs-lookup"><span data-stu-id="423e9-122">string</span></span>  | <span data-ttu-id="423e9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="423e9-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="423e9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="423e9-125">Request body</span></span>
<span data-ttu-id="423e9-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="423e9-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="423e9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="423e9-127">Response</span></span>

<span data-ttu-id="423e9-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="423e9-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="423e9-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="423e9-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="423e9-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="423e9-131">Request</span></span>
<span data-ttu-id="423e9-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="423e9-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_calendargroup"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="423e9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="423e9-133">Response</span></span>
<span data-ttu-id="423e9-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="423e9-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
