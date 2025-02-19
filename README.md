Siguiendo la arquitectura propuesta.
Agregar un recurso: 
titular: (carpeta)
nuevo (archivo php)
Response : (archivo php, la ubicación y  el nombre debe ser dado según arquitectura propuesta).Objeto con las siguientes propiedades:
IsOk : [true/false]
Mensaje: [segunCorresponda]
Request: (archivo php, la ubicación y el nombre debe ser dado según arquitectura propuesta. Contiene datos de ejemplo). Objeto con las siguientes propiedades: 
{
  "Titular": {
    "Direccion": {
      "Calle": "BV. SAN MARTIN",
      "CalleNro": "2777",
      "Localidad": "MARCELINO ESCALADA",
      "Provincia": "SANTA FE"
    },
    "NroDocumento": 12345678,
    "ApellidoNombre": "Perez, Remigio Fabian"
  }
}
En el recurso validar que exista una dirección: if($obj->Direccion == null)
Si no existe dirección devolver:
isOk = false
Mensaje: la dirección es obligatoria
En el recurso validar que existe numero documento y apellidoNombre
Sino existe alguno devolver:
IsOk = false
Mensaje: el [numero documento|apellidoNombre] es obligatorio.
En el recurso, si no se cumplen más de una validación, el mensaje debe contener el mensaje de todas las validaciones separadas por “-“ (guión medio.)
En el recurso si esta todo ok devolver
IsOk: true
Mensaje : “Titular agregado correctamente”
