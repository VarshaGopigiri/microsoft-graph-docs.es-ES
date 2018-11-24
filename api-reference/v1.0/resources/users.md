# <a name="working-with-users-in-microsoft-graph"></a><span data-ttu-id="48f70-101">Trabajar con usuarios en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="48f70-101">Working with users in Microsoft Graph</span></span>

<span data-ttu-id="48f70-102">Puede usar Microsoft Graph para crear experiencias de aplicaciones convincentes basadas en usuarios, sus relaciones con otros usuarios y grupos y su correo, calendario y archivos.</span><span class="sxs-lookup"><span data-stu-id="48f70-102">You can use Microsoft Graph to build compelling app experiences based on users, their relationships with other users and groups, and their mail, calendar, and files.</span></span>

<span data-ttu-id="48f70-103">Puede acceder a los [usuarios](user.md) a través de Microsoft Graph de dos formas:</span><span class="sxs-lookup"><span data-stu-id="48f70-103">You can access [users](user.md) through Microsoft Graph in two ways:</span></span>

- <span data-ttu-id="48f70-104">Mediante su identificador, `/users/{id | userPrincipalName}`</span><span class="sxs-lookup"><span data-stu-id="48f70-104">By their ID, `/users/{id | userPrincipalName}`</span></span> 
- <span data-ttu-id="48f70-105">Mediante el alias `/me` del usuario que ha iniciado sesión, que es el mismo que `/users/{signed-in user's id}`</span><span class="sxs-lookup"><span data-stu-id="48f70-105">By using the `/me` alias for the signed-in user, which is the same as `/users/{signed-in user's id}`</span></span>

## <a name="authorization"></a><span data-ttu-id="48f70-106">Authorization</span><span class="sxs-lookup"><span data-stu-id="48f70-106">Authorization</span></span>

<span data-ttu-id="48f70-p101">Se requiere uno de los siguientes [permisos](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) para acceder a las operaciones de usuario. Los tres primeros permisos los puede conceder un usuario a una aplicación. El resto solo los puede conceder el administrador a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="48f70-p101">One of the following [permissions](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) is required to access user operations. The first three permissions can be granted to an app by a user. The rest can only be granted to an app by the administrator.</span></span>

- <span data-ttu-id="48f70-110">User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="48f70-110">User.ReadBasic.All</span></span>
- <span data-ttu-id="48f70-111">User.Read</span><span class="sxs-lookup"><span data-stu-id="48f70-111">User.Read</span></span>
- <span data-ttu-id="48f70-112">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="48f70-112">User.ReadWrite</span></span>
- <span data-ttu-id="48f70-113">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="48f70-113">User.Read.All</span></span>
- <span data-ttu-id="48f70-114">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48f70-114">User.ReadWrite.All</span></span>
- <span data-ttu-id="48f70-115">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="48f70-115">Directory.Read.All</span></span>
- <span data-ttu-id="48f70-116">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48f70-116">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="48f70-117">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="48f70-117">Directory.AccessAsUser.All</span></span>

## <a name="common-properties"></a><span data-ttu-id="48f70-118">Propiedades comunes</span><span class="sxs-lookup"><span data-stu-id="48f70-118">Common properties</span></span>

<span data-ttu-id="48f70-119">Las siguientes propiedades representan el conjunto predeterminado de propiedades que se devuelven al obtener un usuario o enumerar usuarios.</span><span class="sxs-lookup"><span data-stu-id="48f70-119">The following represent the default set of properties that are returned when getting a user or listing users.</span></span> <span data-ttu-id="48f70-120">Son un subconjunto de todas las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="48f70-120">These are a subset of all available properties.</span></span> <span data-ttu-id="48f70-121">Para obtener más propiedades de usuario, use el parámetro de consulta `$select`.</span><span class="sxs-lookup"><span data-stu-id="48f70-121">To get more user properties, use the `$select` query parameter.</span></span> 

|<span data-ttu-id="48f70-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="48f70-122">Property</span></span> |<span data-ttu-id="48f70-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="48f70-123">Description</span></span> |
|:----------|:-------------|
|<span data-ttu-id="48f70-124">id</span><span class="sxs-lookup"><span data-stu-id="48f70-124">id</span></span> | <span data-ttu-id="48f70-125">El identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-125">The unique identifier for the user.</span></span>|
|<span data-ttu-id="48f70-126">businessPhones</span><span class="sxs-lookup"><span data-stu-id="48f70-126">businessPhones</span></span> | <span data-ttu-id="48f70-127">Los números de teléfono del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-127">The user's phone numbers.</span></span>|
|<span data-ttu-id="48f70-128">displayName</span><span class="sxs-lookup"><span data-stu-id="48f70-128">displayName</span></span> | <span data-ttu-id="48f70-129">El nombre del usuario que aparece en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="48f70-129">The name displayed in the address book for the user.</span></span>|
|<span data-ttu-id="48f70-130">givenName</span><span class="sxs-lookup"><span data-stu-id="48f70-130">givenName</span></span>| <span data-ttu-id="48f70-131">El nombre de pila del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-131">The first name of the user.</span></span> |
|<span data-ttu-id="48f70-132">jobTitle</span><span class="sxs-lookup"><span data-stu-id="48f70-132">jobTitle</span></span> | <span data-ttu-id="48f70-133">El puesto del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-133">The user's job title.</span></span>|
|<span data-ttu-id="48f70-134">mail</span><span class="sxs-lookup"><span data-stu-id="48f70-134">mail</span></span>| <span data-ttu-id="48f70-135">La dirección de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-135">The user's email address.</span></span> |
|<span data-ttu-id="48f70-136">mobilePhone</span><span class="sxs-lookup"><span data-stu-id="48f70-136">mobilePhone</span></span> | <span data-ttu-id="48f70-137">El número de teléfono móvil del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-137">The user's cellphone number.</span></span>|
|<span data-ttu-id="48f70-138">officeLocation</span><span class="sxs-lookup"><span data-stu-id="48f70-138">officeLocation</span></span> | <span data-ttu-id="48f70-139">La ubicación de la oficina física del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-139">The user's physical office location.</span></span>|
|<span data-ttu-id="48f70-140">preferredLanguage</span><span class="sxs-lookup"><span data-stu-id="48f70-140">preferredLanguage</span></span> | <span data-ttu-id="48f70-141">El idioma de preferencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-141">The user's language of preference.</span></span>|
|<span data-ttu-id="48f70-142">surname</span><span class="sxs-lookup"><span data-stu-id="48f70-142">surname</span></span>| <span data-ttu-id="48f70-143">El apellido del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-143">The last name of the user.</span></span> |
|<span data-ttu-id="48f70-144">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="48f70-144">userPrincipalName</span></span>| <span data-ttu-id="48f70-145">El nombre principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-145">The user's principal name.</span></span> |

<br/>

<span data-ttu-id="48f70-146">Para obtener información detallada y una lista de todas las propiedades, consulte el objeto [user](user.md).</span><span class="sxs-lookup"><span data-stu-id="48f70-146">For details and a list of all the properties, see the [user](user.md) object.</span></span>

## <a name="common-operations"></a><span data-ttu-id="48f70-147">Operaciones comunes</span><span class="sxs-lookup"><span data-stu-id="48f70-147">Common operations</span></span>

> <span data-ttu-id="48f70-148">**Nota:** Algunas de estas operaciones requieren permisos adicionales.</span><span class="sxs-lookup"><span data-stu-id="48f70-148">**Note:** Some of these operations require additional permissions.</span></span>

| <span data-ttu-id="48f70-149">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="48f70-149">Path</span></span>    | <span data-ttu-id="48f70-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="48f70-150">Description</span></span> |
|:---------|:-------------|
|[`/users`](../api/user_list.md) | <span data-ttu-id="48f70-151">Enumera los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="48f70-151">Lists users in the organization.</span></span> |
|[`/users/{id}`](../api/user_get.md) | <span data-ttu-id="48f70-152">Obtiene un usuario específico por su identificador.</span><span class="sxs-lookup"><span data-stu-id="48f70-152">Gets a specific user by id.</span></span> |
|[`/users/{id}/photo/$value`](../api/profilephoto_get.md)| <span data-ttu-id="48f70-153">Obtiene la foto de perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-153">Gets the user's profile photo.</span></span> |
|[`/users/{id}/manager`](../api/user_list_manager.md) | <span data-ttu-id="48f70-154">Obtiene el administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-154">Gets the user's manager.</span></span> |
|[`/users/{id}/messages`](../api/user_list_messages.md)| <span data-ttu-id="48f70-155">Enumera los mensajes de correo electrónico del usuario en su bandeja de entrada principal.</span><span class="sxs-lookup"><span data-stu-id="48f70-155">Lists the user's email messages in their primary inbox.</span></span> |
|[`/users/{id}/events`](../api/user_list_events.md) | <span data-ttu-id="48f70-156">Enumera los eventos próximos del usuario en su calendario.</span><span class="sxs-lookup"><span data-stu-id="48f70-156">Lists the user's upcoming events in their calendar.</span></span> |
|[`/users/{id}/drive`](../api/drive_get.md)| <span data-ttu-id="48f70-157">Obtiene el almacén de archivos del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="48f70-157">Gets the user's OneDrive file store.</span></span> |
|[`/users/{id}/memberOf`](../api/user_list_memberof.md)| <span data-ttu-id="48f70-158">Enumera los grupos de los que el usuario es miembro.</span><span class="sxs-lookup"><span data-stu-id="48f70-158">Lists the groups that the user is a member of.</span></span> |
