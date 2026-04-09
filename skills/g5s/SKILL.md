---
name: g5s
description: GLM-5.1 Sephirot — Claude Code backed by glm-5.1:cloud via Ollama Cloud. Sephirot pre-cargado. Nada local. Trigger: /g5s, "g5s", "glm mode", "modo glm"
---

# G5S — GLM-5.1 Sephirot (Ollama Cloud)

Claude Code wrapper → **glm-5.1:cloud via Ollama Cloud**. Sephirot activa automáticamente al arrancar.

## Arquitectura

```
M2 ──[g5s]──▶ LiteLLM :4002 ──▶ Ollama :11434 ──▶ Ollama Cloud glm-5.1
```

Nada local — compute en Ollama Cloud. Config: `~/.openclaw/config/litellm-g5s.yaml`

## Cuándo

Context 200K, coding SOTA ZAI. Tasks donde GLM-5.1 tiene ventaja sobre Gemma.
Para decisiones arquitectónicas → Claude normal (Opus).

## Uso

```bash
g5s              # sesión interactiva, Sephirot pre-cargado
g5s --status     # estado del bridge
g5s --stop       # apagar bridge
g5s --pull       # bajar glm-5.1:cloud
```

## Cuando se activa este skill

```bash
~/.openclaw/tools/g5s
```
