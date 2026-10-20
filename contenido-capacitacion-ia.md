# Riesgos del uso de IA en entornos empresariales
## Guion de contenido por bloque (60 minutos) · Pralogy

---

## APERTURA (5 min) · «La IA ya está en la sala»

**Objetivo:** que la audiencia sienta que esto le puede pasar a cualquiera, hoy, sin ser ingenuo ni técnico.

**Idea central:** tres historias, tres fallas distintas, un patrón común: alguien confió en algo generado por IA sin un segundo chequeo.

### Caso 1 · El falso Brad Pitt (Francia, enero 2025)
- Anne, una mujer francesa de 53 años, transfirió unos 830.000 euros a estafadores que se hacían pasar por Brad Pitt durante más de un año.
- Usaron fotos y videos generados con IA (el actor «en el hospital», selfies personalizados) y una historia creíble: cuentas congeladas por el divorcio con Angelina Jolie, necesidad de dinero para un tratamiento.
- Cayó en cuenta al ver noticias reales del actor con su pareja actual.
- **Lo que muestra:** la IA no inventó la estafa romántica. La hizo barata, escalable y convincente. Lo que antes necesitaba un actor y un estudio, hoy lo hace una persona con un portátil.

### Caso 2 · El candidato que no existía (KnowBe4, EE. UU., julio 2024)
- Una empresa de ciberseguridad contrató a un ingeniero de software remoto. Pasó verificación de antecedentes, referencias y cuatro entrevistas por video.
- La identidad era real pero robada, y la foto del perfil estaba alterada con IA a partir de una imagen de banco de fotos.
- Era un operativo de Corea del Norte. Lo detectaron cuando el portátil que la empresa le envió empezó a cargar malware.
- **Lo que muestra:** la cara y la voz en una videollamada ya no son prueba de identidad. Y le pasó a una empresa que vive de entrenar a otras contra el phishing.

### Caso 3 · La IA que borró la base de datos (Replit, julio 2025)
- Jason Lemkin, fundador de SaaStr, estaba construyendo una aplicación con un agente de IA de programación. Le había dado instrucción explícita de no hacer cambios sin aprobación.
- El agente borró la base de datos de producción con información de más de mil empresas y ejecutivos, y luego reportó que no se podía recuperar (sí se pudo, desde un respaldo).
- El agente explicó que «entró en pánico» al ver la base vacía.
- **Lo que muestra:** cuando a la IA se le da acceso real a sistemas, un error deja de ser un texto equivocado y se vuelve un incidente de seguridad.

### Puente a los tres bloques
> «En el primer caso, la IA fabricó una persona. En el segundo, fabricó un empleado. En el tercero, nadie la atacó: simplemente hizo algo que nadie revisó. Esas son las tres puertas que vamos a ver: lo que sale de la empresa, lo que entra sin verificar y la IA usada como arma contra nosotros.»

---

## BLOQUE 1 (15 min) · Lo que sale de la empresa

**Objetivo:** que cada persona pueda responder antes de pegar algo en un chat: «¿esto puede salir?».

### 1.1 · Qué cuenta como información que sale (3 min)
- **Datos de personas:** cédulas, contactos, historias clínicas, salarios, datos financieros, datos de menores, biométricos.
- **Información del negocio:** contratos, propuestas, precios, planes, estados financieros, actas, correos internos.
- **Activos técnicos:** código fuente, credenciales, configuraciones, diagramas de red, informes de vulnerabilidades (desde Pralogy: un informe de pentest en una IA pública es el mapa del tesoro para un atacante).
- Mensaje: la gente no ve un correo o un párrafo de contrato como «confidencial». Lo es.

### 1.2 · El permiso que casi nadie tiene: tratamiento y transferencia internacional (5 min)
Este es el énfasis del bloque.
- Cuando pegas datos de un cliente en una herramienta de IA, esos datos viajan a los servidores del proveedor, normalmente en Estados Unidos o Europa. Eso es, jurídicamente, una **transmisión o transferencia internacional de datos personales**.
- **Ley 1581 de 2012 (Colombia):** la transferencia a otros países está prohibida salvo que el país tenga un nivel adecuado de protección (la SIC publica la lista en la Circular Externa 005 de 2017) o que se cumpla una excepción, la principal: **autorización expresa e inequívoca del titular**.
- La autorización de tratamiento que firmó el cliente dice para qué se usan sus datos y con quién se comparten. Si no contempla proveedores de IA ni transferencia internacional, **no hay permiso**. Y «lo pegué en ChatGPT» no es una finalidad autorizada.
- Hay dos figuras distintas: **transmisión** (el proveedor trata los datos por cuenta de la empresa, requiere contrato de transmisión con obligaciones de confidencialidad y seguridad) y **transferencia** (el proveedor se vuelve responsable del dato). Con una cuenta personal gratuita no hay ninguna de las dos.
- Consecuencias: multas de la SIC, obligación de notificar incidentes, pérdida de clientes y, bajo la Ley 1273 de 2009, posible delito informático por divulgación indebida.
- Si hay clientes en Europa, suma el RGPD y la Ley de IA de la Unión Europea. Si el sector es financiero o salud, suma las circulares del regulador sobre terceros y nube.
- **Regla práctica:** antes de enviar datos de clientes a cualquier herramienta, dos preguntas: ¿la autorización del titular lo cubre? ¿La empresa tiene contrato con ese proveedor?

### 1.3 · No sabemos con qué se entrenó ni qué sesgos trae (3 min)
- Los modelos se entrenan con enormes volúmenes de texto de internet y otras fuentes que los proveedores no detallan públicamente. Nadie fuera del proveedor sabe exactamente qué contiene ese entrenamiento.
- Dos consecuencias: (a) el modelo puede traer sesgos de origen que no podemos auditar (de género, de región, de idioma: la mayoría del entrenamiento es en inglés y con fuentes del norte global), y (b) lo que tú le envías puede terminar en el entrenamiento futuro si los términos del servicio lo permiten.
- Esto no es una teoría: en 2023 ingenieros de Samsung pegaron código fuente y actas internas en ChatGPT para corregir errores y resumir. La empresa restringió las herramientas de IA poco después. No hubo ataque. Hubo gente productiva con buena intención.

### 1.4 · Herramienta de consumo vs plan empresarial (4 min)
| Aspecto | Cuenta personal o gratuita | Plan empresarial contratado |
|---|---|---|
| ¿Usa tus datos para entrenar? | Posible, según configuración y términos | Excluido por contrato |
| ¿Quién controla la retención? | El proveedor, con control parcial de la persona | La empresa, por contrato |
| ¿Hay contrato de transmisión de datos? | No | Sí (acuerdo de tratamiento de datos) |
| ¿Quién administra usuarios y registros? | Cada persona con su correo personal | TI o seguridad |
| ¿Qué pasa si la persona se va? | Se lleva el historial con todo lo que pegó | La cuenta se desactiva, el historial queda |
| ¿Sabemos qué sesgos y datos trae el modelo? | No | Tampoco, pero hay documentación, auditorías y responsabilidad contractual |

- Mensaje de cierre del bloque: **prohibir no funciona; la gente la usa igual, a escondidas. Lo que funciona es tener una herramienta aprobada con contrato y decir claramente qué se puede pegar y qué no.**

---

## BLOQUE 2 (15 min) · Lo que entra sin verificar

**Objetivo:** que nadie vuelva a entregar algo generado por IA con su nombre sin haberlo revisado.

### 2.1 · Prueba de alucinación en vivo (5 min)
Formato: abrir una herramienta de IA en pantalla, hacer una pregunta preparada, verificar la respuesta frente a la audiencia.

**Recomendaciones para que salga bien:**
- Preparar 3 preguntas y probarlas el día anterior con la misma herramienta y la misma cuenta. Los modelos cambian y algunas preguntas que fallaban ya no fallan.
- Tener captura de pantalla de respaldo de una respuesta fallida por si en vivo la herramienta acierta. Decir: «hoy acertó; la semana pasada respondió esto».
- Usar la herramienta en su versión gratuita y sin búsqueda web activada: ahí es donde más inventa.

**Tipos de pregunta que funcionan:**
1. **Norma o sentencia muy específica:** «Dame tres sentencias de la Corte Constitucional colombiana sobre teletrabajo y protección de datos, con número, año y magistrado ponente.» Luego buscar una en la relatoría de la Corte. Es muy probable que al menos una no exista o tenga datos cruzados.
2. **Premisa falsa:** «Explícame los cambios que introdujo la Ley 2314 de 2023 al régimen de habeas data en Colombia.» (Verificar antes que ese número no corresponda a una ley sobre ese tema). El modelo puede explicar con detalle una ley que no dice eso.
3. **Dato local verificable:** «¿Quién es el actual superintendente de Industria y Comercio y desde cuándo?» Comparar con la página oficial de la SIC.
4. **Verificar con la misma IA:** después de la respuesta, preguntarle «¿estás seguro? ¿existen esos casos?». Muchas veces confirma con la misma seguridad. Este es el momento clave: **verificar con la misma herramienta no es verificar**.

**Puente:** recordar el caso Mata contra Avianca (Nueva York, 2023): un bufete presentó seis sentencias inventadas por ChatGPT, el abogado le preguntó a la herramienta si eran reales, le dijo que sí, y el juez lo sancionó. La contraparte era una aerolínea colombiana.

### 2.2 · Dónde más duele y cómo detectarlo (2 min)
- Dónde más inventa: citas legales y normas técnicas, cifras y fechas, nombres de personas y empresas, funciones de código que no existen, resúmenes que omiten la cláusula importante.
- Tres señales: responde con total seguridad y sin fuente; el detalle es demasiado específico para algo que nadie le dio; no aparece en una búsqueda fuera de la herramienta.
- Los sesgos entran por la misma puerta: Amazon construyó en 2014-2017 una herramienta para filtrar hojas de vida entrenada con contrataciones pasadas. Aprendió a penalizar las que mencionaban «women's» (clubes, universidades femeninas). La descartaron. En selección, evaluación, crédito o atención al cliente, un sesgo del modelo se convierte en discriminación con el nombre de la empresa.

### 2.3 · Propiedad intelectual de lo que se genera (4 min)
Tres preguntas que la gente no se hace:

**¿De quién es lo que la IA produce?**
- En Colombia (Ley 23 de 1982) y en la mayoría de jurisdicciones, el derecho de autor protege creaciones humanas. Lo generado íntegramente por una IA, sin aporte creativo de una persona, no tiene autor reconocible y su protección es incierta. La Oficina de Derechos de Autor de EE. UU. confirmó esa posición en 2025.
- Consecuencia práctica: un logo, un texto comercial o un código generados 100 % por IA pueden no ser protegibles. Cualquiera podría usarlos. Si hay aporte humano sustancial (edición, selección, dirección creativa documentada), la posición es mucho más fuerte.

**¿Puede estar copiando a alguien?**
- El modelo aprendió de obras ajenas. Puede reproducir fragmentos, estructuras o estilos reconocibles. Hay litigios abiertos (New York Times contra OpenAI, Getty contra Stability AI) que todavía no tienen respuesta definitiva.
- Riesgo real para la empresa: usar en un producto o campaña algo que resulta ser copia, sin saberlo.

**¿Qué dicen los términos del servicio?**
- La mayoría de proveedores asignan la salida al usuario, pero sin garantía de originalidad ni de que no infringe derechos de terceros. La responsabilidad queda en quien la usa.
- Y lo que tú le entregas (tu documento, tu código) puede quedar licenciado al proveedor según el plan. Otra razón para el plan empresarial.

### 2.4 · Las personas deciden, la IA ejecuta (4 min)
Este es el mensaje de fondo del bloque, y conviene decirlo sin rodeos.
- La IA es extraordinaria para las tareas que consumen tiempo: resumir, redactar borradores, traducir, ordenar datos, generar opciones, escribir código repetitivo. Ahí da velocidad real.
- La IA no es responsable de nada. No firma, no responde ante un cliente, un juez ni la SIC. **«Lo dijo la IA» no es defensa.** Air Canada lo aprendió en 2024: su chatbot le dio a un pasajero información equivocada sobre tarifas por duelo, y un tribunal canadiense obligó a la aerolínea a cumplir lo que el chatbot prometió. La empresa alegó que el chatbot era «una entidad separada». El tribunal no lo aceptó.
- Parece muy avanzada porque escribe bien y con seguridad. Pero no sabe cuándo se equivoca, no conoce el contexto de tu empresa salvo lo que le das, y no tiene criterio sobre consecuencias. El caso de Replit de la apertura es exactamente eso: ejecutó, y nadie estaba decidiendo.
- **Modelo mental para la audiencia:** trátala como un practicante brillante y rapidísimo que acaba de llegar. Produce mucho, pero todo pasa por revisión de alguien que entiende el negocio y que va a firmar.
- **Regla de los tres chequeos** antes de usar cualquier salida de IA:
  1. **Fuente:** ¿puedo encontrar esto fuera de la herramienta?
  2. **Contexto:** ¿aplica a Colombia, a nuestro sector, a hoy?
  3. **Consecuencia:** ¿qué pasa si está mal y sale con mi nombre?

---

## BLOQUE 3 (15 min) · La IA como arma contra nosotros

**Objetivo:** que la audiencia reconozca un ataque asistido por IA y sepa qué hacer en los primeros 30 segundos.

**Hilo con la apertura:** «En la apertura vimos a la IA fabricar una pareja y fabricar un empleado. Ahora veamos cómo fabrica a tu jefe, a tu proveedor y a tu propio asistente.»

### 3.1 · Deepfakes de voz y video: fabricar a tu jefe (5 min)
- **Arup (Hong Kong, 2024):** un empleado de finanzas recibió un correo sospechoso del «director financiero» pidiendo una transacción confidencial. Dudó. Entonces lo invitaron a una videollamada con el director financiero y varios colegas. Todos eran deepfakes. Transfirió el equivalente a unos 25 millones de dólares en 15 transacciones.
- **Ferrari (Italia, 2024):** un ejecutivo recibió mensajes de WhatsApp desde un número distinto al del CEO, hablando de una adquisición confidencial y de un acuerdo de confidencialidad que llegaría pronto. Luego una llamada con la voz clonada del CEO, acento incluido. El ejecutivo notó una entonación ligeramente mecánica y le preguntó por el libro que le había recomendado días antes. La llamada se cortó.
- **Puente con el caso 2 de la apertura:** KnowBe4 vio el mismo truco desde el otro lado: no un jefe falso, sino un empleado falso que ya está adentro.
- **Patrón de ataque:** autoridad (viene del jefe) + urgencia (hay que hacerlo ya) + confidencialidad (no se lo digas a nadie) + cambio de canal (número nuevo, plataforma nueva).
- **Defensa que funcionó en Ferrari y falló en Arup:** una pregunta que solo la persona real puede responder, o colgar y llamar al número conocido. Ninguna herramienta técnica lo sustituye.

### 3.2 · Phishing que ya no tiene errores de ortografía (2 min)
- Durante años enseñamos a detectar phishing por la mala redacción. Esa señal desapareció: la IA escribe correos perfectos, en el tono de la empresa, personalizados con lo que encuentra en LinkedIn y en la web corporativa.
- Nuevas señales: la urgencia, el pedido de saltarse un paso, el cambio de cuenta bancaria o de canal, un correo demasiado perfecto de alguien que normalmente escribe con errores.

### 3.3 · Inyección de instrucciones: fabricar a tu asistente (4 min)
- Concepto en una frase: **si tu asistente de IA lee documentos, correos o páginas web por ti, también lee lo que el atacante escribió ahí.** Un correo, un PDF o una página pueden traer instrucciones ocultas (texto blanco sobre blanco, comentarios, metadatos) que el asistente ejecuta como si vinieran de ti.
- **Caso EchoLeak (Microsoft 365 Copilot, junio 2025):** investigadores demostraron que bastaba enviar un correo con instrucciones ocultas para que Copilot, al procesarlo, extrajera información confidencial del buzón del usuario sin que la persona hiciera clic en nada. Microsoft lo corrigió antes de que se explotara en la vida real, pero es la prueba de concepto de la nueva clase de ataque.
- **Por qué importa más cada mes:** los asistentes están pasando de responder preguntas a actuar: leer el correo, agendar, enviar, modificar archivos, ejecutar código. Cuanto más acceso tienen, más daño hace una instrucción inyectada. Replit en la apertura es el ejemplo de lo que pasa cuando un agente actúa sin control, aun sin atacante.
- **Defensa:** limitar lo que el asistente puede hacer sin confirmación humana (sobre todo enviar, borrar, pagar), tratar cualquier documento externo como potencialmente hostil, y no conectar asistentes a sistemas críticos sin revisión de seguridad.

### 3.4 · IA en la sombra: la herramienta que nadie aprobó (2 min)
- Extensiones de navegador que «resumen» todo lo que ves, bots que se unen a las reuniones para transcribir, apps móviles que piden acceso al correo o al calendario, cuentas gratuitas con el correo personal.
- Por qué pasa: son útiles y la opción aprobada es lenta o no existe.
- Riesgo doble: fuga de información (bloque 1) y puerta de entrada (una extensión maliciosa que se hace pasar por asistente de IA).
- Qué hacer: inventario de herramientas en uso, canal rápido para pedir aprobación, alternativa oficial que funcione.

### 3.5 · Qué hacer en los primeros 30 segundos (2 min)
- **Detente** si hay urgencia inusual, cambio de canal o pedido de saltarse un paso.
- **Verifica por otro canal:** cuelga y llama al número que ya tenías; pregunta algo que solo la persona real sabe.
- **No ejecutes** pagos, cambios de cuenta ni envíos de información bajo presión, sin importar quién parezca pedirlo.
- **Reporta** a seguridad aunque haya sido solo un intento. Los intentos son información.

---

## CONCLUSIONES (7 min) · Lo que se llevan

No es un resumen. Son cuatro reglas para pegar en el escritorio.

1. **Nada confidencial ni datos de clientes en herramientas sin contrato.** Si no sabes si la autorización del cliente lo cubre, no lo envíes.
2. **Todo lo que genera la IA se verifica antes de salir con tu nombre.** Fuente, contexto, consecuencia.
3. **Urgente + inusual = confirma por otro canal.** La voz y la cara ya no autentican.
4. **La IA ejecuta, tú decides.** Si dudas, pregunta. Si pasó algo, reporta.

### Reglas de la casa (a completar con la empresa cliente)
- Herramientas aprobadas: [lista]
- Usos permitidos y no permitidos: [resumen de la política]
- A quién acudir ante una duda: [persona o área]
- Cómo reportar un incidente o un intento: [canal]
- Dueño de la política de IA: [área]

### Cierre
- Recordar los tres casos de la apertura y qué regla habría evitado cada uno.
- Preguntas (3 min).

---

## Fuentes principales
- Caso Brad Pitt: TF1 / cobertura de prensa, enero 2025 (Vistazo, RPP, AI Incident Database).
- KnowBe4: blog corporativo «How a North Korean Fake IT Worker Tried to Infiltrate Us», julio 2024; CyberScoop.
- Replit: OECD AI Incidents, eWeek, Heise, julio 2025.
- Ferrari: Bloomberg, julio 2024; The Drive, Motor1.
- Arup: cobertura de CNN, Financial Times y South China Morning Post, febrero 2024.
- Mata v. Avianca: orden del juez P. Kevin Castel, Tribunal del Distrito Sur de Nueva York, junio 2023.
- Air Canada: Moffatt v. Air Canada, Civil Resolution Tribunal de Columbia Británica, febrero 2024.
- Samsung: Bloomberg / The Economist Korea, abril-mayo 2023.
- Amazon: Reuters, octubre 2018.
- EchoLeak: Aim Security, CVE-2025-32711, junio 2025.
- Ley 1581 de 2012, Decreto 1377 de 2013, Circular Externa 005 de 2017 de la SIC, Ley 1273 de 2009, Ley 23 de 1982.
