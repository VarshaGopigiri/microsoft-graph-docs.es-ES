---
title: Trabajar con API para el ámbito educativo en Microsoft Graph
description: Las API para el ámbito educativo de Microsoft Graph mejoran los recursos y los datos de Office 365 con la información pertinente para los escenarios de educación, que incluye centros educativos, estudiantes, profesores, clases e inscripciones. Esto hace que resulte fácil compilar soluciones que se integran con recursos educativos.
localization_priority: Priority
ms.openlocfilehash: 8c2131c0806bf17e7241b0a95dc3094c6496505d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880272"
---
# <a name="working-with-education-apis-in-microsoft-graph"></a><span data-ttu-id="6e1a3-104">Trabajar con API para el ámbito educativo en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="6e1a3-104">Working with education APIs in Microsoft Graph</span></span>

<span data-ttu-id="6e1a3-105">Las API para el ámbito educativo de Microsoft Graph mejoran los recursos y los datos de Office 365 con la información pertinente para los escenarios de educación, que incluye centros educativos, estudiantes, profesores, clases e inscripciones.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-105">The education APIs in Microsoft Graph enhance Office 365 resources and data with information that is relevant for education scenarios, including schools, students, teachers, classes, and enrollments.</span></span> <span data-ttu-id="6e1a3-106">Esto hace que resulte fácil compilar soluciones que se integran con recursos educativos.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-106">This makes it easy for you to build solutions that integrate with educational resources.</span></span>

<span data-ttu-id="6e1a3-107">Las API para el ámbito educativo incluyen recursos de generación de listados y de tareas que puede usar para interactuar con los servicios de generación de listas de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-107">The education APIs include rostering resources and assignments resources that you can use to interact with the rostering services in Microsoft Teams.</span></span> <span data-ttu-id="6e1a3-108">Puede usar estos recursos para administrar un listado de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-108">You can use these resources to manage a school roster.</span></span>

## <a name="authorization"></a><span data-ttu-id="6e1a3-109">Autorización</span><span class="sxs-lookup"><span data-stu-id="6e1a3-109">Authorization</span></span>

<span data-ttu-id="6e1a3-110">Para llamar a las API para el ámbito educativo de Microsoft Graph, la aplicación tiene que adquirir un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-110">To call the education APIs in Microsoft Graph, your app will need to acquire an access token.</span></span> <span data-ttu-id="6e1a3-111">Para obtener más información sobre los tokens de acceso, vea [Obtener tokens de acceso para llamar a Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview).</span><span class="sxs-lookup"><span data-stu-id="6e1a3-111">For details about access tokens, see [Get access tokens to call Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview).</span></span> <span data-ttu-id="6e1a3-112">La aplicación también necesitará los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-112">Your app will also need the appropriate permissions.</span></span> <span data-ttu-id="6e1a3-113">Para obtener más información, vea [Permisos para el ámbito educativo](/graph/permissions-reference#education-permissions).</span><span class="sxs-lookup"><span data-stu-id="6e1a3-113">For more information, see [Education permissions](/graph/permissions-reference#education-permissions).</span></span> 

### <a name="app-permissions-to-enable-school-it-admins-to-consent"></a><span data-ttu-id="6e1a3-114">Permisos de aplicación para habilitar a los administradores de TI del centro educativo para dar consentimiento</span><span class="sxs-lookup"><span data-stu-id="6e1a3-114">App permissions to enable school IT admins to consent</span></span> 

<span data-ttu-id="6e1a3-115">Para implementar aplicaciones que se integran con las API para el ámbito educativo de Microsoft Graph, los administradores de TI del centro educativo deben dar primero consentimiento a los permisos que solicita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-115">To deploy apps that are integrated with the Education APIs in Microsoft Graph, school IT admins must first grant consent to the permissions requested by the app.</span></span> <span data-ttu-id="6e1a3-116">Este consentimiento únicamente hay que darlo una sola vez, a menos que cambien los permisos.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-116">This consent has to be granted only once, unless the permissions change.</span></span> <span data-ttu-id="6e1a3-117">Cuando el administrador da el consentimiento, la aplicación se aprovisiona para todos los usuarios del inquilino.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-117">After the admin consents, the app is provisioned for all users in the tenant.</span></span>

<span data-ttu-id="6e1a3-118">Para mostrar un cuadro de diálogo de consentimiento, use la siguiente llamada a REST.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-118">To show a consent dialog box, use the following REST call.</span></span>

```
GET https://login.microsoftonline.com/{tenant}/adminconsent?
client_id={clientId}&state=12345&redirect_uri={redirectUrl}
```

|<span data-ttu-id="6e1a3-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6e1a3-119">Parameter</span></span>|<span data-ttu-id="6e1a3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e1a3-120">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6e1a3-121">Tenant</span><span class="sxs-lookup"><span data-stu-id="6e1a3-121">Tenant</span></span>|<span data-ttu-id="6e1a3-122">Identificador de inquilino del centro educativo.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-122">Tenant ID of the school.</span></span> <span data-ttu-id="6e1a3-123">Use el identificador completo, que incluye onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-123">Use the full ID, which includes onmicrosoft.com.</span></span>|
|<span data-ttu-id="6e1a3-124">clientId</span><span class="sxs-lookup"><span data-stu-id="6e1a3-124">clientId</span></span>|<span data-ttu-id="6e1a3-125">Identificador de cliente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-125">Client ID of the app.</span></span>|
|<span data-ttu-id="6e1a3-126">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="6e1a3-126">redirectUrl</span></span>|<span data-ttu-id="6e1a3-127">Dirección URL de redireccionamiento de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6e1a3-127">App redirect URL.</span></span>|


## <a name="rostering"></a><span data-ttu-id="6e1a3-128">Generación de listados</span><span class="sxs-lookup"><span data-stu-id="6e1a3-128">Rostering</span></span>

<span data-ttu-id="6e1a3-129">Las API de generación de listados permiten extraer datos de un inquilino de Office 365 del centro educativo aprovisionado con [Microsoft School Data Sync](https://sds.microsoft.com/). Estas API ofrecen acceso a información sobre centros educativos, secciones, profesores, alumnos y listados.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-129">The rostering APIs enable you to extract data from a school's Office 365 tenant provisioned with [Microsoft School Data Sync](https://sds.microsoft.com/). These APIs provide access to information about schools, sections, teachers, students, and rosters.</span></span> <span data-ttu-id="6e1a3-130">La API admiten tanto escenarios solo de aplicación (sincronización) como escenarios de aplicación y usuario (interactivos).</span><span class="sxs-lookup"><span data-stu-id="6e1a3-130">The APIs support both app-only (sync) scenarios, and app + user (interactive) scenarios.</span></span> <span data-ttu-id="6e1a3-131">Las API que admiten escenarios interactivos aplican directivas de RBAC adecuadas a la región según el rol de usuario que llama a la API.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-131">The APIs that support interactive scenarios enforce region-appropriate RBAC policies based on the user role calling the API.</span></span> <span data-ttu-id="6e1a3-132">Esto proporciona una API coherente y una superficie de directiva mínima, independientemente de la configuración de administración de inquilinos.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-132">This provides a consistent API and minimal policy surface, regardless of the administrative configuration within tenants.</span></span> <span data-ttu-id="6e1a3-133">Además, las API proporcionan también permisos específicos del ámbito educativo para asegurarse de que el usuario correcto tiene acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-133">In addition, the APIs also provide education-specific permissions to ensure that the right user has access to the data.</span></span>

<span data-ttu-id="6e1a3-134">Puede usar las API de generación de listados para permitir que un usuario de la aplicación conozca:</span><span class="sxs-lookup"><span data-stu-id="6e1a3-134">You can use the rostering APIs to enable an app user to know:</span></span>

- <span data-ttu-id="6e1a3-135">Quién soy</span><span class="sxs-lookup"><span data-stu-id="6e1a3-135">Who I am</span></span>
- <span data-ttu-id="6e1a3-136">Clases a las que asisto o que imparto</span><span class="sxs-lookup"><span data-stu-id="6e1a3-136">What classes I attend or teach</span></span>
- <span data-ttu-id="6e1a3-137">Lo que tengo que hacer y cuándo</span><span class="sxs-lookup"><span data-stu-id="6e1a3-137">What I need to do and by when</span></span>

<span data-ttu-id="6e1a3-138">Las API de generación de listados ofrecen los siguientes recursos claves:</span><span class="sxs-lookup"><span data-stu-id="6e1a3-138">The rostering APIs provide the following key resources:</span></span>

- <span data-ttu-id="6e1a3-139">[educationSchool](educationschool.md): representa el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-139">[educationSchool](educationschool.md) - Represents the school.</span></span>
- <span data-ttu-id="6e1a3-140">[educationClass](educationclass.md): representa una clase en un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-140">[educationClass](educationclass.md) - Represents a class within a school.</span></span>
- <span data-ttu-id="6e1a3-141">[educationTerm](educationterm.md): representa una parte designada del año académico.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-141">[educationTerm](educationterm.md) - Represents a designated portion of the academic year.</span></span>
- <span data-ttu-id="6e1a3-142">[educationTeacher](educationteacher.md): representa un usuario con el rol principal de "Profesor".</span><span class="sxs-lookup"><span data-stu-id="6e1a3-142">[educationTeacher](educationteacher.md) - Represents a users with the primary role of 'Teacher'.</span></span>
- <span data-ttu-id="6e1a3-143">[educationStudent](educationstudent.md): representa un usuario con el rol principal de "alumno".</span><span class="sxs-lookup"><span data-stu-id="6e1a3-143">[educationStudent](educationstudent.md) - Represents a users with the primary role of 'student'.</span></span>

<span data-ttu-id="6e1a3-144">Las API de generación de listados admiten los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="6e1a3-144">The rostering APIs support the following scenarios:</span></span>

- [<span data-ttu-id="6e1a3-145">Mostrar todos los centros educativos</span><span class="sxs-lookup"><span data-stu-id="6e1a3-145">List all schools</span></span>](../api/educationroot-list-schools.md) 
- [<span data-ttu-id="6e1a3-146">Mostrar los centros educativos en los que se imparte una clase</span><span class="sxs-lookup"><span data-stu-id="6e1a3-146">List schools in which a class is taught</span></span>](../api/educationclass-list-schools.md)
- [<span data-ttu-id="6e1a3-147">Mostrar los centros educativos correspondientes a un usuario</span><span class="sxs-lookup"><span data-stu-id="6e1a3-147">List schools for a user</span></span>](../api/educationuser-list-schools.md)
- [<span data-ttu-id="6e1a3-148">Obtener todas las clases</span><span class="sxs-lookup"><span data-stu-id="6e1a3-148">Get all classes</span></span>](../api/educationroot-list-classes.md)
- [<span data-ttu-id="6e1a3-149">Obtener las clases de un centro educativo</span><span class="sxs-lookup"><span data-stu-id="6e1a3-149">Get classes in a school</span></span>](../api/educationschool-list-classes.md)
- [<span data-ttu-id="6e1a3-150">Mostrar las clases correspondientes a un usuario</span><span class="sxs-lookup"><span data-stu-id="6e1a3-150">List classes for a user</span></span>](../api/educationuser-list-classes.md)
- [<span data-ttu-id="6e1a3-151">Agregar clases a un centro educativo</span><span class="sxs-lookup"><span data-stu-id="6e1a3-151">Add classes to a school</span></span>](../api/educationschool-post-classes.md)
- [<span data-ttu-id="6e1a3-152">Obtener los alumnos y profesores de una clase</span><span class="sxs-lookup"><span data-stu-id="6e1a3-152">Get students and teachers for a class</span></span>](../api/educationclass-list-members.md)
- [<span data-ttu-id="6e1a3-153">Agregar miembros a una clase</span><span class="sxs-lookup"><span data-stu-id="6e1a3-153">Add members to a class</span></span>](../api/educationclass-post-members.md) 
- [<span data-ttu-id="6e1a3-154">Mostrar los profesores de una clase</span><span class="sxs-lookup"><span data-stu-id="6e1a3-154">List teachers for a class</span></span>](../api/educationclass-list-teachers.md)
- [<span data-ttu-id="6e1a3-155">Obtener los usuarios de un centro educativo</span><span class="sxs-lookup"><span data-stu-id="6e1a3-155">Get users in a school</span></span>](../api/educationschool-list-users.md)

<!-- Should you list delete scenarios here as well? -->

## <a name="next-steps"></a><span data-ttu-id="6e1a3-156">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="6e1a3-156">Next steps</span></span>
<span data-ttu-id="6e1a3-157">Use las API para el ámbito educativo de Microsoft Graph para compilar soluciones educativas con acceso a listados de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-157">Use the Microsoft Graph education APIs to build education solutions that access school rosters.</span></span> <span data-ttu-id="6e1a3-158">Para obtener más información:</span><span class="sxs-lookup"><span data-stu-id="6e1a3-158">To learn more:</span></span>

- <span data-ttu-id="6e1a3-159">Explore los recursos y los métodos que son más útiles para su escenario.</span><span class="sxs-lookup"><span data-stu-id="6e1a3-159">Explore the resources and methods that are most helpful to your scenario.</span></span>
- <span data-ttu-id="6e1a3-160">Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="6e1a3-160">Try the API in the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>

