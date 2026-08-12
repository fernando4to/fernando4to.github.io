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
  • $790 millones (CLP) en ventas acumuladas — empresa edtech que
    fundé y dirigí durante 7 años, con un equipo de 37 personas
    (2016–2023).
  • De 50 a 200 colegios en 6 meses — piloto nacional con el
    Ministerio de Educación; 450.000 ejercicios entregados (2019).
  • Cierre ordenado tras la crisis social y la pandemia — 100% de
    finiquitos e indemnizaciones pagados.

  TRAYECTORIA
  • 2026–hoy · Director y accionista, Terco SpA — constructora de
    pinturas y terminaciones, 170 trabajadores.
  • 2024–2025 · MBA Ejecutivo, IAE Business School · Mentor NAVES-IAE.
  • 2016–2023 · Fundador y Gerente General, Adaptativamente (edtech).
  • Magíster en Economía e Ingeniería Comercial, U. Católica ·
    Certificado en Estrategia de IA, Kellogg (2025).

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
  a) Tarjeta-gancho (imagen 1080×1350): genera de ella un recorte
     og-image de 1200×630, JPEG ≤ 300 KB (WhatsApp rechaza og:image
     pesadas), y conéctala al head de /mariapinto/.
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
   e imagen correctos. Ojo: WhatsApp cachea vistas previas — para
   re-probar tras un cambio, agrega ?v=2 al link.
4. Todo funciona con JavaScript desactivado.
5. Ninguna página enlaza a otro segmento.
6. Crear un segmento nuevo = copiar carpeta + editar textos, sin
   tocar CSS.

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
    - `assets/img/og-mariapinto.jpg` (95,9 KB, límite 300 KB) — vista
      previa del link, conectada al `og:image` de `/mariapinto/` junto
      con `og:image:width/height/alt`.
  El og:image NO es un recorte literal de la tarjeta: la tarjeta es
  vertical (1080×1350) y el og:image es horizontal (1200×630), así que
  una franja del centro habría dejado fuera el nombre o el número.
  Son los mismos textos reordenados, en
  `_fuente-img/og-mariapinto.html`. Ambos comandos de regeneración
  están comentados dentro de cada archivo fuente.
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
- **Fases 3, 4, 5 — pendientes.**
