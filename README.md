# Fale com o Zé Gotinha

Chatbot oficial de vacinas — proposta de portfólio

## Resumo

- Chatbot informativo sobre vacinação baseado em conteúdos oficiais do Programa Nacional de Imunizações (PNI) e no Calendário Nacional de Vacinação.
- Objetivo: disseminar conhecimento científico e estimular a cobertura vacinal, sempre com referências e orientação para procurar a UBS.

## Conteúdo incluído

- `kb_fale_com_ze_gotinha.json` — base inicial de FAQs e respostas.
- `assets/` — imagens, avatar e outros recursos visuais.
- `index.html` — página pública com o widget do chatbot (GitHub Pages).

## Principais fontes (usar links oficiais nas respostas)

- Vacinação — Ministério da Saúde
- Programa Nacional de Imunizações (PNI)
- Calendário Nacional de Vacinação
- Calendário Técnico Nacional de Vacinação

## Integração do agente (visão técnica)

- Indexação: Azure AI Search (chunking semântico, extração de tabelas).
- RAG: Copilot Studio / Power Virtual Agents orquestram intents e usam a fonte de documentos + KB JSON.
- O widget web incorpora o canal publicado pelo Copilot Studio.

## Guardrails e governança

- Não fornecer aconselhamento clínico — sempre direcionar para UBS/CRIE e profissionais de saúde.
- Exibir fontes com data em todas as respostas.
- Manter versões das fontes (SharePoint) e registrar atualizações do KB.
- Controlar atualizações: usar issues/PRs para mudanças no KB e notas técnicas.

---

© 2026 — Proposta de portfólio. Este protótipo usa fontes oficiais do Ministério da Saúde e não substitui orientação médica. Para vacinar-se, procure a UBS.
