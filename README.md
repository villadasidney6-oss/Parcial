#Integrantes
1- Villada Papamija Sidney Kent
2- Urbano Marin Eiver Ferney
3- Pilligue Hernandez Milton Adrian


# Safe-Wallet (Billetera Digital y Cripto)

---

## Fase 1: Auditoría Forense y Diagnóstico

### 1. Dinámica de Trabajo
[🔗 Ver Matriz de Hallazgos en Figma](https://www.figma.com/design/Zm7zxZaIRwTYgi4E4CbZY4/Matriz-de-Hallazgos--Safe-Wallet?node-id=0-1&t=Gb6c4jlcMoxH12o2-1)

### 2. Tareas por Rol (Entregables Individuales)

#### Rol A: Auditor de Ecosistema
**Misión:** [Analizar la Factibilidad y el Hardware.]
- **Errores encontrados:**
  - [Bloqueo automático por fallo en biometría es una falla de ecosistema? Debe
proponer alternativas para mejorar la experiencia sin comprometer la seguridad.]
  - [¿Por qué es una falla de ecosistema?
  - Es una falla de ecosistema porque el sistema depende de varios elementos externos que no siempre funcionan correctamente:]
- **Soluciones propuestas:**
  - [Hardware del dispositivo: Cámara frontal puede estar sucia o dañada.1]
  - [Conexión con servidores de autenticación: Puede haber retrasos o fallos en la comunicación, el sistema asume que el usuario está intentando entrar de forma fraudulenta, cuando en realidad el problema puede ser técnico, por eso bloquear la cuenta automáticamente por 24 horas genera frustración y pérdida de confianza.]

#### Rol B: Analista de Psicología UX
**Misión:** [Detectar la carga cognitiva y el impacto emocional en los usuarios de la app Safe-Wallet.]
-Analisis (Pantalla 2: Trading Saturado)
- **Errores encontrados:**
  - El problema: La pantalla de trading de Safe-Wallet presenta demasiada información al mismo tiempo, lo que genera sobrecarga cognitiva en el usuario. Esto dificulta que pueda concentrarse en la decisión principal que es comprar o vender una criptomoneda.
 - En esta pantalla aparecen gráficos en tiempo real, una lista de aproximadamente 50 criptomonedas, noticias que cambian constantemente y un chat de usuarios activo.
 - No existe una organización clara de la información. Todos los elementos parecen tener la misma importancia, por lo que el usuario no sabe en qué debe fijarse primero.
 - Los botones de “Comprar” y “Vender” tienen el mismo color gris, lo que puede provocar que el usuario realice una acción equivocada al operar.
 - Estrés en la toma de decisiones.
- **Soluciones propuestas:**
  - B.Trading Saturado(Solución a pantalla 2)
  - Se debe dividir la pantalla en secciones o usar pestañas para evitar mostrar todo al mismo tiempo.
  -  Los elementos más importantes, como el precio y el gráfico, deben ser más grandes y llamativos. La información secundaria debe tener menor tamaño o protagonismo. Además, usar espacios ayuda a ordenar mejor la pantalla.
  -  Los botones de “Comprar” y “Vender” deben tener colores distintos (verde y rojo) y un diseño claro. También se debe incluir una confirmación antes de realizar la operación.
  -  Se deben limitar las actualizaciones constantes, reducir animaciones innecesarias y evitar mensajes alarmistas. En su lugar, usar un lenguaje más calmado y claro.
  -  Permitir que el usuario configure la pantalla según sus preferencias (ocultar chat, elegir criptomonedas, etc.).


#### Rol C: Especialista en UI y Jerarquía
**Misión:** [Escribe aquí la misión principal del rol]
- **Errores encontrados:**
  Rol C – Especialista en UI y Jerarquía Visual
 FASE 1: Auditoría Forense y Diagnóstico


 Análisis del problema:
 En la aplicación Safe-Wallet se presentan problemas graves en la jerarquía visual y el affordance,
 especialmente en los botones de “Comprar” y “Vender” y en el proceso para retirar fondos.
 Estos problemas generan confusión en los usuarios, errores en las transacciones y desconfianza
 en la plataforma.

 Problema 1: Confusión entre botones “Comprar” y “Vender”
 Los botones de comprar y vender tienen el mismo color gris, lo que provoca que el usuario
 no pueda diferenciarlos fácilmente. Esto es un problema de jerarquía visual y affordance,
 porque los botones no comunican correctamente su función.

 Consecuencias:
 - Usuarios pueden comprar cuando querían vender.
 - Usuarios pueden perder dinero por errores.
 - Se reduce la confianza en la aplicación.
 - Aumenta la carga cognitiva.

 Propuesta de Mejora:
 - Botón Comprar color verde.
 - Botón Vender color rojo.
 - Ubicar los botones en posiciones diferentes.
 - Botón Comprar lado izquierdo.
 - Botón Vender lado derecho.
 - Hacer el botón principal más grande.
 - Agregar iconos (↑ comprar, ↓ vender).

 Esto mejora la jerarquía visual porque el usuario identifica rápidamente la acción principal.

 Problema 2: Menú oculto para retirar fondos
 El retiro de dinero está oculto en muchos menús:
 Configuración → Cuenta → Avanzado → Liquidación.
 Esto es un problema de accesibilidad y arquitectura de información porque retirar dinero
 debería ser una acción fácil y visible, igual que depositar.

 Consecuencias:
 - Usuarios sienten que la app quiere retener su dinero.
 - Genera desconfianza.
 - Mala experiencia de usuario.
 - Sensación de engaño.

 Propuesta de Mejora:
 - Colocar botón “Retirar fondos” en el Dashboard principal.
 - Ubicarlo al lado del botón “Depositar”.
 - Usar icono de transferencia.
 - Máximo 2 pasos para retirar dinero.
 - Mostrar comisiones antes de confirmar el retiro.

 FASE 2: Re-Arquitectura y User Flow

 Propuesta de Flujo de Confianza:

 1. Dashboard
 2. Seleccionar Comprar o Vender
 3. Ingresar monto
 4. Revisión de orden
    - Precio
    - Comisión
    - Tasa de red
    - Total a pagar
 5. Confirmar transacción
 6. Autenticación (biometría o PIN)
 7. Transacción realizada

 Flujo para Retirar Fondos:
 1. Dashboard
 2. Botón Retirar
 3. Seleccionar cuenta bancaria
 4. Mostrar comisión
 5. Confirmar
 6. Autenticación
 7. Retiro realizado

 Este flujo mejora la transparencia, la seguridad y la facilidad de uso.

 FASE 3: Prototipado (Wireframes)

 Propuesta de Pantallas:

 1. Dashboard:
 - Saldo total visible
 - Botones: Depositar / Retirar / Comprar / Vender
 - Lista de criptomonedas en tarjetas

 2. Pantalla de Trading:
 - Gráfica grande
 - Precio actual
 - Input de monto
 - Botón Comprar (verde)
 - Botón Vender (rojo)
 - Botón deslizar para confirmar

 3. Pantalla de Confirmación:
 Desglose:
 Precio: $X
 Comisión: $Y
 Tasa de red: $Z
 Total: $Total

 4. Seguridad:
 Si falla FaceID:
 - Intentar nuevamente
 - Usar PIN
 - Código SMS
 - Código Email
 No bloquear la cuenta inmediatamente.

 Conclusión:
 La aplicación Safe-Wallet tiene problemas graves de jerarquía visual, accesibilidad y affordance.
 La solución es mejorar los colores, tamaños, posiciones de botones, hacer visible el retiro de
 fondos y mostrar los costos antes de confirmar las transacciones. Con estas mejoras se aumenta
 la confianza del usuario, se reducen los errores y se mejora la experiencia de usuario.

#### Rol D: Oficial de Ética y Fricción
**Misión:** Cazar *Dark Patterns* y Fricción Negativa. 

**Errores de cada pantalla:**

- **Costos Ocultos (Pantalla 3: Confirmación de Compra)**
  - **El Problema:** En la pantalla de confirmación, observamos un claro caso de *Drip Pricing* (Precios por Goteo) y Costos Ocultos.
  - **La trampa matemática:** El usuario está comprando 0.05 BTC a un precio de $28,500. El costo base del activo es de $1,425 (0.05 x 28,500). Sin embargo, el "Total a Pagar" exige $1,567.25.
  - **La falta de transparencia:** Hay un sobrecosto de $142.25 (casi un 10% del valor de la transacción) que se agrupa bajo una línea de texto gris, pequeña y sin desglosar que dice: + Tasa de Red y Comisión de Servicio.
  - **Impacto ético:** El usuario se entera del costo real justo en el último segundo, aprovechando la fatiga de la decisión para forzar una transacción desproporcionadamente cara. Esto es inaceptable para una plataforma financiera formal.

- **Confirmshaming y Fricción Negativa (Pantalla 5: Notificación Alarmista)**
  - **El Problema:** Esta pantalla es un compendio de manipulación emocional diseñado para forzar operaciones (y por ende, cobrar comisiones).
  - **Alarmismo (Fear-mongering):** El título en rojo "¡EL MERCADO SE DESPLOMA!" y el subtítulo "Vende ahora o piérdelo todo" generan pánico irracional. En el mundo de las inversiones, las caídas son normales; inducir al pánico provoca que el usuario tome decisiones financieras perjudiciales basadas en el miedo.
  - **Confirmshaming:** Al intentar descartar la acción, la única opción para no vender es un botón que obliga al usuario a aceptar una premisa humillante y aterradora: "No, prefiero perder mis ahorros".
  - **Impacto ético:** Se está castigando psicológicamente al usuario por no realizar la acción que la empresa desea. Esta práctica destruye la percepción de Safe-Wallet como una herramienta "profesional" y la acerca al terreno de las estafas.

**Soluciones para cada pantalla:**

- **A. En la Confirmación de Compra (Solución a Pantalla 3):**
  - **Desglose Obligatorio:** Antes de habilitar el botón de compra, el usuario debe ver un recibo detallado: Monto en BTC + Comisión de Safe-Wallet + Tasa de Red (Minero).
  - **Fricción Positiva:** Reemplazar el botón de un solo toque ("Confirmar Compra") por un mecanismo de confirmación activa, como un "Deslizar para Comprar" (*Swipe to Buy*) o requerir el PIN/Biometría después de mostrar el recibo transparente. Esto asegura que el usuario no compre por accidente y esté 100% consciente del costo final.

- **B. En Situaciones de Alta Volatilidad (Solución a Pantalla 5):**
  - **Alertas Neutrales:** Cambiar el UX Writing por un lenguaje informativo: "El valor de BTC ha bajado un X% en la última hora. Revisa el mercado".
  - **Fricción Positiva en Ventas de Pánico:** Si el usuario decide vender durante una caída abrupta, implementar un modal de advertencia neutro (*Cooling-off prompt*): "Estás a punto de liquidar tus activos durante un periodo de alta volatilidad. ¿Deseas proceder con la venta de 0.05 BTC?".
  - ### 3. Entregable de Fase 1.

### Tabla de diagnóstico

| Aspecto | Diagnóstico | Oportunidad de mejora |
|---|---|---|
| Costos ocultos y retiro de fondos ocultos. | Es el problema más grave porque genera desconfianza en el usuario al ocultar cobros y dificultar el acceso a su dinero. | Mostrar desde el inicio el desglose completo de costos y ubicar la opción de retirar fondos de forma visible, directa y accesible. |

---

## Fase 2: Re-Arquitectura y User Flow en Lucidchart

### 1. El Reto de Simplificación: "Finanzas con Claridad"
[🔗 Ver flujo general en Lucidchart](https://lucid.app/lucidchart/f4541a30-d4fc-468b-8268-a6b27c53f342/edit?viewport_loc=-884%2C-662%2C4988%2C2288%2C0_0&invitationId=inv_cffc7c59-fd8e-4ea0-8f9b-8b8da9f439f7)

### 2. Tareas por Rol en esta Fase

- **Estudiante 1 (Ecosistema):** [🔗 Ver esquema en Lucidchart](https://lucid.app/lucidchart/da588949-1c3d-4186-a9bd-8210c2cc15de/edit?viewport_loc=185%2C339%2C3365%2C1544%2C0_0&invitationId=inv_22fbdec7-51fd-4de8-898b-f2f654a693df)
- **Estudiante 2 (Arquitecto de Información):** [🔗 Ver esquema en Lucidchart](https://lucid.app/lucidspark/6fe8af27-5430-4b27-afa2-3e7909924895/edit?viewport_loc=-1546%2C-2026%2C5760%2C2733%2C0_0&invitationId=inv_4de863c7-cbb4-4901-bb19-78fe46d7b8f3)](#)
- **Estudiante 3 (UX Writer):** [🔗 Pegar enlace aquí](https://lucid.app/lucidchart/1662a9b9-232a-42b5-9f1b-b2abcac9e33a/edit?viewport_loc=-1040%2C-178%2C4401%2C2108%2C0_0&invitationId=inv_94d9f117-8443-4248-906a-9fb3101d1ffc)](#)
- **Estudiante 4 (Validador de Usabilidad):** [🔗 Pegar enlace aquí](https://lucid.app/lucidchart/407baf6f-ec61-43fa-b211-7569cd841190/edit?viewport_loc=-457%2C-230%2C3455%2C1974%2C0_0&invitationId=inv_953876ba-2816-4626-a0cb-f8a402e93494)](#)

---
### 3. Entregable de Fase 2

**Flujo de Pánico (Actual)**  
En el siguiente enlace se encuentra el diagrama de flujo que representa el funcionamiento actual de la app:  
[🔗 Ver diagrama de flujo actual en Lucidchart](https://lucid.app/lucidchart/70081b15-95bf-4732-9a32-ffb2bc03de56/edit?invitationId=inv_7ec24e62-7142-41ac-90ff-3d8103c5f8f3&page=0_0#)

**Flujo de Confianza (Propuesto)**  
En el siguiente enlace se encuentra el diagrama de flujo que representa el funcionamiento correcto de la app, el cual fue creado con el fin de dar solución a los errores que actualmente presenta:  
[🔗 Ver diagrama de flujo propuesto en Lucidchart](https://lucid.app/lucidchart/79c4772a-cb36-4e22-a9ea-4399ed4ffd98/edit?invitationId=inv_50c590bd-d33b-4a1f-8aa3-5b81689be37c&page=0_0#)
## Fase 3: Prototipado de Media Fidelidad (Wireframes)
[🔗 Ver prototipos en Figma (Ecocanje)] (https://www.figma.com/design/MTckv3GFAm2YvtgZh2n5yT/Caso3-EcoEncaje?node-id=104-11&t=ijUymGPci1PzVGyx-1)
