# Project Doctor Marketplace

Marketplace local/Git para instalar o plugin Project Doctor no Codex.

## Como usar

Adicione este marketplace no arquivo `C:\Users\<seu-usuario>\.codex\config.toml`:

```toml
[marketplaces.ryan-plugins]
source_type = "git"
source = "https://github.com/Ryanabcraft/project-doctor-marketplace.git"
```

Depois reinicie o Codex e procure por `Project Doctor` na tela de plugins.

## Plugin incluido

- `project-doctor`: plugin de diagnostico geral para projetos locais.
- `project-doctor`: skill que identifica stack, arquivos importantes, comandos de run/test/build e problemas comuns.

