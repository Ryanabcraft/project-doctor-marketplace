# Project Dotcor Marketplace

Marketplace local/Git para instalar o plugin Project Dotcor no Codex.

## Como usar

Adicione este marketplace no arquivo `C:\Users\<seu-usuario>\.codex\config.toml`:

```toml
[marketplaces.ryan-plugins]
source_type = "git"
source = "https://github.com/Ryanabcraft/project-dotcor-marketplace.git"
```

Depois reinicie o Codex e procure por `Project Dotcor` na tela de plugins.

## Plugin incluído

- `project-dotcor`: plugin de diagnóstico geral para projetos locais.
- `project-doctor`: skill que identifica stack, arquivos importantes, comandos de run/test/build e problemas comuns.
