
# <a name="paging-microsoft-graph-data-in-your-app"></a>Paginación de los datos de Microsoft Graph en la aplicación 

Algunas consultas realizadas en Microsoft Graph devuelven varias páginas de datos debido a la paginación del servidor o al uso del parámetro `$top` para limitar específicamente el tamaño de página en una solicitud. Cuando un conjunto de resultados abarca varias páginas, Microsoft Graph devuelve una propiedad `@odata.nextLink` en la respuesta que contiene una dirección URL a la siguiente página de resultados. 

Por ejemplo, la dirección URL siguiente solicita todos los usuarios en una organización con un tamaño de página de 5 especificado con el parámetro de consulta `$top`:

```html
https://graph.microsoft.com/v1.0/users?$top=5
```

Si el resultado contiene más de cinco usuarios, Microsoft Graph devolverá una propiedad `odata:nextLink` similar a la siguiente junto con la primera página de usuarios.

```json
"@odata.nextLink": "https://graph.microsoft.com/v1.0/users?$top=5&$skiptoken=X%274453707 ... 6633B900000000000000000000%27"
```

Puede recuperar la siguiente página de resultados enviando el valor de dirección URL de la propiedad `@odata:nextLink` a Microsoft Graph. 

```html
https://graph.microsoft.com/v1.0/users?$top=5&$skiptoken=X%274453707 ... 6633B900000000000000000000%27
```

Microsoft Graph continuará devolviendo una referencia a la siguiente página de datos en la propiedad `@odata:nextLink` con cada respuesta, hasta que se hayan leído todas las páginas del resultado.

>**Importante:** Debe incluir la dirección URL completa en la propiedad `@odata:nextLink` de la solicitud de la siguiente página de resultados. Según la API en la que se realice la consulta, el valor de dirección URL `@odata:nextLink` contendrá un `$skiptoken` o un parámetro de consulta `$skip`. La dirección URL contiene también todos los demás parámetros de consulta presentes en la solicitud original. No intente extraer el `$skiptoken` o el valor `$skip` y usarlo en una solicitud diferente. 

El comportamiento de paginación varía entre las distintas API de Microsoft Graph. Al trabajar con datos paginados debe tener en cuenta lo siguiente:

- Las distintas API pueden tener tamaños de página predeterminados y máximos diferentes.
- Las distintas API pueden comportarse de forma diferente si se especifica un tamaño de página (a través del parámetro de consulta `$top`) que supera el tamaño máximo de página para la API. Según la API, se puede omitir el tamaño de página solicitado, se puede usar el tamaño de página máximo predeterminado para la API o Microsoft Graph puede devolver un error. 
- No todos los recursos o relaciones admiten la paginación. Por ejemplo, las consultas a [directoryRoles](../api-reference/v1.0/resources/directoryrole.md) no admiten la paginación. Esto incluye los objetos de rol de lectura así como los miembros de rol.
- Algunas API de Microsoft Graph admiten la paginación hacia atrás anexando el parámetro de consulta `previous-page` (`&previous-page=true`) al valor de dirección URL de la propiedad `@odata:nextLink`. Una vez que se anexe este parámetro a la solicitud, se incluirá en el valor de dirección URL `@odata:nextLink` en las respuestas siguientes. Puede continuar a la paginación hacia atrás hasta que se devuelva una respuesta con un resultado vacío. Si se continúa la paginación se devolverá un error. Como alternativa, puede reanudar la paginación hacia delante desde la respuesta actual si quita el parámetro `previous-page` al enviar la solicitud de la siguiente página de resultados. 

