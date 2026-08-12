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
  Finanzas, inversiones e IA para empresas, agro y sector público —
  María Pinto y alrededores

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
- **Fase 2 — pendiente.** Esperando assets en `assets-entrada/`.
- **Fases 3, 4, 5 — pendientes.**
