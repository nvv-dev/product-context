# product-context

> Los datos del negocio en un solo archivo, para no repetirlos en cada sesión.

**Contexto del producto** · Skill para agentes de código de la comunidad [nvvdev](https://github.com/nvv-dev). Funciona en Claude Code como plugin o como skill suelta, y en cualquier agente compatible con el formato abierto [`SKILL.md`](https://agentskills.io).

*English summary at the end.*

## Qué hace

Crea y mantiene `.agents/product-context.md`: qué es el producto, cliente ideal, problema y alternativas, posicionamiento, objeciones, pruebas, lenguaje del cliente y aprendizajes, con versión y registro de cambios. Si el archivo ya existe, lo resume en cinco líneas y actualiza solo lo que pediste. Lo que nadie ha confirmado queda como pregunta abierta, nunca como suposición.

## Objetivo

Que el copy, el contenido, el diseño y el SEO partan de los mismos hechos aprobados y no se contradigan entre páginas.

## Cuándo usarla

- Al empezar trabajo de marketing, copy, diseño o SEO para un producto
- Cuando aparece un dato nuevo: una objeción, una prueba, un resultado de una campaña

## Cuándo no

- Especificaciones técnicas o requisitos funcionales: eso va en la spec
- Datos personales de clientes: el archivo solo guarda lo que tienes permiso de guardar

## Ejemplo

```text
Crea el product-context de Widget Studio a partir del README y la landing actual.
```

## Cómo se activa

Esta skill **se activa sola**: Claude Code lee su descripción y la carga cuando la tarea coincide. También puedes pedirla por nombre ("usa la skill product-context") o invocarla con `/product-context:product-context` (plugin) o `/product-context` (copiada a `.claude/skills/`).

## Instalación

### Opción 1: Claude Code, como plugin (recomendada)

Dentro de Claude Code:

```text
/plugin marketplace add nvv-dev/claude-plugins
/plugin install product-context@nvvdev
```

La primera línea agrega el catálogo de nvvdev una sola vez; la segunda instala esta skill. Si prefieres el paquete completo, instala `growth-workflow@nvvdev` en su lugar (incluye esta skill y las demás de [growth-workflow](https://github.com/nvv-dev/growth-workflow)); no instales los dos a la vez.

### Opción 2: Claude Code, copiando la skill

Para un solo proyecto (se comparte con tu equipo por git):

```bash
git clone --depth 1 https://github.com/nvv-dev/product-context.git /tmp/product-context
mkdir -p .claude/skills
cp -R /tmp/product-context/skills/product-context .claude/skills/
```

Para todos tus proyectos, cópiala en `~/.claude/skills/` en lugar de `.claude/skills/`.

### Opción 3: otros agentes

Copia la carpeta `skills/product-context/` en la carpeta de skills de tu agente (cada agente documenta la suya). Con la CLI [skills](https://github.com/vercel-labs/skills) de Vercel Labs:

```bash
DISABLE_TELEMETRY=1 npx skills add nvv-dev/product-context
```

### Verificar

Abre una sesión nueva y pregunta "¿qué skills tienes disponibles?"; `product-context` debe aparecer. Con el plugin, `/plugin` la muestra como instalada.

### Actualizar o desinstalar

- Plugin: `/plugin marketplace update nvvdev` para actualizar; `/plugin uninstall product-context@nvvdev` para quitarla.
- Copia manual: repite la copia para actualizar, o borra la carpeta `.claude/skills/product-context`.

Antes de instalar cualquier skill, incluida esta, conviene leerla: es un solo archivo, [`skills/product-context/SKILL.md`](skills/product-context/SKILL.md). Ver [vetting-external-skills](https://github.com/nvv-dev/vetting-external-skills).

## Contenido

| Ruta | Qué es |
|---|---|
| `skills/product-context/SKILL.md` | La skill: instrucciones en inglés para que los escáneres de seguridad las analicen completas; el agente responde en tu idioma |
| `.claude-plugin/plugin.json` | Manifiesto para instalarla como plugin |
| `.github/workflows/` | Validación de estructura y escaneo con SkillSpector en cada cambio |

## Contribuir

Este repo se **genera** desde [nvv-dev/growth-workflow](https://github.com/nvv-dev/growth-workflow), donde vive la versión canónica. Abre issues y PRs allí. La mejor contribución es un caso real en la sección *Known failures* de la skill, con la regla que lo evita.

## Origen

Escrita desde cero por nvvdev. Inspirada en: [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) (product-marketing: one shared product file that other skills read first).

## Licencia

MIT.

---

## English

**product-context** — Creates and maintains a versioned .agents/product-context.md (product, ideal customer, positioning, objections, proof, learnings) that copy, content, design and SEO work read first.

Install in Claude Code with `/plugin marketplace add nvv-dev/claude-plugins` and `/plugin install product-context@nvvdev`, or copy `skills/product-context/` into `.claude/skills/` (project) or `~/.claude/skills/` (personal). Other agents: copy the folder into their skills directory, or run `DISABLE_TELEMETRY=1 npx skills add nvv-dev/product-context`. Loads automatically when the task matches its description. Canonical source: [nvv-dev/growth-workflow](https://github.com/nvv-dev/growth-workflow). License: MIT.
