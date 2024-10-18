# SIS257_tiendaropa
Desarrollo de Aplicación Int/Internet II

::: JANDRA LENCERIA ::: JANDRALENCERIA es una tienda de ropa que ofrece productos tanto de manera virtual como presencial. Nos especializamos en ropa de lencería de alta calidad para nuestros clientes, brindando un servicio personalizado y cercano.

Descripción del negocio
JANDRALENCERIA se caracteriza por la venta de prendas de vestir exclusivas y variadas para todo tipo de gustos y necesidades. Nos encontramos en una plataforma virtual donde los usuarios pueden realizar compras fácilmente desde la comodidad de su hogar, además de contar con una tienda física para quienes prefieran una experiencia presencial.

Tipos de productos:
Conjuntos de lencería
Ropa deportiva
Medias
Ropa íntima de hombre
Ropa íntima de niñ@
Colales
Brasier
Ropa casual
Plataforma de ventas:
Virtual: Tienda en línea con entregas a domicilio.
Presencial: Local físico disponible para atención directa.
Entidades del sistema
Usuarios Los usuarios registrados podrán hacer compras tanto en línea como en la tienda física. Los campos necesarios para los usuarios son:
#id_usuario: Identificador único del usuario. nombre: Nombre del usuario. apellido: Apellido del usuario. celular: Número de contacto. dirección: Domicilio del usuario para entregas. correo_electronico: Correo para comunicaciones. contraseña: Para acceder al sistema. tipo_usuario: Cliente o Administrador. 2. Productos Los productos disponibles para la venta en la tienda incluyen los siguientes campos:

#id_producto: Identificador único del producto. nombre: Nombre del producto. descripción: Detalles del producto. color: Color disponible. talle: Talla del producto. precio: Precio del producto. cantidad: Cantidad disponible. categoría: Clasificación del producto. fecha_ingreso: Fecha en que el producto fue añadido. 3. Categorías de Producto Los productos se agrupan por categorías:

#id_categoria: Identificador único de la categoría. nombre: Nombre de la categoría (e.g., Ropa de Hombre, Ropa de Mujer, Accesorios). descripción: Descripción de la categoría. subcategorías: Clasificación adicional si aplica. 4. Métodos de Pago Los métodos de pago disponibles para la tienda incluyen:

#id_metodo_pago: Identificador único del método de pago. tipo_pago: Tipo de pago (Efectivo, Transferencia, Tarjeta de Crédito, etc.). 5. Métodos de Envío Para la entrega de productos, los métodos de envío disponibles son:

#id_metodo_envio: Identificador único del método de envío. tipo_envio: Tipo de envío (Envío a domicilio, Recogida en tienda). 6. Órdenes de Pedidos Cada compra realizada genera una orden con los siguientes detalles:

#id_orden_pedido: Identificador único de la orden. #id_usuario: Identificador del usuario que realizó la compra (FK). fecha_orden: Fecha en que se realizó la compra. total_compra: Importe total a pagar. estado_pedido: Estado de la orden (Pendiente, Enviado, Entregado). #id_metodo_pago: Método de pago utilizado (FK). #id_metodo_envio: Método de envío seleccionado (FK). 7. Detalle de Órdenes Cada orden puede contener múltiples productos, por lo que se detalla lo siguiente:

#id_detalle_orden: Identificador único del detalle. #id_orden_pedido: Identificador de la orden (FK). #id_producto: Identificador del producto (FK). cantidad: Cantidad de cada producto en la orden. precio_unitario: Precio unitario del producto en el momento de la compra. 8. Facturas Cada transacción genera una factura:

#id_factura: Identificador único de la factura. #id_orden_pedido: Referencia a la orden de compra (FK). fecha_emision: Fecha de emisión de la factura. total: Monto total de la compra. estado: Estado de la factura (Pagada, Pendiente). 9. Historial de Pedidos El historial permite ver todas las órdenes de un cliente:

#id_historial: Identificador único del historial. #id_usuario: Identificador del usuario (FK). #id_orden_pedido: Identificador de la orden (FK). fecha_pedido: Fecha de cada pedido. 10. Chat de Atención al Cliente Los clientes pueden comunicarse con el soporte mediante un enlace directo a WhatsApp:

#id_chat_atencion: Identificador único de la conversación. #id_usuario: Identificador del usuario que realiza la consulta (FK). enlace_whatsapp: Enlace directo para iniciar una conversación con el soporte.

Objetivo del repositorio
Este repositorio está destinado a desarrollar el sistema de ventas de JANDRALENCERIA, el cual permitirá gestionar usuarios, productos, métodos de pago y envío, así como órdenes, facturación y soporte al cliente. Además, se incluyen funcionalidades como reseñas, cupon