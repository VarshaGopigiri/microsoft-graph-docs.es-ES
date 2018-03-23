# <a name="reportroot-getteamsuseractivityusercounts"></a><span data-ttu-id="2d12a-101">reportRoot: getTeamsUserActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="2d12a-101">reportRoot: getTeamsUserActivityUserCounts</span></span>

<span data-ttu-id="2d12a-102">Obtener el número de usuarios de Microsoft Teams por tipo de actividad.</span><span class="sxs-lookup"><span data-stu-id="2d12a-102">Get the number of Microsoft Teams users by activity type.</span></span> <span data-ttu-id="2d12a-103">Los tipos de actividad son el número de mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipos.</span><span class="sxs-lookup"><span data-stu-id="2d12a-103">The activity types are number of teams chat messages, private chat messages, calls, or meetings.</span></span>

## <a name="permissions"></a><span data-ttu-id="2d12a-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="2d12a-104">Permissions</span></span>

<span data-ttu-id="2d12a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2d12a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="2d12a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2d12a-107">Permission type</span></span>                        | <span data-ttu-id="2d12a-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2d12a-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="2d12a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2d12a-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="2d12a-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d12a-110">Not supported.</span></span>                           |
| <span data-ttu-id="2d12a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d12a-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2d12a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d12a-112">Not supported.</span></span>                           |
| <span data-ttu-id="2d12a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2d12a-113">Application</span></span>                            | <span data-ttu-id="2d12a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="2d12a-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="2d12a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d12a-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="2d12a-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d12a-116">Request parameters</span></span>

<span data-ttu-id="2d12a-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="2d12a-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="2d12a-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2d12a-118">Parameter</span></span> | <span data-ttu-id="2d12a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d12a-119">Type</span></span>   | <span data-ttu-id="2d12a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d12a-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="2d12a-121">period</span><span class="sxs-lookup"><span data-stu-id="2d12a-121">period</span></span>    | <span data-ttu-id="2d12a-122">cadena</span><span class="sxs-lookup"><span data-stu-id="2d12a-122">string</span></span> | <span data-ttu-id="2d12a-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="2d12a-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="2d12a-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="2d12a-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="2d12a-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="2d12a-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="2d12a-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2d12a-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="2d12a-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2d12a-127">Request headers</span></span>

| <span data-ttu-id="2d12a-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="2d12a-128">Name</span></span>          | <span data-ttu-id="2d12a-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d12a-129">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="2d12a-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="2d12a-130">Authorization</span></span> | <span data-ttu-id="2d12a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2d12a-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="2d12a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d12a-133">Response</span></span>

<span data-ttu-id="2d12a-134">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="2d12a-134">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="2d12a-135">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d12a-135">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="2d12a-136">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="2d12a-136">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="2d12a-137">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="2d12a-137">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="2d12a-138">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="2d12a-138">Report Refresh Date</span></span>
- <span data-ttu-id="2d12a-139">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="2d12a-139">Report Date</span></span>
- <span data-ttu-id="2d12a-140">Mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="2d12a-140">Team Chat Messages</span></span>
- <span data-ttu-id="2d12a-141">Mensajes de chat privados</span><span class="sxs-lookup"><span data-stu-id="2d12a-141">Private Chat Messages</span></span>
- <span data-ttu-id="2d12a-142">Llamadas</span><span class="sxs-lookup"><span data-stu-id="2d12a-142">API Calls</span></span>
- <span data-ttu-id="2d12a-143">Reuniones</span><span class="sxs-lookup"><span data-stu-id="2d12a-143">meetings</span></span>
- <span data-ttu-id="2d12a-144">Otras acciones</span><span class="sxs-lookup"><span data-stu-id="2d12a-144">Other Actions</span></span>
- <span data-ttu-id="2d12a-145">Período del informe</span><span class="sxs-lookup"><span data-stu-id="2d12a-145">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="2d12a-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d12a-146">Example</span></span>

#### <a name="request"></a><span data-ttu-id="2d12a-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d12a-147">Request</span></span>

<span data-ttu-id="2d12a-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2d12a-148">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="2d12a-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d12a-149">Response</span></span>

<span data-ttu-id="2d12a-150">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d12a-150">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="2d12a-151">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="2d12a-151">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Team Chat Messages,Private Chat Messages,Calls,Meetings,Other Actions,Report Period
```
