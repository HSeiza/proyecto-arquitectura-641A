# Requerimiento no funcionales

| # | Atributo       | Metrica                              | Umbral        | Condicion de carga      | Verificacion                     | Consecuencia si no se cumple       |
|---|----------------|--------------------------------------|---------------|-------------------------|----------------------------------|------------------------------      |
| 1 | Disponibilidad | < 7 horas mes                        | 3.5 horas mes | 50 personas al dia      | Logs del servicio y UoTime Robot | Abando y baja adopcion del sistema |
| 2 | Rendimiento    | milisegundos                         | 5 o 6 IPS     | 10 usuarios simultaneos | Pruebas de carga                 | Caida de cualquier servicio        |
| 3 | Recuperabilidad| cada 1 hora backup                   | 1 hora        | Desastres               | BackUp cada 1 hora               | Perdida de contratos comerciales   |
| 4 | Seguridad      | intentos fallidos                    | 3 intentos    | Login de usuario        | Pruebas de penetracion           | Acceso no autorizado al sistema    |

### Esenario 1
-Fuente:    Usuario final
-Estimulo:  Ver catalogo
-Artefacto: Cargar el catalogo de la tienda en el navegador del usuario final
-Entorno:   24/7
-Respuesta: El catalogo en el navegador
-Medida:    Activo el 99.9% mes

## Esenario 2
-Fuente:     Usuario final
-Estimulo:   Calcular costos totales
-Artefacto:  Carrito de compras
-Entorno:    10 usuarios concurrentes
-Respuesta:  Mostrar al usuario el total de su compra
-Medida:     5 o 6 instrucciones en paralelo
## Esenario 3
-Fuente:     Usuario malicioso
-Estimulo:   Intentar iniciar sesion con credenciales incorrectas
-Artefacto:  Modulo de autenticacion
-Entorno:    Operacion normal
-Respuesta:  Bloquear la cuenta tras 3 intentos fallidos
-Medida:     Bloqueo activado en menos de 1 segundo