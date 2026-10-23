# 🐷 Porquinho Financeiro
### Case study · Aplicação pessoal de finanças

<div align="center">

**Organização financeira com foco em clareza, privacidade e uso mobile-first.**

[🌐 Abrir demonstração](https://porquinho-financeiro.guilhermekira2015.workers.dev/) · [👤 Perfil GitHub](https://github.com/Maciel-hub)

</div>

---

## Visão geral

O **Porquinho Financeiro** é uma Progressive Web App (PWA) criada para ajudar a acompanhar receitas, despesas, contas a vencer, dívidas, metas e comprovantes em uma experiência adaptada a dispositivos móveis.

O projeto parte de um problema cotidiano: informações financeiras acabam espalhadas entre aplicativos, anotações e comprovantes. A proposta é reunir esses registros em um só lugar, com uma interface clara e ferramentas práticas para acompanhar a situação financeira.

> Este estudo de caso descreve o projeto e seu estado conhecido. A demonstração pode evoluir ao longo do tempo; recursos que dependem de serviços adicionais são identificados como pendentes.

## Funcionalidades implementadas

- **Dashboard financeiro:** visão de saldos e movimentações, atalhos e próximos pagamentos.
- **Lançamentos:** registro de receitas e despesas.
- **Contas e vencimentos:** alertas visuais para contas próximas do vencimento e contas atrasadas.
- **Dívidas e parcelas:** acompanhamento dos compromissos financeiros, incluindo cuidados com parcelas descontadas em folha para evitar duplicidade no saldo.
- **Metas:** criação de reservas e acompanhamento do valor destinado, sem alterar automaticamente o saldo bancário.
- **Análises:** gráficos de gastos e receitas por período/categoria.
- **Comprovantes:** leitura OCR local assistida; os dados extraídos devem ser revisados e confirmados antes de registrar o lançamento.
- **Exportação e backup:** recursos para preservar e exportar dados do usuário.
- **Experiência PWA:** interface adaptável, instalação na tela inicial e recursos de cache/offline.

## Arquitetura e tecnologias

| Camada | Tecnologia / abordagem |
| --- | --- |
| Interface | HTML, CSS e JavaScript |
| Aplicação | Progressive Web App (PWA) |
| Dados e autenticação | Supabase |
| Proteção de dados | Autenticação e políticas Row Level Security (RLS) |
| Hospedagem atual | Cloudflare Workers |
| Recursos offline | Service Worker e armazenamento local |
| Comprovantes | OCR local com revisão pelo usuário |
| Fluxo de trabalho | Git e versionamento |

O projeto utiliza JavaScript no cliente e mantém a lógica da aplicação separada dos estilos e de parte dos recursos de interface. A camada de dados usa autenticação e políticas de acesso para separar as informações dos usuários.

## Segurança e privacidade

Finanças pessoais são dados sensíveis. Por isso, o projeto considera alguns princípios importantes:

- Não publicar backups financeiros, senhas ou chaves privadas no repositório.
- Manter o código-fonte em repositório privado enquanto o projeto não estiver preparado para publicação.
- Aplicar autenticação e políticas de acesso no banco de dados.
- Solicitar revisão humana dos dados extraídos de comprovantes antes de salvá-los.
- Informar claramente quando uma integração ainda não está ativa.

**Limitações conhecidas no estado documentado:** notificações locais de teste não equivalem a notificações push automáticas. O envio de push agendado ainda depende de um emissor no servidor e de um agendador confiável. Recursos de compartilhamento financeiro entre usuários também não devem ser considerados disponíveis sem implementação e validação específicas.

## Desafios e decisões de produto

- **Priorizar o uso no celular:** estruturar a navegação e os principais fluxos para telas pequenas.
- **Evitar lançamentos incorretos:** permitir que o usuário revise os campos extraídos do comprovante.
- **Não duplicar movimentos:** considerar situações em que uma parcela já foi descontada diretamente no holerite.
- **Ser transparente sobre o estado dos recursos:** distinguir funcionalidades implementadas de integrações ainda pendentes.
- **Preservar os dados existentes:** tratar alterações de interface sem modificar registros financeiros do usuário.

## Próximas etapas

- Validar os fluxos em navegadores reais e em dispositivos iOS e Android.
- Medir carregamento, sincronização e comportamento offline.
- Finalizar e testar o fluxo de notificações push automáticas antes de anunciá-lo como disponível.
- Melhorar a documentação técnica e adicionar capturas reais da interface.
- Avaliar uma publicação pública do código apenas depois de revisar configurações, dependências e possíveis informações privadas.

## Demonstração

**[Abrir o Porquinho Financeiro](https://porquinho-financeiro.guilhermekira2015.workers.dev/)**

A demonstração é hospedada separadamente do repositório público de portfólio. Não utilize dados financeiros reais em ambientes de demonstração sem antes confirmar que o ambiente e as políticas de privacidade estão adequados ao seu uso.

---

<div align="center">

*Construído para resolver um problema real, com evolução contínua e transparência técnica.*

</div>
