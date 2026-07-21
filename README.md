# ⚽ Academia de Futebol Tycoon (Roblox)

**Versão:** 0.0.1  
**Linguagem:** Luau (`--!strict`)  
**Arquitetura:** Modular Service Framework (Client-Server-Shared)  

## 📌 Visão Geral do Projeto
Jogo no Roblox em que o jogador administra e evolui uma academia de futebol através de progressão ativa (treino manual, chutes ao gol, física interativa da bola) e expansão física com equipamentos automáticos (Passadores Automáticos).

## 📂 Módulos e Estrutura Principal
- `ReplicatedStorage.SYSTEM_ARCHITECTURE`: Single Source of Truth (SSOT) e diretrizes de desenvolvimento.
- `ReplicatedStorage.Localization`: Módulo de internacionalização (Inglês como base nativa com suporte a PT-BR e ES-ES).
- `ReplicatedStorage.TycoonItems`: Templates dos equipamentos da academia.
- `ServerScriptService.PlayerDataManager`: Gerenciador de dados resiliente com reconciliação e suporte a DataStore / Sessão em memória.
- `ServerScriptService.PlayerDataServer`: Eventos de entrada/saída de jogadores e desligamento seguro (`BindToClose`).
- `ServerScriptService.TycoonManager`: Gerenciador server-authoritative de mecânicas físicas de futebol (gol real e bola física) e automações.
- `StarterGui.MainHUDGui` & `StarterPlayerScripts.HUDController`: Interface de usuário moderna (HUD de moedas) sincronizada em tempo real.
