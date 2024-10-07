# SIS257_TiendaRopa
# JANDRALENCERIA

**JANDRALENCERIA** es una tienda de ropa que ofrece productos tanto de manera virtual como presencial. Nos especializamos en ropa de lencería de alta calidad para nuestros clientes, brindando un servicio personalizado y cercano.

## descripción del negocio

JANDRALENCERIA se caracteriza por la venta de prendas de vestir exclusivas y variadas para todo tipo de gustos y necesidades. Nos encontramos en una plataforma virtual donde los usuarios pueden realizar compras fácilmente desde la comodidad de su hogar, además de contar con una tienda física para quienes prefieran una experiencia presencial.

### tipos de productos:
- Conjuntos de lencería
- Ropa deportiva
- Medias
- Ropa íntima de hombre
- Ropa íntima de niñ@
- Colales
- Brasier
- Ropa casual

### plataforma de ventas:
- **virtual**: Tienda en línea con entregas a domicilio.
- **presencial**: Local físico disponible para atención directa.

## entidades del sistema

### 1. usuarios
Los usuarios registrados podrán hacer compras tanto en línea como en la tienda física. Los campos necesarios para los usuarios son:
- **id_usuario**: Identificador único del usuario.
- **Nombre**: Nombre del usuario.
- **Apellido**: Apellido del usuario.
- **Celular**: Número de contacto.
- **Dirección**: Domicilio del usuario para entregas.
- **Correo electrónico**: Correo para comunicaciones.
- **Contraseña**: Para acceder al sistema.
- **Tipo de usuario**: Cliente o Administrador.

### 2. productos
Los productos disponibles para la venta en la tienda incluyen los siguientes campos:
- **id_producto**: Identificador único del producto.
- **Nombre**: Nombre del producto.
- **Descripción**: Detalles del producto.
- **Color**: Color disponible.
- **Talle**: Talla del producto.
- **Precio**: Precio del producto.
- **Cantidad**: Cantidad disponible.
- **Categoría**: Clasificación del producto.
- **Fecha de ingreso**: Fecha en que el producto fue añadido.

### 3. metodos-de-pago
Los métodos de pago disponibles para la tienda incluyen:
- **id_metodo_pago**: Identificador único del método de pago.
- **Efectivo**: Pago directo en la tienda física.
- **Transferencia Bancaria (QR)**: Pagos mediante transferencia bancaria utilizando código QR.

### 4. metodos-de-envio
Para la entrega de productos, los métodos de envío disponibles son:
- **id_metodo_envio**: Identificador único del método de envío.
- **Envío a domicilio**: Los productos serán enviados directamente a la dirección registrada por el cliente.
- **Recogida en tienda**: Los clientes podrán recoger sus productos en el local físico de JANDRALENCERIA.

### 5. ordenes-de-pedidos
Cada compra realizada genera una orden con los siguientes detalles:
- **id_orden_pedido**: Identificador único de la orden.
- **Usuario**: Cliente que realizó la compra.
- **Lista de productos**: Productos adquiridos.
- **Cantidad de productos**: Total de artículos en la orden.
- **Total de la compra**: Importe total a pagar.
- **Método de pago**: Forma en que se realizó el pago.
- **Método de envío**: Método de entrega seleccionado.
- **Estado del pedido**: Pendiente, Enviado, Entregado.
- **Fecha de la orden**: Día en que se realizó la compra.

### 6. categorias-de-producto
Los productos se agrupan por categorías:
- **id_categoria_producto**: Identificador único de la categoría.
- **Nombre**: Nombre de la categoría (Conjuntos de lencería, Ropa deportiva, etc.).
- **Descripción**: Descripción de la categoría.
- **Subcategorías**: Clasificación adicional si aplica.

### 7. descuentos-y-promociones
Se pueden aplicar descuentos a los productos:
- **id_descuento**: Identificador único del descuento.
- **Tipo de descuento**: Porcentaje o cantidad fija.
- **Monto de descuento**: Valor del descuento.
- **Producto aplicable**: Productos que reciben el descuento.
- **Fecha de inicio y fin**: Duración de la promoción.

### 8. resenas-de-productos
Los clientes pueden dejar opiniones sobre los productos:
- **id_resena**: Identificador único de la reseña.
- **Producto**: Producto reseñado.
- **Usuario**: Cliente que dejó la reseña.
- **Calificación**: Puntuación de 1 a 5 estrellas.
- **Comentario**: Opinión del cliente.
- **Fecha de la reseña**: Fecha en que se realizó la reseña.

### 9. facturas
Cada transacción genera una factura:
- **id_factura**: Identificador único de la factura.
- **Orden**: Referencia a la orden de compra.
- **Usuario**: Cliente que recibió la factura.
- **Fecha de emisión**: Fecha de la factura.
- **Total**: Monto total de la compra.
- **Estado**: Pagada, Pendiente.

### 10. historial-de-pedidos
El historial permite ver todas las órdenes de un cliente:
- **id_historial_pedido**: Identificador único del historial.
- **Usuario**: Cliente.
- **Lista de órdenes**: Pedidos realizados por el cliente.
- **Fecha de cada pedido**: Fechas de las compras.

### 11. cupones-de-descuento
Los clientes pueden aplicar cupones en sus compras:
- **id_cupon_descuento**: Identificador único del cupón.
- **Código del cupón**: Código aplicable en la compra.
- **Descuento**: Valor del descuento aplicado.
- **Fecha de inicio y caducidad**: Vigencia del cupón.
- **Condiciones de uso**: Reglas para utilizar el cupón.

### 12. chat-de-atencion-al-cliente
Los clientes pueden comunicarse con el soporte mediante un enlace directo a WhatsApp:
- **id_chat_atencion**: Identificador único de la conversación.
- **Usuario**: Cliente que realiza la consulta.
- **Mensaje**: Texto del mensaje enviado.
- **Fecha y hora del mensaje**: Registro de la conversación.
- **Enlace a WhatsApp**: Enlace directo para iniciar una conversación con el soporte.

### 13. historial-de-transacciones
Se almacenan todas las transacciones realizadas por los clientes:
- **id_historial_transaccion**: Identificador único de la transacción.
- **Usuario**: Cliente que realizó la transacción.
- **Fecha de transacción**: Fecha en que se realizó el pago.
- **Método de pago**: Forma en que se pagó (Efectivo, Transferencia).
- **Total**: Importe de la transacción.
- **Estado**: Éxito, Fallido, Pendiente.

## objetivo del repositorio
Este repositorio está destinado a desarrollar el sistema de ventas de JANDRALENCERIA, el cual permitirá gestionar usuarios, productos, métodos de pago y envío, así como órdenes, facturación y soporte al cliente. Además, se incluyen funcionalidades como reseñas, cupones de descuento y un chat de atención directa a través de WhatsApp.
