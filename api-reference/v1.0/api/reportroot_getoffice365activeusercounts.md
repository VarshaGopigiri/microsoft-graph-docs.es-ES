# <a name="reportroot-getoffice365activeusercounts"></a><span data-ttu-id="c9f14-101">reportRoot: getOffice365ActiveUserCounts</span><span class="sxs-lookup"><span data-stu-id="c9f14-101">reportRoot: getOffice365ActiveUserCounts</span></span>

<span data-ttu-id="c9f14-102">Obtiene el número de usuarios activos diarios en el período de informe por producto.</span><span class="sxs-lookup"><span data-stu-id="c9f14-102">Get the count of daily active users in the reporting period by product.</span></span>

> <span data-ttu-id="c9f14-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="c9f14-103">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="c9f14-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="c9f14-104">Permissions</span></span>

<span data-ttu-id="c9f14-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c9f14-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="c9f14-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c9f14-107">Permission type</span></span>                        | <span data-ttu-id="c9f14-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c9f14-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="c9f14-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c9f14-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="c9f14-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c9f14-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="c9f14-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c9f14-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c9f14-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c9f14-112">Not supported.</span></span>                           |
| <span data-ttu-id="c9f14-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c9f14-113">Application</span></span>                            | <span data-ttu-id="c9f14-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c9f14-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="c9f14-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c9f14-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActiveUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="c9f14-116">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="c9f14-116">Function parameters</span></span>

<span data-ttu-id="c9f14-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="c9f14-117">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="c9f14-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c9f14-118">Parameter</span></span> | <span data-ttu-id="c9f14-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9f14-119">Type</span></span>   | <span data-ttu-id="c9f14-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9f14-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="c9f14-121">period</span><span class="sxs-lookup"><span data-stu-id="c9f14-121">period</span></span>    | <span data-ttu-id="c9f14-122">cadena</span><span class="sxs-lookup"><span data-stu-id="c9f14-122">string</span></span> | <span data-ttu-id="c9f14-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c9f14-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="c9f14-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="c9f14-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="c9f14-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c9f14-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="c9f14-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="c9f14-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="c9f14-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c9f14-127">Request headers</span></span>

| <span data-ttu-id="c9f14-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9f14-128">Name</span></span>          | <span data-ttu-id="c9f14-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9f14-129">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="c9f14-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="c9f14-130">Authorization</span></span> | <span data-ttu-id="c9f14-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c9f14-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="c9f14-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9f14-133">Response</span></span>

<span data-ttu-id="c9f14-134">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="c9f14-134">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="c9f14-135">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9f14-135">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="c9f14-136">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="c9f14-136">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="c9f14-137">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="c9f14-137">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="c9f14-138">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="c9f14-138">Report Refresh Date</span></span>
- <span data-ttu-id="c9f14-139">Office 365</span><span class="sxs-lookup"><span data-stu-id="c9f14-139">Office 365</span></span>
- <span data-ttu-id="c9f14-140">Exchange</span><span class="sxs-lookup"><span data-stu-id="c9f14-140">Exchange</span></span>
- <span data-ttu-id="c9f14-141">OneDrive</span><span class="sxs-lookup"><span data-stu-id="c9f14-141">OneDrive</span></span>
- <span data-ttu-id="c9f14-142">SharePoint</span><span class="sxs-lookup"><span data-stu-id="c9f14-142">SharePoint</span></span>
- <span data-ttu-id="c9f14-143">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="c9f14-143">Skype For Business</span></span> 
- <span data-ttu-id="c9f14-144">Yammer</span><span class="sxs-lookup"><span data-stu-id="c9f14-144">Yammer</span></span>
- <span data-ttu-id="c9f14-145">Teams</span><span class="sxs-lookup"><span data-stu-id="c9f14-145">Teams</span></span>
- <span data-ttu-id="c9f14-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="c9f14-146">Report Date</span></span>
- <span data-ttu-id="c9f14-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="c9f14-147">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="c9f14-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c9f14-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="c9f14-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c9f14-149">Request</span></span>

<span data-ttu-id="c9f14-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c9f14-150">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activeusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActiveUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="c9f14-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9f14-151">Response</span></span>

<span data-ttu-id="c9f14-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9f14-152">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="c9f14-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="c9f14-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Office 365,Exchange,OneDrive,SharePoint,Skype For Business,Yammer,Teams,Report Date,Report Period
```
