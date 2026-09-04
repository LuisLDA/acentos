# 🇪🇨 acento-ecuatoriano

Una **Agent Skill** que hace que tu agente de código hable como dev quiteño: cálido,
directo, con el gerundio andino, los diminutivos y el "no más" atenuador — **sin perder
ni un gramo de precisión técnica**.

> A ver mija, ya le encontré. El problema está en `src/utils/post-media.ts:42`: esa URL
> viene firmada y ya se venció, por eso te sale el placeholder gris. Ponte pilas con eso
> porque en un listado de 30 días **la mayoría** está muerta, no es un caso raro.

## Instalación

```bash
npx skills add LuisLDA/acento-ecuatoriano
```

Funciona con Claude Code, Cursor, Codex, Copilot y demás agentes que soporten
[Agent Skills](https://skills.sh).

## Uso

Invócala por su nombre:

```
/acento-ecuatoriano
```

O simplemente pídelo en lenguaje natural: *"háblame en ecuatoriano"*, *"modo quiteño"*,
*"respóndeme en criollo"*.

Una vez activa, **el registro se mantiene para el resto de la sesión**. Para salir, di
*"habla normal"* o *"modo neutro"*.

## Qué la hace distinta

El error clásico de una skill de acento es espolvorear tres palabras raras sobre español
neutro — eso suena a turista. Esta skill pone el peso en la **sintaxis**, que es lo que de
verdad hace ecuatoriano a un texto:

- **Gerundio andino** — "Ya te doy revisando el archivo", "Dame viendo si eso compila"
- **"No más" atenuador** — "Dale no más, eso no rompe nada"
- **"Pues" enclítico** — "Ya pues, eso era"
- **"Le" pleonástico** — "Ya le arreglé al componente"
- **Diminutivos de ritmo** — "un ratito", "ahicito", "un toquecito"

La jerga (`mija`, `ponte pilas`, `chévere`, `bacán`, `de una`, `chuta`, `ñaño`, `full`,
`de ley`, `cachar`, `camellar`, `chulla`, `yapa`) es el adorno, no la estructura.

## Los límites, que son la parte importante

Esta skill es deliberadamente estricta en dos frentes:

**1. El acento no llega a lo que se versiona.** Vive en la prosa que el agente te escribe
a ti, y en ningún otro lado. Código, comentarios, mensajes de commit, docs, copy de
producto (toasts, labels, prompts) y contenido para terceros conservan las reglas de tu
proyecto. Un *"ponte pilas mija"* en un toast se va a producción y lo ve un cliente en
México.

**2. La precisión gana siempre.** Los diagnósticos, las advertencias y los datos técnicos
—rutas, comandos, mensajes de error, snippets— van literales. El registro cálido nunca
suaviza una mala noticia: *"Ponte pilas mija, esto borra la tabla en producción"* es más
fuerte que la versión neutra, no más débil.

Además hay una lista explícita de **términos vetados**: `longo`, `cholo`, `indio`, `mono`
o `serrano` como insulto no son color local — son racismo y regionalismo con historia.
Tampoco vulgaridad ni chistes de estereotipo: la gracia es hablar así, no burlarse de
quien habla así.

## Estructura

```
acento-ecuatoriano/
├── SKILL.md      # la skill
├── README.md
└── LICENSE
```

## Licencia

MIT — ver [LICENSE](LICENSE).
