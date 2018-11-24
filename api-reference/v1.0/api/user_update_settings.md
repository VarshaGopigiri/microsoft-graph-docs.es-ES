# <a name="update-settings"></a><span data-ttu-id="b4c15-101">Configuración de actualización</span><span class="sxs-lookup"><span data-stu-id="b4c15-101">Update settings</span></span>

<span data-ttu-id="b4c15-102">Actualizar las propiedades del objeto [settings](../resources/user_settings.md) .</span><span class="sxs-lookup"><span data-stu-id="b4c15-102">Update the properties of the [settings](../resources/user_settings.md) object.</span></span> <span data-ttu-id="b4c15-103">Los usuarios en la misma organización pueden tener diferentes configuraciones basadas en sus preferencias o en las directivas de la organización.</span><span class="sxs-lookup"><span data-stu-id="b4c15-103">Users in the same organization can have different settings based on their preference or on the organization policies.</span></span> <span data-ttu-id="b4c15-104">Para obtener al usuario actual configuración, vea [Configuración del usuario actual](user_get_settings.md).</span><span class="sxs-lookup"><span data-stu-id="b4c15-104">To get the user current settings, see [current user settings](user_get_settings.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="b4c15-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b4c15-105">Permissions</span></span>

<span data-ttu-id="b4c15-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b4c15-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b4c15-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4c15-108">Permission type</span></span>      | <span data-ttu-id="b4c15-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4c15-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b4c15-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4c15-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b4c15-111">User.ReadWrite, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4c15-111">User.ReadWrite, User.ReadWrite.All</span></span>   |
|<span data-ttu-id="b4c15-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4c15-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b4c15-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4c15-113">Not supported.</span></span>    |
|<span data-ttu-id="b4c15-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4c15-114">Application</span></span> | <span data-ttu-id="b4c15-115">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4c15-115">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b4c15-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4c15-116">HTTP request</span></span>

```http
PATCH https://graph.microsoft.com/v1.0/me/settings
```

<span data-ttu-id="b4c15-117">Solicitar a un 'id' o 'userPrincipalName' sólo es accesible por el usuario o por un usuario con los permisos de User.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="b4c15-117">Request with a 'user id' or 'userPrincipalName' is only accessible by the user or by a user with the User.ReadWrite.All permissions.</span></span> <span data-ttu-id="b4c15-118">Para obtener más información, vea [permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b4c15-118">To learn more, see [Permissions](../../../concepts/permissions_reference.md).</span></span> 

```http
PATCH https://graph.microsoft.com/v1.0/users/{id | userPrincipalName}/settings/
```

## <a name="request-headers"></a><span data-ttu-id="b4c15-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b4c15-119">Request headers</span></span>

| <span data-ttu-id="b4c15-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4c15-120">Header</span></span>       | <span data-ttu-id="b4c15-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b4c15-121">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="b4c15-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b4c15-122">Authorization</span></span>  | <span data-ttu-id="b4c15-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b4c15-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b4c15-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b4c15-125">Content-Type</span></span>  | <span data-ttu-id="b4c15-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b4c15-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b4c15-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b4c15-127">Request body</span></span>

<span data-ttu-id="b4c15-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b4c15-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b4c15-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4c15-131">Property</span></span>     | <span data-ttu-id="b4c15-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4c15-132">Type</span></span>   |<span data-ttu-id="b4c15-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4c15-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b4c15-134">contributionToContentDiscoveryDisabled</span><span class="sxs-lookup"><span data-stu-id="b4c15-134">contributionToContentDiscoveryDisabled</span></span>|<span data-ttu-id="b4c15-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="b4c15-135">Boolean</span></span>|<span data-ttu-id="b4c15-136">En el valor true deshabilita el acceso de delegado a la API de [tendencias](../../beta/resources/insights_trending.md) y deshabilitar el acceso a los documentos de Office profundizar para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b4c15-136">Set to true do disable delegate access to the [Trending](../../beta/resources/insights_trending.md) API and to disable access to documents in Office Delve for the user.</span></span> <span data-ttu-id="b4c15-137">Configuración en true también afecta a la relevancia del contenido que se muestra en Office 365: por ejemplo, los sitios que se sugiere en la página principal de SharePoint y la vista de detección en OneDrive para la empresa muestran resultados menos relevantes.</span><span class="sxs-lookup"><span data-stu-id="b4c15-137">Setting to true also affects the relevance of the content displayed in Office 365 - for example, Suggested sites in SharePoint Home and the Discover view in OneDrive for Business show less relevant results.</span></span> <span data-ttu-id="b4c15-138">Esta configuración refleja el estado de control en [Office profundizar](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout).</span><span class="sxs-lookup"><span data-stu-id="b4c15-138">This setting reflects the control state in [Office Delve](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout).</span></span>|

## <a name="example"></a><span data-ttu-id="b4c15-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4c15-139">Example</span></span> 

##### <a name="request"></a><span data-ttu-id="b4c15-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b4c15-140">Request</span></span>

<span data-ttu-id="b4c15-141">Este es un ejemplo de solicitud en cómo voluntaria de un usuario desde Delve y deshabilitar su contribución en la relevancia de contenido para toda la organización.</span><span class="sxs-lookup"><span data-stu-id="b4c15-141">Here is an example request on how to opt-out a user from Delve and disable his contribution on content relevancy for the whole organization.</span></span>

```http
PATCH https://graph.microsoft.com/v1.0/me/settings
Content-type: application/json
Content-length: 37

{
  "contributionToContentDiscoveryDisabled": true
}
```

##### <a name="response"></a><span data-ttu-id="b4c15-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4c15-142">Response</span></span>

<span data-ttu-id="b4c15-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4c15-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": true
}
```

#### <a name="batch-request"></a><span data-ttu-id="b4c15-146">Solicitud de lote</span><span class="sxs-lookup"><span data-stu-id="b4c15-146">Batch request</span></span>

<span data-ttu-id="b4c15-147">También es posible voluntaria de varios usuarios desde Delve y deshabilitar su contribución en la relevancia de contenido para toda la organización a través de una solicitud por lotes.</span><span class="sxs-lookup"><span data-stu-id="b4c15-147">It's also possible to opt-out multiple users from Delve and disable their contribution on content relevancy for the whole organization through a batch request.</span></span>
<span data-ttu-id="b4c15-148">Para obtener más información, vea [el procesamiento por lotes de JSON](https://developer.microsoft.com/graph/docs/concepts/json_batching).</span><span class="sxs-lookup"><span data-stu-id="b4c15-148">To learn more, see [JSON batching](https://developer.microsoft.com/graph/docs/concepts/json_batching).</span></span>

<span data-ttu-id="b4c15-149">**Importante**: sólo los miembros del grupo de roles de [Administración de la organización](https://support.office.com/article/permissions-in-the-office-365-security-compliance-center-d10608af-7934-490a-818e-e68f17d0e9c1?ui=en-US&rs=en-US&ad=US) pueden actualizar varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="b4c15-149">**Important**: Only members of the [Organization Management](https://support.office.com/article/permissions-in-the-office-365-security-compliance-center-d10608af-7934-490a-818e-e68f17d0e9c1?ui=en-US&rs=en-US&ad=US) role group can update multiple users.</span></span> 



