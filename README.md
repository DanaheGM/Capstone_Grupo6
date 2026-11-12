BudSound

App móvil para pedirle canciones al DJ en un evento. Es nuestro proyecto de título (Capstone APT) en Duoc UC, 2026.

De qué se trata

En las fiestas y eventos siempre pasa lo mismo: la gente se acerca a la cabina a pedir canciones, el DJ no escucha bien, se le llena de papelitos o simplemente no puede atender a todos. BudSound busca ordenar eso.

El DJ comparte un código QR en el evento. Los asistentes lo escanean desde la app, buscan la canción que quieren y se la mandan al DJ con una propina. El DJ ve las solicitudes en el momento y decide cuáles acepta, así que sigue teniendo el control de lo que suena.

La propina solo se cobra si el DJ acepta la canción. Si la rechaza, no se cobra nada.

Cómo funciona
El DJ vincula su cuenta de MercadoPago (es obligatorio antes de crear un evento).
Crea el evento y la app genera el QR.
El participante escanea el QR, busca una canción y elige el monto de la propina (entre $500 y $20.000).
Al enviar la solicitud, el pago queda reservado, pero todavía no se cobra.
El DJ tiene 7 minutos para aceptar o rechazar.
Si acepta, se cobra la propina.
Si rechaza, la reserva se cancela.
Al terminar, el DJ cierra el evento y ve cuánto recaudó y un resumen de las solicitudes.
Roles

La app es una sola, pero al iniciar sesión se entra como Participante o como DJ, y cada uno tiene su propia navegación.

Participante:

Escanear el QR del evento
Buscar canciones
Enviar una solicitud con propina
Ver si su solicitud fue aceptada o rechazada

DJ:

Vincular su cuenta de MercadoPago
Crear un evento (solo uno activo a la vez)
Recibir las solicitudes en tiempo real y aceptarlas o rechazarlas
Cerrar el evento y revisar lo recaudado
Reglas que definimos
Las solicitudes se ordenan por orden de llegada, no por el monto de la propina.
Pagar no asegura que la canción suene. Eso siempre lo decide el DJ.
Una persona no puede pedir la misma canción más de una vez cada 15 minutos.
El DJ recibe el dinero directo en su cuenta. BudSound nunca guarda dinero de otros; solo se queda con su comisión.
Modelo de negocio

Para el DJ la app es gratis. BudSound cobra una comisión de entre 5% y 10% sobre cada solicitud aceptada, que se descuenta automáticamente al momento del pago.

Algunas decisiones del proyecto

Propina en vez de "prioridad". La primera idea era cobrar para que una canción pasara antes en la fila. Antes de empezar a programar nos dimos cuenta de que eso podía chocar con los términos de servicio de Spotify y YouTube, así que cambiamos el modelo: ahora es una propina para el DJ y la fila siempre va por orden de llegada.

No reproducimos música. Por el mismo motivo, la app no reproduce canciones. Usamos la iTunes Search API solo para obtener el nombre, el artista y la portada, y así poder buscarlas.

De Transbank a MercadoPago. Partimos con Transbank Webpay y después nos cambiamos a MercadoPago. Con MercadoPago armamos el split de pagos (cada DJ recibe directo en su cuenta) y la reserva del pago antes de cobrarlo.

Diseño
Fondo oscuro con detalles en rosa neón y botones verde lima, pensado para usarse de noche en un evento.
Modo daltónico, que cambia el verde y el rojo por azul, naranja y amarillo.
Pantallas de bienvenida para quien usa la app por primera vez.
Verificación de correo al registrarse.
Tecnologías
Flutter (app, un solo código para todo)
Node.js con Express (backend)
PostgreSQL (base de datos)
Socket.io (solicitudes en tiempo real)
iTunes Search API (búsqueda de canciones)
MercadoPago (pagos)
Railway (hosting)
Lo que no incluye esta versión

Dejamos fuera del alcance del MVP:

Reproducir música dentro de la app
Perfil público del DJ
Ofrecer el servicio a locales
Pago por transferencia
Equipo
Danahe González
Gabriel Sepúlveda
Benjamín Valenzuela

Trabajamos con Scrum durante 18 semanas, divididas en 7 sprints.
