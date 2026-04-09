---
name: g4s
description: Gemma 4 Sephirot — Claude Code backed by gemma4:31b-cloud via Ollama Cloud. Sephirot pre-cargado. Nada local. Trigger: /g4s, "g4s", "gemma mode", "modo gemma"
---

# G4S — Gemma 4 Sephirot (Ollama Cloud)

Claude Code wrapper → **gemma4:31b-cloud via Ollama Cloud**. Sephirot activa automáticamente al arrancar.

## Arquitectura

```
M2 ──[g4s]──▶ LiteLLM :4001 ──▶ Ollama :11434 ──▶ Ollama Cloud gemma4:31b
```

Nada local — compute en Ollama Cloud. Config: `~/.openclaw/config/litellm-g4s.yaml`

## Cuándo

Refactoring largo, bulk, exploración. Sin consumir tokens Anthropic.
Para decisiones arquitectónicas o seguridad → Claude normal (Opus).

## Uso

```bash
g4s              # sesión interactiva, Sephirot pre-cargado
g4s --status     # estado del bridge
g4s --stop       # apagar bridge
g4s --pull       # bajar gemma4:31b-cloud
```

## Cuando se activa este skill

```bash
~/.openclaw/tools/g4s
```
