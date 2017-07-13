<span data-ttu-id="7df2c-p109">El ejemplo siguiente busca el grupo que tiene la extensión `graphlearn_courses` con un `courseId` de coincidencia de valor de propiedad `123`, y obtiene las propiedades del grupo **displayName**, **id** y **descripción** y los datos personalizados en la extensión `graphlearn_courses`. (En la consulta actual, asegúrese de aplicar la codificación de la URL según sea necesario).</span><span class="sxs-lookup"><span data-stu-id="7df2c-p109">The following example looks for the group that has the `graphlearn_courses` extension with a `courseId` property value matching `123`, and gets the group properties **displayName**, **id**, and **description**, and the custom data in the `graphlearn_courses` extension. (In the actual query, make sure you apply URL encoding as necessary.)</span></span>

El ejemplo siguiente busca el grupo que tiene la extensión `graphlearn_courses` con un `courseId` de coincidencia de valor de propiedad `123`, y obtiene las propiedades del grupo **displayName**, **id** y **descripción** y los datos personalizados en la extensión `graphlearn_courses`. (En la consulta actual, asegúrese de aplicar la codificación de la URL según sea necesario).

#### <span data-ttu-id="7df2c-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7df2c-157">Request</span></span>
<a id="request" class="xliff"></a>

```http
GET https://graph.microsoft.com/v1.0/groups?$filter=graphlearn_courses/courseId eq ‘123’&$select=displayName,id,description,graphlearn_courses
```


##### <span data-ttu-id="7df2c-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7df2c-158">Response</span></span>
<a id="response" class="xliff"></a>
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-length: 326
{
  "value": [
    {
      "displayName": "New Managers March 2017",
      "id": "14429ae5-3e74-41a2-9fa8-028fbb984637",
      "description": "New Managers training course for March 2017",
      "graphlearn_courses": {
        "@odata.type": "#microsoft.graph.ComplexExtensionValue",
        "courseId":"123",
        "courseName":"New Managers",
        "courseType":"Online"
      }
    }
  ]
}
```

## <span data-ttu-id="7df2c-159">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7df2c-159">See also</span></span>
<a id="see-also" class="xliff"></a>

- [<span data-ttu-id="7df2c-160">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="7df2c-160">Add custom data to resources using extensions</span></span>](extensibility_overview.md)
- [<span data-ttu-id="7df2c-161">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="7df2c-161">Add custom data to users using open extensions (preview)</span></span>](extensibility_open_users.md)
- <span data-ttu-id="7df2c-162">
  [Dominios de Office 365](https://technet.microsoft.com/en-us/library/office-365-domains.aspx)</span><span class="sxs-lookup"><span data-stu-id="7df2c-162">[Office 365 domains](https://technet.microsoft.com/en-us/library/office-365-domains.aspx)</span></span>
- [<span data-ttu-id="7df2c-163">Agregar y comprobar un dominio para el nuevo Office 365</span><span class="sxs-lookup"><span data-stu-id="7df2c-163">Adding and Verifying a Domain for the NEW Office 365</span></span>](http://office365support.ca/adding-and-verifying-a-domain-for-the-new-office-365/)
- [<span data-ttu-id="7df2c-164">Tipo de recurso schemaExtension</span><span class="sxs-lookup"><span data-stu-id="7df2c-164">schemaExtension resource type</span></span>](../api-reference/v1.0/resources/schemaextension.md)
- [<span data-ttu-id="7df2c-165">Listar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="7df2c-165">List schemaExtensions</span></span>](../api-reference/v1.0/api/schemaextension_list.md)
- [<span data-ttu-id="7df2c-166">Crear schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="7df2c-166">Create schemaExtension</span></span>](../api-reference/v1.0/api/schemaextension_post_schemaextensions.md)
- [<span data-ttu-id="7df2c-167">Obtener schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="7df2c-167">Get schemaExtension</span></span>](../api-reference/v1.0/api/schemaextension_get.md)
- [<span data-ttu-id="7df2c-168">Actualizar schemaExtension</span><span class="sxs-lookup"><span data-stu-id="7df2c-168">Update schemaExtension</span></span>](../api-reference/v1.0/api/schemaextension_update.md)
- [<span data-ttu-id="7df2c-169">Eliminar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="7df2c-169">Delete schemaExtension</span></span>](../api-reference/v1.0/api/schemaextension_delete.md)
