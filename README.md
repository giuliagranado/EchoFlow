# 🌊 EchoFlow

> **Agente de Automação Híbrido e 100% Local para Desktop**  
> *Projeto desenvolvido para o Hackathon Hack Brasil 2026*

---

## 📌 Sobre o Projeto

O **EchoFlow** é um assistente inteligente para PC que aprende tarefas repetitivas observando as ações do usuário sob demanda e aceita comandos em linguagem natural (texto ou voz) para executar automações de forma adaptativa.

Em vez de apenas gravar cliques estáticos por coordenadas fixas (que quebram se uma janela se mover), a IA local do EchoFlow interpreta o contexto e a **intenção** do usuário, transformando sequências de ações em scripts limpos e reutilizáveis em Python.

---

## 🔒 Privacidade em Primeiro Lugar

Ao contrário de ferramentas de gravação contínua de tela, o EchoFlow garante segurança e privacidade total:

- **Captura Sob Demanda:** A gravação só é ativada quando o usuário aciona explicitamente o botão "Rec".
- **Inferência 100% Offline:** Modelos de linguagem e visão (como Google Gemma via Ollama) rodam localmente na própria máquina.
- **Zero Envio para a Nuvem:** Nenhum print de tela ou dado do usuário sai do seu computador.

---

## 🚀 Como Funciona (Os 3 Pilares)

1. **Captura Leve e Sob Demanda:** O aplicativo registra o fluxo de trabalho (cliques de mouse e janela ativa) e realiza capturas de tela pontuais apenas no momento da ação.
2. **De Cliques para Intenção (IA Local):** O modelo local analisa o fluxo de ações e converte a interação em um script Python inteligente e ajustável.
3. **Comando Híbrido Adaptativo:** O usuário aciona o agente por voz ou texto (ex: *"Faz aquele fechamento de mês, mas hoje envia para o e-mail do João"*). O assistente recupera a automação salva e adapta apenas os parâmetros necessários.

---

## 🛠️ Stack Tecnológica

| Camada | Tecnologias | Descrição / Função |
| :--- | :--- | :--- |
| **Captura & Contexto** | `pynput`, `mss`, `pywinauto` / `AT-SPI`, `EasyOCR` | Detecção de interação do usuário, capturas de tela velozes, estrutura de acessibilidade do SO e leitura de texto. |
| **IA Local & Voz** | `Ollama` (`Gemma 2`, `PaliGemma`), `faster-whisper` | Inferência offline para tradução de intenção, análise visual e comandos de voz. |
| **Motor de Automação** | `Playwright`, `PyAutoGUI`, `Pandas`, `OpenPyXL` | Execução de tarefas em navegadores, aplicativos desktop e manipulação direta de planilhas. |
| **Memória & Busca** | `SQLite`, `ChromaDB` / `FAISS` | Banco relacional para histórico e banco vetorial para busca semântica de automações salvas. |
| **Interface Desktop** | `Tauri` / `CustomTkinter` / `PyQt` | Barra flutuante de acionamento rápido e painel de controle intuitivo. |

---

## 💻 Como Executar

```bash
# 1. Clonar o repositório
git clone <URL-DO-SEU-REPOSITORIO>

# 2. Acessar a pasta do projeto
cd EchoFlow

# 3. Criar e ativar o ambiente virtual
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate

# 4. Instalar as dependências
pip install -r requirements.txt
```

---

## 📄 Licença

Este projeto é disponibilizado sob a licença **MIT**. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
