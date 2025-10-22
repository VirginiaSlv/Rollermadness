# Rollermadness

o projeto RollerMadness é um jogo Simples, realizado para particar uma atividade acadêmica. 

## 🎯 Objetivo do Projeto

1.  **Implementar a Transição de Fases:** Mudar da Fase 1 para a Fase 2 após o jogador atingir um certo número de coletas (5 moedas).
2.  **Criação da Fase 2:** Introdução de novos obstáculos.
3.  **Sistema de Vitória:** Implementação de uma tela de Vitória ao concluir os objetivos da Fase 2.

---

## ⚙️ Configuração e Inicialização

Para rodar o projeto corretamente, siga estas instruções no Unity Editor:

### 1. Configuração do Build Settings

As duas fases do jogo são implementadas como cenas separadas.

1.  Vá em **File** -> **Build Settings...**
2.  Arraste as cenas (`Fase1` e `Fase2`, ou os nomes que você usou) para a lista **Scenes In Build**.

### 2. Configuração do GameManager (Fase 1)

**Cena: `Fase1`**

| Variável (no Inspector) | Valor/Objeto | Observação |
| :--- | :--- | :--- |
| **Is Phase One** | ✅ (Marcado) | Indica que a cena atual é a Fase 1. |
| **Coins To Phase 2** | `5` | Define o requisito de 5 moedas para mudar de fase. |
| **Next Phase Scene Name** | `[Nome da Cena da Fase 2]` | **IMPORTANTE:** Defina o nome exato da sua segunda cena (Ex: `Fase2`). |
| **Can Beat Level** | ✅ (Marcado) | Mantém o sistema de pontuação de meta ativo. |
| **Beat Level Canvas** | `[Placeholder/Canvas]` | Preencher para evitar o erro `UnassignedReferenceException`. |
| **Victory Canvas** | `[Seu Canvas de Vitória]` | Arrastar o Canvas de Vitória criado na Hierarquia. |

### 3. Configuração do GameManager (Fase 2)

**Cena: `Fase2`**

| Variável (no Inspector) | Valor/Objeto | Observação |
| :--- | :--- | :--- |
| **Is Phase One** | ❌ (Desmarcado) | Indica que a cena atual é a Fase 2. |
| **Can Beat Level** | ✅ (Marcado) | Ativa a contagem para a vitória final. |
| **Beat Level Score** | `[Valor de Moedas]` | Define o total de moedas para acionar a tela de vitória. |
| **Victory Canvas** | `[Seu Canvas de Vitória]` | Arrastar o Canvas de Vitória criado na Hierarquia. |

