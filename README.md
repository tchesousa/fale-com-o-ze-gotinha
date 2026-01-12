# Fale com o Zé Gotinha

Chatbot oficial de vacinas — proposta de portfólio

## Resumo

- Chatbot informativo sobre vacinação baseado em conteúdos oficiais do Programa Nacional de Imunizações (PNI) e no Calendário Nacional de Vacinação.
- Objetivo: disseminar conhecimento científico e estimular a cobertura vacinal, sempre com referências e orientação para procurar a UBS.

## Conteúdo incluído

- `kb_fale_com_ze_gotinha.json` �� base inicial de FAQs e respostas.
- `assets/` — imagens, avatar e outros recursos visuais.
- `index.html` — página pública com o widget do chatbot (GitHub Pages).

## Principais fontes (usar links oficiais nas respostas)

- Vacinação — Ministério da Saúde
- Programa Nacional de Imunizações (PNI)
- Calendário Nacional de Vacinação
- Calendário Técnico Nacional de Vacinação

## Como publicar no GitHub Pages

1. Verifique que o repositório tem `index.html` na raiz (ou renomeie `portfolio.html` → `index.html`).
2. No GitHub: Settings → Pages → Branch: `main`, Folder: `/ (root)` → Save.
3. Aguarde alguns minutos e acesse `https://<usuario>.github.io/<repo>/`.
4. (Opcional) Adicione `CNAME` na raiz para usar domínio personalizado.

## Integração do agente (visão técnica)

- Indexação: Azure AI Search (chunking semântico, extração de tabelas).
- RAG: Copilot Studio / Power Virtual Agents orquestram intents e usam a fonte de documentos + KB JSON.
- O widget web incorpora o canal publicado pelo Copilot Studio.

## Guardrails e governança

- Não fornecer aconselhamento clínico — sempre direcionar para UBS/CRIE e profissionais de saúde.
- Exibir fontes com data em todas as respostas.
- Manter versões das fontes (SharePoint) e registrar atualizações do KB.
- Controlar atualizações: usar issues/PRs para mudanças no KB e notas técnicas.

## Checklist recomendado antes da publicação

- [ ] `index.html` presente e apontando para assets corretos.
- [ ] `kb_fale_com_ze_gotinha.json` validado (estrutura JSON, campos `question`, `answer`, `sources`, `date`).
- [ ] Todas as respostas exibem fontes e data.
- [ ] Banner/disclaimer visível: “Este protótipo usa fontes oficiais do Ministério da Saúde e não substitui orientação médica.”
- [ ] Política de privacidade mínima / aviso sobre dados coletados (se houver logs ou analytics).
- [ ] Testes de acessibilidade (cores, contraste, navegação por teclado).
- [ ] Testes de linkagem para PDFs/Notas Técnicas (links abrem em nova aba).

## Publicação

Siga as instruções acima para publicar o site via GitHub Pages. Para integrar o agente, publique o bot no Copilot Studio / Power Virtual Agents e incorpore o snippet no `index.html`.

---

© 2026 — Proposta de portfólio. Este protótipo usa fontes oficiais do Ministério da Saúde e não substitui orientação médica. Para vacinar-se, procure a UBS.
