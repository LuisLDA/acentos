# 🇪🇨 acentos

**Agent Skills** que le dan a tu agente de código un acento ecuatoriano de verdad — sin
perder ni un gramo de precisión técnica.

Ecuador no tiene un acento, tiene varios, y son **muy** distintos entre sí. Por eso cada
uno es una skill aparte: mezclarlos suena a nadie.

| Skill | Región | Suena así |
|---|---|---|
| [`acento-ecuador-sierra`](skills/acento-ecuador-sierra) | Quito / Sierra | *"A ver mija, ya te doy revisando. Dale no más, eso no rompe nada."* |
| [`acento-ecuador-costa`](skills/acento-ecuador-costa) | Guayaquil / Costa | *"Oe bro, ya lo veo. De una, eso no rompe nada."* |

## Instalación

```bash
# las dos
npx skills add LuisLDA/acentos

# solo una
npx skills add LuisLDA/acentos --skill acento-ecuador-costa
```

El CLI las instala en `.agents/skills/` y las enlaza a los agentes que tengas: Claude Code,
Codex, Cursor, Cline, Amp, Copilot y 70+ más. Agrega `-g` para instalar a nivel de usuario
en vez de por proyecto, o `-l` para ver el contenido sin instalar nada.

## Uso

Invócalas por su nombre:

```
/acento-ecuador-sierra
/acento-ecuador-costa
```

O pídelo en lenguaje natural: *"háblame en quiteño"*, *"modo costeño"*, *"acento de la
costa"*, *"habla como guayaco"*.

Una vez activa, **el registro se mantiene para el resto de la sesión**. Para salir, di
*"habla normal"* o *"modo neutro"*.

## Qué las hace distintas

El error clásico de una skill de acento es espolvorear tres palabras raras sobre español
neutro — eso suena a turista. Acá el peso está en la **sintaxis**, que es lo que de verdad
marca la región.

**Sierra — atenúa.** Gerundio andino (*"ya te doy revisando"*), `no más` ablandador
(*"dale no más"*), `pues` enclítico, `le` pleonástico (*"ya le arreglé al componente"*),
diminutivos de ritmo (*"ahicito"*, *"un ratito"*) y léxico kichwa (*achachay*, *guagua*).

**Costa — afirma.** Frases cortas y frontales, vocativos constantes (*bro*, *loco*,
*ñaño*), interjección de arranque (*¡oe!*, *¡ve!*), elisión lexicalizada (*pa'*, *na' que
ver*) y su propio léxico (*qué nota*, *fresco*, *ni de vainas*, *chendo*, *al pelo*).

Cada skill lleva una sección explícita de **qué marcadores de la otra región tiene
prohibidos**. Sin eso, las dos derivan al mismo español genérico.

## Los límites, que son la parte importante

Las dos skills son deliberadamente estrictas en tres frentes:

**1. El acento no llega a lo que se versiona.** Vive en la prosa que el agente te escribe a
ti, y en ningún otro lado. Código, comentarios, mensajes de commit, docs, copy de producto
(toasts, labels, prompts) y contenido para terceros conservan las reglas de tu proyecto. Un
*"ponte pilas mija"* en un toast se va a producción y lo ve un cliente en México.

**2. La precisión gana siempre.** Diagnósticos, advertencias y datos técnicos —rutas,
comandos, mensajes de error, snippets— van literales. El registro cálido nunca suaviza una
mala noticia: *"Oe, pilas: esto borra la tabla en producción"* es más fuerte que la versión
neutra, no más débil.

**3. Nada de burla ni de racismo.** Hay una lista explícita de términos vetados: `longo`,
`cholo`, `indio`, `montubio` como insulto, y el par regional `mono` / `serrano`. No son
color local, son racismo y regionalismo con historia. Tampoco vulgaridad, ni chistes de
estereotipo — y la skill de la costa prohíbe transcribir la /s/ aspirada (*"loh maneh"*),
que escrita se lee como caricatura y no como acento.

## Estructura

```
acentos/
├── README.md
├── LICENSE
└── skills/
    ├── acento-ecuador-sierra/SKILL.md
    └── acento-ecuador-costa/SKILL.md
```

## Contribuir

¿Falta un acento (manaba, lojano, esmeraldeño) o hay jerga mal usada? Los PRs son
bienvenidos — sobre todo de hablantes nativos de cada región.

## Licencia

MIT — ver [LICENSE](LICENSE).
