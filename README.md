# 🤖 Criação de Agentes de IA com o Microsoft AI Foundry

> **Repositório Nota 10** | Projeto de Estudo e Capacitação Técnica sobre Agentes de IA, Engenharia de Prompts e RAG no Microsoft AI Foundry.

---

## 📌 1. Contexto e Objetivos

### Contexto
O avanço da Inteligência Artificial Generativa e das arquiteturas agenticas (*Agentic AI*) transformou o desenvolvimento de software. A plataforma **Microsoft AI Foundry** (anteriormente conhecida como Azure AI Studio) consolida ferramentas para conceber, construir, avaliar e implantar agentes inteligentes prontos para produção. 

Este repositório documenta a jornada de estudo e estruturação pedagógica baseada no curso de **Criação de Agentes de IA com o Microsoft AI Foundry** (40 horas), alinhado às diretrizes do SENAI-SP, à trilha no-code de 40h para iniciantes e ao guia de preparação oficial do exame **AI-103 (Azure AI Application and Agent Developer)**.

### Objetivos de Estudo
* **Compreensão Arquitetural:** Diferenciar automação tradicional de agentes autônomos de IA, compreendendo o ciclo de vida dos agentes no Microsoft Foundry (Foundry Agent Service, Threads, Runs, Messages e Guardrails).
* **Engenharia de Prompts & Conversação:** Dominar o design de System Messages, definição de personas, diretrizes de segurança e controle de estado conversacional.
* **Fundamentação em Conhecimento (RAG & Foundry IQ):** Implementar bases de conhecimento conectadas a documentos corporativos (PDFs, manuais, políticas de RH) sem necessidade de programação complexa.
* **IA Responsável & Governança:** Aplicar filtros de conteúdo, mitigar alucinações e configurar políticas de segurança antes da publicação.
* **Estruturação de Ensino e Entregáveis:** Planejar um cronograma de 40 horas adaptado para alunos iniciantes e estruturar entregas e rubricas de avaliação integráveis ao Google Classroom.

---

## 📚 2. Curadoria de Fontes

Para fundamentar este caderno de estudos e alimentar o assistente no **Gemini Notebook**, foram curadas e analisadas 3 fontes primárias essenciais:

| # | Fonte / Documento | Formato | Descrição & Escopo |
|---|-------------------|---------|---------------------|
| 1 | **Trilha de Formação - Construindo seu Primeiro Agente com Microsoft Foundry** | `.docx` | Roteiro de 40 horas focado em alunos iniciantes e leigos. Divide o aprendizado em 6 módulos práticos, culminando em um *Projeto Integrador: Agente Corporativo Inteligente*. |
| 2 | **Plano de Curso: Criação de Agentes de IA com o Microsoft AI Foundry** | `.docx` | Plano formal do SENAI-SP (Aperfeiçoamento Profissional - 40h). Define capacidades técnicas, socioemocionais, ementa de conteúdos formativos, critérios de avaliação e requisitos de infraestrutura. |
| 3 | **AI-103: Desenvolvedor de Aplicativos e Agentes de IA do Azure - Guia de Preparação do Instrutor** | `.pdf` | Guia oficial da Microsoft (Março/2026) para o exame de certificação AI-103. Cobre o espectro completo do Microsoft Foundry, SDKs, orquestração multiagente, conectores MCP, visão, fala e IA Responsável. |

---

## 🧪 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting & Raciocínio)

### Perguntas Estratégicas Elaboradas
Durante as rodadas de teste e refinamento no Gemini Notebook, foram desenvolvidos prompts estratégicos para extrair cronogramas, matrizes de avaliação e scripts de automação.

#### Variação 1: Prompt Inicial (Genérico)
> *"Crie um curso de 40h de agentes de IA para o classroom."*
* **Resultado Obtido:** Resposta genérica, com tópicos abstratos de IA e sem consideração pela lentidão de alunos iniciantes ou pelos repositórios de laboratório oficiais.
* **Inconveniente/Dificuldade:** Faltavam evidências de entrega específicas, critérios de pontuação e divisão de carga horária adequada para leigos.

#### Variação 2: Prompt Estruturado e Contextualizado (Refinado)
> *"Crie um cronograma para 40h, utilizando os cursos do Microsoft Learn. Encontre os laboratórios que possam ser realizados. Os alunos são leigos e demoram para realizar os laboratórios; monte um planejamento com entregas no Classroom baseando-se estritamente nas fontes."*
* **Resultado Obtido:** Cronograma altamente prático distribuído em 6 módulos, com tempos estendidos para laboratórios no-code (ex: `mslearn-ai-fundamentals/Instructions/Exercises/00-explore-foundry.html`), além de 5 entregas claras para o Google Classroom (capturas de tela, logs de teste, relatórios).
* **Referência nas Fontes:** Módulo 6 da Trilha de 40h (Projeto Integrador - Etapas 1 a 7) e diretrizes pedagógicas do Plano de Curso SENAI.

#### Variação 3: Prompt de Automação e Integração (Script de Atividades)
> *"Crie um script para importar/gerar as atividades propostas no Google Classroom (ex: em Python/API ou CSV)."*
* **Resultado Obtido:** Script Python utilizando o padrão da Google Classroom API para geração automática das 5 atividades do Projeto Integrador, com títulos, descrições detalhadas, evidências exigidas e rubrica de pontuação.

### "Cicatrizes" e Lições Aprendidas (Troubleshooting)
1. **Diferença de Nomenclatura (Azure AI Studio vs. Microsoft Foundry):**
   * *Desafio:* Materiais antigos referiam-se a "Azure AI Studio".
   * *Solução:* Foi necessário padronizar a terminologia para **Microsoft Foundry** e orientar os alunos a utilizarem estritamente a *Nova Experiência do Portal* para evitar inconsistências de interface nos laboratórios.
2. **Tempo de Execução de Leigos em Laboratórios:**
   * *Desafio:* Alunos não técnicos se perdem facilmente em configurações de ambiente e permissões RBAC.
   * *Solução:* O cronograma alocou 8h para o Módulo 1 (Primeiros Passos) e 10h para o Módulo 3 (Construção do Agente UI), incluindo demonstrações prévias (*demos*) conduzidas pelo instrutor antes da prática autônoma.
3. **Escopo Fechado em Respostas RAG (Mitigação de Alucinações):**
   * *Desafio:* Agentes tendiam a responder perguntas gerais fora do contexto corporativo.
   * *Solução:* Ajuste da *System Message* com instrução explícita de fallback:
     > *"Você é um assistente corporativo educado e profissional. Responda apenas utilizando as informações disponíveis nos documentos fornecidos. Caso não encontre a resposta, oriente o usuário a procurar o setor responsável."*

---

## 📖 4. Miniguia de Estudo (Entrega Final)

### A. Resumo Estruturado dos Módulos (Trilha 40h + SENAI)

```
[Módulo 1: Primeiros Passos (8h)] ──► [Módulo 2: Prompts & Modelos (8h)]
            │                                     │
            ▼                                     ▼
[Módulo 3: Construção sem Código (10h)] ──► [Módulo 4: RAG & Documentos (6h)]
            │                                     │
            ▼                                     ▼
[Módulo 5: IA Responsável (3h)]  ──► [Módulo 6: Projeto Integrador (5h)]
```

* **Módulo 1: Primeiros Passos e Ambiente (8h)**
  * Conceitos de IA Generativa, navegação no portal Microsoft Foundry, criação de projetos e experimentos no Playground.
* **Módulo 2: Modelos e Engenharia de Prompts (8h)**
  * Seleção de modelos no Catálogo, estrutura de prompts (instruções, contexto, exemplos, formato de saída) e ajustes de parâmetros.
* **Módulo 3: Construindo o Primeiro Agente sem Código (10h)**
  * Configuração no *Foundry Agent Service*, definição de personas, gerenciamento de threads, mensagens e estado conversacional.
* **Módulo 4: Base de Conhecimento e Documentos - RAG (6h)**
  * Upload de PDFs corporativos (Políticas de RH, Benefícios, Manuais) usando *Foundry IQ* para fundamentação de respostas (*Grounding*).
* **Módulo 5: IA Responsável e Segurança (3h)**
  * Configuração de Filtros de Conteúdo (*Content Safety*), guardrails éticos, controle de vieses e testes de verificação de limites.
* **Módulo 6: Projeto Integrador Final (5h)**
  * Execução e publicação do *Assistente Corporativo Inteligente*, registro de 10 testes funcionais, relatório de avaliação e publicação no GitHub.

---

### B. Glossário de Principais Conceitos

| Conceito | Definição Técnica |
|----------|-------------------|
| **Microsoft Foundry** | Plataforma unificada da Microsoft (sucessora do Azure AI Studio) para desenvolvimento, avaliação e implantação de modelos e agentes de IA. |
| **Foundry Agent Service** | Serviço gerenciado que orquestra a execução de agentes, mantendo histórico de conversas (*Threads*), estado e execução de ferramentas (*Runs*). |
| **RAG (Retrieval-Augmented Generation)** | Técnica que conecta modelos de linguagem a bases de dados externas (como documentos e PDFs) para gerar respostas fundamentadas e precisas. |
| **Foundry IQ** | Recurso do Microsoft Foundry focado em extração de informações, busca vetorial e gerenciamento de conhecimento para agentes. |
| **System Message / Prompt do Sistema** | Conjunto primário de instruções que define as regras, tom de voz, persona e limites de atuação do agente de IA. |
| **IA Responsável (Responsible AI)** | Conjunto de práticas e ferramentas (filtros de conteúdo, verificação de alucinações, mitigação de danos) para garantir uso ético e seguro da IA. |
| **MCP (Model Context Protocol)** | Padrão aberto de conexão que permite a agentes de IA integrarem-se a ferramentas, APIs e sistemas externos. |

---

### C. Conjunto de Prompts Reutilizáveis (Biblioteca de Prompts)

#### 1. Prompt do Sistema para Assistente Corporativo (No-Code RAG)
```text
Você é o Assistente Corporativo Inteligente da [NOME DA EMPRESA].
Sua função é auxiliar os colaboradores fornecendo respostas precisas sobre políticas internas, benefícios e procedimentos corporativos.

DIRETRIZES DE COMPORTAMENTO:
1. Responda APENAS utilizando as informações contidas nos documentos fornecidos na base de conhecimento.
2. Seja sempre cortês, profissional e conciso.
3. Se a informação não estiver presente nos documentos, diga claramente: "Não encontrei essa informação nos documentos corporativos disponíveis. Por favor, entre em contato com o setor de Recursos Humanos."
4. NUNCA invente informações, datas, valores ou procedimentos não documentados.
```

#### 2. Prompt para Avaliação e Teste de Estresse do Agente
```text
Atue como um auditor de segurança e qualidade de IA. Avalie a seguinte resposta fornecida pelo agente corporativo em relação à pergunta do usuário e ao documento fonte:

Pergunta do Usuário: [INSERIR PERGUNTA]
Documento Fonte: [INSERIR TRECHO DO DOCUMENTO]
Resposta do Agente: [INSERIR RESPOSTA DO AGENTE]

Analise e responda nos seguintes pontos:
1. Aderência: A resposta usou estritamente o documento fonte? (Sim/Não)
2. Precisão: Houve alguma alucinação ou extrapolação?
3. Tom de Voz: O tom foi cortês e profissional?
4. Sugestão de Melhoria de Prompt: Como podemos ajustar as instruções do agente caso haja falha?
```

#### 3. Script Python Reutilizável para Geração de Atividades no Google Classroom API
```python
"""
Script de Atividades do Projeto Integrador - Google Classroom API
Gera automaticamente as 5 tarefas do cronograma de 40h para o Microsoft AI Foundry.
"""

def obter_atividades_classroom():
    return [
        {
            "title": "Atividade 1: Criação do Projeto no Microsoft Foundry",
            "description": "Acesse o portal Microsoft Foundry e crie seu projeto inicial.\n\nEvidências:\n1. Nome do projeto.\n2. Print do Dashboard.",
            "maxPoints": 10
        },
        {
            "title": "Atividade 2: Configuração do Agente e System Message",
            "description": "Configure o agente 'Assistente Corporativo' e defina o System Message de segurança.\n\nEvidência:\n1. Captura de tela das instruções salvas.",
            "maxPoints": 20
        },
        {
            "title": "Atividade 3: Upload da Base de Conhecimento (RAG)",
            "description": "Carregue no mínimo 3 documentos PDF (Políticas de RH, Benefícios, Manuais).\n\nEvidência:\n1. Lista de arquivos confirmados na base de conhecimento.",
            "maxPoints": 20
        },
        {
            "title": "Atividade 4: Log de 10 Testes de Conversação",
            "description": "Realize 10 perguntas de teste ao agente e avalie se ele usou os documentos.\n\nEvidência:\n1. Registro impresso/PDF do histórico de perguntas e respostas.",
            "maxPoints": 20
        },
        {
            "title": "Atividade 5: Relatório Final e Avaliação de IA Responsável",
            "description": "Elabore um relatório consolidado com os pontos fortes do agente, melhorias feitas e publicação.\n\nEvidência:\n1. Relatório em PDF + Print do agente publicado.",
            "maxPoints": 30
        }
    ]

if __name__ == "__main__":
    for act in obter_atividades_classroom():
        print(f"📌 {act['title']} ({act['maxPoints']} pts)")
```

---

## 🛠️ Como Utilizar Este Repositório
1. **Para Alunos:** Siga a ordem dos módulos no Miniguia de Estudo e utilize os prompts fornecidos para testar seu agente no Microsoft Foundry.
2. **Para Educadores/Instrutores:** Utilize o script Python e as rubricas de avaliação fornecidas para configurar sua turma no Google Classroom ou LMS de preferência.

---
*Projeto desenvolvido como parte do curso de Criação de Agentes de IA com o Microsoft AI Foundry.*

