# PROYECTO: Sitio de captación multi-segmento (GitHub Pages)
# Versión definitiva. Reemplaza cualquier versión anterior.

## CÓMO TRABAJAR CONMIGO
- No soy programador (base: Python básico). Define cada herramienta o
  concepto la primera vez que lo uses, en una línea. Justifica cada
  decisión técnica no trivial.
- Trabaja por FASES. Al terminar cada fase: muestra qué hiciste, haz
  commit, y espera mi OK antes de seguir.
- Nunca inventes contenido: usa el copy que te doy tal cual. Donde
  falte contenido, deja un placeholder visible [PENDIENTE].
- Nunca borres ni modifiques los archivos que yo entregue en
  assets-entrada/.
- Guarda este documento completo como CLAUDE.md en la raíz del repo
  (es la memoria del proyecto para sesiones futuras).

## ENTORNO
macOS Intel, zsh, git y VS Code instalados. Cuenta de GitHub creada,
sin repos. Es posible que falte `gh` (GitHub CLI): verifícalo en
Fase 0 e instálalo/autentícalo si falta.

## OBJETIVO Y MODELO
Sitio estático de captación con UNA URL POR SEGMENTO de audiencia.
Modelo de distribución: yo comparto por WhatsApp/redes una
tarjeta-imagen que apunta a la URL de su segmento (par tarjeta→URL).
Las audiencias nunca se cruzan: ninguna página enlaza a otra.
Narrativa de cada landing (StoryBrand): el cliente es el héroe con un
problema; yo soy el guía con un plan y autoridad demostrada.

Segmentos definidos (slugs propuestos, ajustables):
  /mariapinto/   → asesoría local agro + municipal  ← SE CONSTRUYE HOY
  /clases/       → docencia universitaria           ← futuro
  /pymes/        → consultoría estratégica pymes    ← futuro
  /emprender/    → emprendimientos IDE/AIDE         ← futuro
Raíz (/): tarjeta neutra mínima — nombre, "Economista (PUC) ·
Asesoría estratégica y financiera", botón WhatsApp, link LinkedIn.
Sin menú, sin enlaces a segmentos.

## RESTRICCIONES TÉCNICAS (no negociables)
1. HTML + CSS puros. Sin frameworks, sin npm, sin build, sin
   generadores. Razón: nada que se rompa ni que dependa de versiones;
   GitHub Pages lo sirve tal cual; yo puedo leer cada archivo.
2. El sitio funciona con JavaScript desactivado. JS solo si es
   imprescindible y progresivo.
3. Mobile-first real: se abre desde WhatsApp, en celulares de gama
   media, con datos móviles rurales. Presupuesto: cada página < 300 KB
   en total (sin contar PDFs).
4. Un solo CSS compartido: /assets/css/base.css con variables
   (design tokens) de color y tipografía. Todos los segmentos heredan
   identidad; un cambio se propaga solo.
5. HTML semántico, contraste WCAG AA, alt en toda imagen.
6. Cada página de segmento lleva <meta name="robots"
   content="noindex"> — los segmentos se distribuyen por link directo
   y no deben aparecer en Google. La raíz sí es indexable.

## ESTRUCTURA
/index.html                  ← tarjeta neutra
/mariapinto/index.html       ← segmento inicial
/assets/css/base.css
/assets/img/                 ← imágenes optimizadas por ti
/assets/docs/                ← PDFs
/assets-entrada/             ← aquí YO deposito los archivos crudos
/404.html                    ← simple, con link a la raíz
/NUEVO-SEGMENTO.md           ← se escribe en Fase 5
/CLAUDE.md                   ← este documento

## PLANTILLA DE SEGMENTO (mismo orden siempre)
1. Nombre + propuesta de valor calibrada al segmento
2. "Qué resuelvo" — bullets calibrados
3. "Resultados" — 3 cifras con contexto
4. Trayectoria breve
5. CTA: botón WhatsApp grande + teléfono y correo en texto plano
   (el visor de Android no siempre activa enlaces) + link LinkedIn
6. Botón "Descargar PDF (una página)"
Head por segmento: <title>, meta description, y Open Graph completo
(og:title, og:description, og:image con URL ABSOLUTA, og:url).

## CTA — DECISIÓN DE DISEÑO (aplica a /mariapinto/)
El CTA es UN botón de WhatsApp, no un formulario ni un calendario.
Razón: el visitante ya viene de WhatsApp; cada paso o campo extra
pierde contactos, y la calificación del lead ocurre en la conversación,
no en un embudo. Microcopy del botón:
  "Escríbeme por WhatsApp — respondo el mismo día"
Nada de iframes de terceros (Typeform, Calendly): violarían las
restricciones 1, 2 y 3.

## MEDICIÓN SIN HERRAMIENTAS
El botón de WhatsApp de cada segmento lleva texto prellenado distinto:
  https://wa.me/56967789324?text=Hola%20Fernando%2C%20vi%20tu%20p%C3%A1gina%20(María%20Pinto)
Así el primer mensaje de cada contacto me dice de qué segmento vino.
Analítica formal (GoatCounter u otra): fase futura, no ahora.

## HERRAMIENTA DE RECEPCIÓN (fuera de este repo — nota de contexto)
Los botones wa.me de este sitio caen en WhatsApp Business (app en mi
teléfono, no código). Ahí vive el manejo de leads: respuestas rápidas,
etiquetas por segmento, estados. El link con texto prellenado por
segmento es el único empalme entre el sitio y esa app. Claude Code no
configura WhatsApp Business; se administra a mano.

## CONTENIDO DEL SEGMENTO /mariapinto/ (usar tal cual —
## copy definitivo, sin marcas pendientes)

  FERNANDO QUEVEDO
  Finanzas, inversiones e IA para empresas y sector público — con foco
  en el agro de María Pinto

  QUÉ RESUELVO
  • ¿Conviene esta inversión? — Evaluación con números: riego,
    maquinaria, packing.
  • Finanzas para decidir — presupuestos, proyecciones e indicadores
    de gestión.
  • Venta al Estado — Mercado Público y licitaciones, de la
    postulación a la adjudicación.
  • IA con criterio — diagnóstico y hoja de ruta: en qué conviene
    invertir en IA, en qué no, y por dónde partir sin quemar plata.
  • Capacitación en finanzas, emprendimiento e IA aplicada, para
    dueños, equipos y organizaciones.

  RESULTADOS
  • $790 millones (CLP) en ventas acumuladas — empresa de tecnología
    educativa que fundé y dirigí durante 7 años, con un equipo de
    37 personas (2016–2023).
  • De 50 a 200 colegios en 6 meses — piloto nacional con el
    Ministerio de Educación; 450.000 ejercicios entregados (2019).
  • Cierre ordenado tras la crisis social y la pandemia — 100% de
    finiquitos e indemnizaciones pagados.

  TRAYECTORIA
  • 2026–hoy · Director y accionista, Terco SpA — constructora de
    pinturas y terminaciones, 170 trabajadores; diseñé su expansión a
    vivienda con subsidio (DS 19 / DS 49).
  • 2024–2025 · Mentor del programa NAVES, IAE Business School
    (Argentina).
  • 2016–2023 · Fundador y Gerente General, Adaptativamente
    (tecnología educativa para colegios).
  • Antes · Docencia en economía: U. Adolfo Ibáñez y PUC.

  FORMACIÓN
  • Magíster en Economía (Políticas Públicas) e Ingeniería Comercial,
    U. Católica de Chile.
  • Posgrados en Economía en Europa: Máster de investigación, U. de
    Tilburg (Países Bajos); investigación doctoral, U. de Viena
    (Austria).
  • MBA Ejecutivo, IAE Business School (Argentina, 2025).
  • Certificado en Estrategia de IA, Kellogg School of Management
    (2025).

  CIERRE
  Primera conversación sin costo.
  WhatsApp +56 9 6778 9324 · fquevedoc@proton.me · LinkedIn

## FASES

FASE 0 — Entorno. Verifica git y gh; instala y autentica gh si falta
(explícame qué hace cada comando antes de correrlo).

FASE 1 — Esqueleto. Repo local con la estructura completa, base.css
con tokens, raíz neutra, /mariapinto/ con el copy de arriba y
placeholders de imagen, 404. Commit.

FASE 2 — Assets (te los entregaré DE A UNO en assets-entrada/;
al integrar cada uno, avísame y pídeme el siguiente):
  a) Tarjeta-gancho (imagen 1080×1350): conéctala al head de
     /mariapinto/. DEROGADO en cuanto a la og-image: su diseño, peso y
     medidas los fija la SPEC CANÓNICA TARJETA v6, más arriba. Esta
     línea se conserva solo como registro del plan original.
  b) CV one-pager PDF (80×160 mm): a /assets/docs/ con el nombre
     "Fernando Quevedo - Asesorias.pdf", conectado al botón de
     descarga. Verifica que pese < 1 MB.
  c) CV móvil exportado de Claude Design: NO incrustes su HTML.
     Úsalo solo como referencia visual (colores, tipografías,
     jerarquía) y replica ese look en el HTML semántico del sitio.
     Razón: los exports de herramientas de diseño traen
     posicionamiento absoluto y peso que rompen la responsividad.
     Extrae sus colores y tipografías a los tokens de base.css.

FASE 3 — Publicación. Crea el repo remoto con el nombre EXACTO
<mi-usuario>.github.io (pídeme mi usuario), público, push, activa
GitHub Pages (rama main, raíz). Dame la URL para probarla en mi
celular ANTES de seguir.

FASE 4 — Dominio propio [SOLO cuando yo confirme la compra en NIC
Chile]. Archivo CNAME con el dominio, lista exacta de registros DNS
que debo cargar en el panel de NIC (los 4 registros A de GitHub
Pages + CNAME www), actualiza todas las og:url y og:image absolutas
al dominio nuevo, y activa "Enforce HTTPS" cuando propague.

FASE 5 — Escalamiento. Escribe NUEVO-SEGMENTO.md: procedimiento
paso a paso (copiar carpeta plantilla, editar los textos calibrados,
cambiar title/description/og, cambiar el texto prellenado del
wa.me, verificar noindex) con los 3 segmentos futuros ya listados.
Crear un segmento nuevo debe tomar minutos.

## CRITERIOS DE ACEPTACIÓN
1. Legible y completo en un celular de gama media con 4G.
2. Lighthouse móvil ≥ 90 en Performance y Accesibilidad (Lighthouse:
   auditor integrado en Chrome; explícame cómo correrlo una vez).
3. La vista previa del link en WhatsApp muestra título, descripción
   e imagen correctos. El procedimiento para re-probar tras un cambio
   —calentar el CDN primero, y por qué un ?v=N gastado queda quemado—
   está en la SPEC CANÓNICA TARJETA v6.
4. Todo funciona con JavaScript desactivado.
5. Ninguna página enlaza a otro segmento.
6. Crear un segmento nuevo = copiar carpeta + editar textos, sin
   tocar CSS.

## SPEC CANÓNICA TARJETA v6

Esta especificación manda sobre `/assets/img/og-mariapinto.jpg`, sobre
el `og:title` y sobre las metas de descripción de `/mariapinto/`.
REEMPLAZA ÍNTEGRAMENTE cualquier spec previa de la tarjeta: la v4 (que
vivía aquí) y la instrucción de volver a 2 niveles, que queda ANULADA.
No hubo una v5 escrita en este documento. Todo cambio futuro reemplaza
esta spec completa — nunca la parcha.

MOTIVO DEL CAMBIO, para que no se deshaga por error:
  1. La jerarquía entre L2 y L3 se resuelve por TONO, no por tamaño ni
     por peso. Las dos líneas comparten altura de mayúscula y peso; lo
     único que las separa es que L3 va en gris.
  2. La duplicación real nunca estuvo entre la imagen y la descripción,
     sino entre la imagen y el `og:title`. Por eso el título ya no
     repite "Finanzas, inversiones e IA · María Pinto" —que es
     exactamente lo que dice la imagen— y pasa a decir la promesa.

### LA IMAGEN (/assets/img/og-mariapinto.jpg)
Lienzo 1200×630 px, JPEG calidad 80-85, peso ≤ 300 KB, baseline nunca
progresivo (WhatsApp no dibuja los progresivos). Fondo `#051C2C` y
barra de acento `#2251FF`, tokens de `/assets/css/base.css`; si los
tokens cambian, mandan los tokens. Sin versalitas, sin letter-spacing,
sin degradados, sin sombras.

TRES niveles de texto, en este orden, una línea cada uno:
  L1: Fernando Quevedo — caja mixta, bold 700, BLANCO, cap 81 px.
  L2: Finanzas, inversiones e IA — regular 400, BLANCO, cap 60-62 px.
  L3: María Pinto — regular 400, GRIS `#A8B6C2`, cap 60-62 px.
Márgenes: laterales ≥ 80 px en las tres líneas; verticales ≥ 63 px; el
aire sobrante se distribuye alrededor del bloque.

EL GRIS DE L3 — `#A8B6C2`, contraste 8,38:1 sobre `#051C2C` por
fórmula y 8,64:1 medido sobre el JPEG entregado. Piso: 7:1.
No manda ningún token de `base.css` porque ninguno sirve sobre fondo
oscuro: `--c-ink-soft` (#5A6470) está calibrado contra blanco y aquí
cae a 2,89:1, y `--c-line` (#D5DAE0) pasa el número (12,35:1) pero es
color de líneas divisorias, no de texto, y a esa altura casi no
desenfatiza. Este gris existe solo sobre fondo oscuro. Ojo: el proyecto
ya tenía otro gris para fondo oscuro, `#9AA6B2` (7,01:1), usado en la
tarjeta 1080×1350; se conservó ahí y NO se unificó. Si algún día se
unifican, gana `#A8B6C2` por margen de contraste.

POR QUÉ L1 MIDE 81 px. "Fernando Quevedo" en caja mixta bold ocupa
8,346 em; a 92 px de altura de mayúscula mediría 1178 px de ancho
contra los 1040 disponibles con márgenes de 80. El máximo real es
81 px en bold. Con L1 a 81 y L2 en su piso de 60 el ratio de tamaño
queda en 1,350. Se acepta: la jerarquía la construyen tamaño, peso y
tono juntos, y la única variante que subía el ratio dejaba nombre y
lema en el mismo peso, con el nombre menos dominante.

### REGLAS PERMANENTES
JERARQUÍA. Se construye por tamaño, peso Y tono. El tono solo
desenfatiza mientras el contraste medido se mantenga ≥ 7:1; nunca por
debajo.

RESOLUCIÓN DE CONFLICTOS.
1. Si un texto no cabe: primero se corta contenido.
2. Si el contenido es atómico (un nombre propio): se reduce tamaño,
   nunca bajo 60 px de altura de mayúscula.
3. Jamás se compensa rompiendo márgenes mínimos ni la jerarquía.
4. Si (1)-(3) no pueden cumplirse a la vez: DETENTE y reporta variantes
   medidas al píxel. No inventes contenido.
Aplicación conocida: L2 entra al ras — mide 954 px de los 1040
disponibles y su altura de mayúscula máxima es 64,5 px. No hay espacio
para alargarla. Nunca se comprime el tracking ni se achica bajo el piso.

### CÓMO SE MIDE
ALTURA DE MAYÚSCULA. No se estima: se mide en píxeles sobre el JPEG
entregado, con un glifo de referencia plano arriba y abajo (`F`, `E`,
`M`). No sirven la `Q` (su cola desciende bajo la línea base) ni la `i`
(su punto sube sobre la altura de mayúscula). El umbral para separar
glifo de fondo es el punto medio de luminancia entre el fondo y el
color declarado de esa línea; con un umbral fijo, una línea gris y una
blanca no son comparables. Para Source Sans 3, altura de mayúscula =
0,6518 × font-size en bold y 0,6563 en regular.
CONTRASTE. Fórmula WCAG sobre el núcleo del trazo, no sobre los bordes
suavizados: se ordenan los píxeles de la línea por luminancia y se toma
el percentil 85.

### TEXTOS
`og:title` — no repite NADA de lo que ya dice la imagen, ni siquiera el
nombre: la imagen ya lo grita en la línea más grande, y el título es el
único renglón que WhatsApp dibuja en negrita. Se gasta entero en la
promesa:
  "Antes de invertir, ponle números"
`meta description` y `og:description`, idénticas byte a byte
(96 caracteres):
  "Riego, maquinaria, packing o el proyecto que tengas entre manos.
  Primera conversación sin costo."
`og:image:alt` (describe la imagen, por eso sí conserva la fórmula
larga, para lectores de pantalla):
  "Fernando Quevedo — Finanzas, inversiones e IA · María Pinto"
NOTA: el `<title>` del HTML NO se tocó y sigue diciendo "Fernando
Quevedo — Finanzas, inversiones e IA · María Pinto". Es deliberado
—esta spec solo levantó el bloqueo sobre `og:title`— pero queda
divergente: el título de la pestaña y el de la vista previa ya no
coinciden. Decidir en una próxima pasada.

### PUBLICACIÓN — CALENTAR EL CDN ANTES DE PROBAR
WhatsApp cachea la vista previa POR URL PEGADA (no por `og:url`: está
comprobado en terreno, `?v=2` y `?v=3` se comportaron distinto). Y si
raspa la imagen cuando el objeto todavía está frío en el CDN de GitHub
(`x-cache: MISS`) y la descarga no alcanza a completarse, guarda el
fracaso para esa URL durante días, aunque el archivo esté perfecto.
Orden correcto tras cada cambio de og-image:
  1. Desplegar y esperar a que la URL sirva el archivo nuevo.
  2. Calentar: pedir la imagen dos o tres veces hasta ver `x-cache: HIT`.
  3. Recién entonces probar con un `?v=N` que nunca se haya usado.
OJO CON LA VENTANA: GitHub Pages sirve con `cache-control: max-age=600`,
así que el borde del CDN se enfría a los 10 MINUTOS sin tráfico y vuelve
a `x-cache: MISS`. El calentamiento no se hace "después de desplegar":
se hace INMEDIATAMENTE ANTES de la prueba. Si pasó más de un rato entre
una cosa y la otra, se calienta de nuevo. Comprobado: tras el despliegue
la imagen estaba caliente, y 10 minutos después ya marcaba MISS.
Una URL que ya falló queda quemada. Para recuperarla: Sharing Debugger
de Meta (`developers.facebook.com/tools/debug/`, botón "Scrape Again"),
o esperar a que expire el caché.

---

## ESTADO DEL PROYECTO (bitácora — se actualiza al cerrar cada fase)

- **Fase 0 — LISTA.** Entorno verificado: git 2.23.0, gh 2.96.0
  autenticado como `fernando4to`, Homebrew 6.0.12. Nada por instalar.
- **Fase 1 — LISTA.** Esqueleto completo, `base.css` con tokens
  provisionales, raíz neutra, `/mariapinto/` con el copy definitivo,
  404. Pendientes visibles: URL de LinkedIn, imagen (2a), PDF (2b).
- **Fase 2c — LISTA (adelantada).** Importado el sistema visual del
  proyecto de Claude Design "# CV de una página"
  (`bfb43113-8198-41fb-9aa1-2b2ad1a5f38c`), archivo
  `Fernando Quevedo - Asesorias A4 copy.dc.html`, vía el MCP
  claude_design. Confirmado que su HTML NO es incrustable: depende de
  `support.js` (70,6 KB de runtime React generado) y de `doc-page.js`
  (shell de documento paginado con `@page` y unidades en mm). Se
  extrajo a tokens:
    - Colores: `#051C2C` azul profundo · `#2251FF` azul vivo ·
      `#1A1D21` tinta · `#5A6470` gris · `#FFFFFF` fondo.
    - Tipografía: Source Sans 3 (variable, subconjunto latino,
      28 KB), auto-hospedada en `/assets/fonts/`.
    - Jerarquía: barra azul sobre el nombre, nombre en versalitas,
      títulos de sección grandes con línea fina bajo, viñeta cuadrada
      azul dibujada en CSS.
  Resuelto el [PENDIENTE] de LinkedIn:
  `https://www.linkedin.com/in/fernando-quevedo-callejas/`.
  El QR del CV se omitió a propósito (se genera por JS y no aporta a
  quien ya está en el celular).
- **Fase 2b — LISTA.** El PDF de descarga es
  `CV v2 Orientado al publico.dc.html` del mismo proyecto de Claude
  Design (decisión de Fernando). Ese archivo es 100% estático (no tiene
  `data-dc-script` ni variables `{{ }}`), así que se reprodujo en HTML
  plano imprimible en `_fuente-pdf/cv-asesorias.html` y se imprimió con
  Chrome headless a `assets/docs/Fernando Quevedo - Asesorias.pdf`
  (1 página carta, 79,8 KB, límite 1 MB). El comando para regenerarlo
  está comentado dentro de `_fuente-pdf/cv-asesorias.html`.
  La carpeta `_fuente-pdf/` empieza con guion bajo a propósito: GitHub
  Pages ignora esas carpetas, así que la fuente queda versionada pero
  no publicada. (Por eso el repo NO debe llevar `.nojekyll`.)
  Ojo: este CV es tamaño CARTA, no 80×160 mm como decía la Fase 2b
  original; y usa Helvetica con títulos de sección chicos y espaciados,
  mientras el sitio usa Source Sans 3 con títulos grandes (tomados del
  CV A4). La paleta sí es idéntica en los tres.
- **Fase 2a — LISTA.** La tarjeta-gancho es `Tarjeta gancho.dc.html`
  del proyecto de Claude Design. También es estática (su bloque
  `data-dc-script` viene vacío), así que se reprodujo en
  `_fuente-img/tarjeta-gancho.html` y se renderizó con Chrome headless.
  Productos, ambos JPEG calidad 90:
    - `assets/img/tarjeta-mariapinto-1080x1350.jpg` (168,4 KB) — la
      imagen que Fernando comparte por WhatsApp/redes.
    - `assets/img/og-mariapinto.jpg` — vista previa del link, conectada
      al `og:image` de `/mariapinto/` junto con
      `og:image:width/height/alt`. Su diseño ya NO es el de esta fase:
      lo rige la SPEC CANÓNICA TARJETA v6, más arriba.
  El og:image nunca fue un recorte literal de la tarjeta: la tarjeta es
  vertical (1080×1350) y el og:image es horizontal (1200×630), así que
  una franja del centro habría dejado fuera el nombre o el número. Cada
  uno tiene su propio archivo fuente en `_fuente-img/`, con el comando
  de regeneración comentado adentro.
  Color nuevo que aporta la tarjeta y que solo se usa sobre fondo
  oscuro: `#9AA6B2` (gris azulado, 7,0:1 sobre `#051C2C`).
  Se quitó el placeholder de imagen del cuerpo de `/mariapinto/`: el
  visitante acaba de ver y tocar la tarjeta en WhatsApp, repetirla
  gastaría la primera pantalla del celular. Si se quiere de vuelta, es
  un `<img>` y ya existe el JPG.
- **YA NO QUEDAN [PENDIENTE] en el sitio.** Fase 2 completa.
- **Contenido de `/mariapinto/` alineado** con
  `Fernando Quevedo - Asesorias.dc.html` (el CV móvil de 80×160 mm, 4
  páginas, del mismo proyecto de Claude Design). "Qué resuelvo" y
  "Resultados" ya eran idénticos. Se corrigió:
    - Terco: se agregó "; diseñé su expansión a vivienda con subsidio
      (DS 19 / DS 49)".
    - 2024–2025: pasó de "MBA Ejecutivo, IAE Business School · Mentor
      NAVES-IAE" a "Mentor del programa NAVES, IAE Business School
      (Argentina)" — el MBA se movió a Formación.
    - "(edtech)" → "(edtech escolar)".
    - Se agregó el ítem "Antes · Docencia en economía: U. Adolfo Ibáñez
      y PUC."
    - Se agregó la sección FORMACIÓN completa (4 ítems), que absorbe el
      Magíster y el certificado Kellogg que antes colgaban de
      Trayectoria, y suma el MBA y los posgrados en Tilburg y Viena.
  Como efecto de esto, la PLANTILLA DE SEGMENTO de más arriba ahora
  tiene 7 bloques, no 6: Formación entra entre Trayectoria y el CTA.
- **LEMA — RESUELTO.** Fernando decidió consistencia total con el de
  los CV: "Finanzas, inversiones e IA para empresas y sector público —
  con foco en el agro de María Pinto". El lema anterior
  ("…para empresas, agro y sector público — María Pinto y alrededores")
  queda descartado y ya no debe usarse en ninguna parte. Aplicado en
  los 3 lugares de `/mariapinto/`: el `<p class="lema">`, la
  `meta description` y el `og:description`. La copy definitiva de más
  arriba en este documento ya está actualizada.
  Única aparición sobreviviente de "María Pinto y alrededores": el pie
  del PDF ("Disponible para asesorías en María Pinto y alrededores"),
  que es otra frase y vive en el CV que Fernando decidió no modificar.
- **DECISIÓN PENDIENTE — contenido extra del CV A4.** El CV trae
  material que la copy definitiva de `/mariapinto/` no tiene. NO se
  agregó a la landing sin autorización. Es: sección FORMACIÓN aparte;
  "diseñé su expansión a vivienda con subsidio (DS 19 / DS 49)" en
  Terco; "(Argentina)" en IAE; "edtech escolar"; "Magíster en Economía
  (Políticas Públicas)"; "Kellogg School of Management"; y un ítem
  nuevo "Antes · Docencia en economía: U. Adolfo Ibáñez y PUC". El CV
  además usa otro lema: "...para empresas y sector público — con foco
  en el agro de María Pinto".
- **Fase 3 — LISTA.** Repo público `fernando4to/fernando4to.github.io`
  creado, `main` empujada, GitHub Pages activo (rama `main`, raíz),
  HTTPS forzado y `http://` redirige con 301.
  URLs en vivo:
    - Raíz (indexable):  https://fernando4to.github.io/
    - Segmento:          https://fernando4to.github.io/mariapinto/
  Verificado en vivo: los dos HTML, el CSS, la fuente, el og:image y el
  PDF responden 200 con el tipo correcto; una ruta inventada cae en
  nuestro 404.html; `noindex` está solo en el segmento y no en la raíz.
  Confirmado que `_fuente-pdf/` y `_fuente-img/` devuelven 404: la
  exclusión por guion bajo de Jekyll funciona. NO agregar `.nojekyll`.
- **NOTA DE PRIVACIDAD.** El repo es público porque GitHub Pages gratis
  solo publica desde repos públicos. Consecuencia: este CLAUDE.md es
  legible por cualquiera en
  github.com/fernando4to/fernando4to.github.io, y al crear los
  segmentos futuros sus carpetas quedarán a la vista en el repo aunque
  las páginas lleven `noindex`. Es decir, el `noindex` esconde los
  segmentos de Google, no del repositorio. Si eso molesta, las salidas
  son: sacar CLAUDE.md del repo (queda solo local), o mover el sitio a
  un repo distinto del que guarda la documentación.
- **CONVENCIÓN DE TÉRMINOS — "edtech".** Decisión de Fernando: en
  `/mariapinto/` NO se usa el anglicismo. Va su propia redacción del
  CV v2: "empresa de tecnología educativa" y "Adaptativamente
  (tecnología educativa para colegios)". Razón: la audiencia es agro y
  municipal, "edtech" es jerga de otro sector, y así la landing queda
  alineada con el PDF que el visitante descarga (que ya decía
  "tecnología educativa" y "plataforma de aprendizaje para colegios").
  Donde SÍ se use la palabra en segmentos futuros —`/clases/` y
  `/emprender/`, cuyas audiencias la manejan— se escribe **"edtech"**:
  minúscula, una sola palabra, sin guion y sin cursiva. Nunca
  "EdTech" ni "ed-tech": en estas frases es sustantivo común en
  español, y el camel case lo haría leer como nombre propio (el nombre
  de la empresa es Adaptativamente). El término es una palanca de
  calibración por segmento, no una regla global.
- **CRITERIO DE ACEPTACIÓN 2 — CUMPLIDO.** Fernando corrió Lighthouse
  móvil sobre el sitio en vivo: **Performance 99, Accesibilidad 100**
  (la meta era ≥ 90 en ambos). Medido con la tipografía
  auto-hospedada de 28 KB y sin JavaScript.
- **TARJETA GANCHO — v6 EN PRODUCCIÓN.** La og-image y las metas de
  descripción se rigen por la **SPEC CANÓNICA TARJETA v6**, más arriba
  en este documento. Ahí están los tres niveles de texto, la regla de
  resolución de conflictos, cómo se mide la altura de mayúscula y el
  procedimiento de publicación. Las specs anteriores (5 niveles y
  2 niveles) fueron eliminadas: no se parchan, se reemplazan.
  Origen del rediseño: en prueba real la vista previa mide ~6 cm en el
  celular, y de los 5 niveles de texto que tenía la primera versión
  solo sobrevivían 2. Por eso el trabajo se reparte por capa — la
  imagen dice quién, qué y dónde; el `og:title` y la `og:description`
  dicen el resto en texto del sistema, que WhatsApp siempre dibuja
  nítido y escalable.
- **Fases 4 y 5 — pendientes.**
