# OrganizIA

App de finanças pessoais em português do Brasil: o que vence, quanto sobra no mês e como fica o saldo dia a dia até o próximo recebimento. Nasceu do módulo financeiro do Jabu.

## O que tem

- Visão geral do mês, com contas atrasadas e dos próximos 7 dias
- Lançamentos (despesa, receita, transferência), fixos e parcelados
- Contas bancárias com saldo atual e previsto
- Cartões de crédito com fechamento, vencimento, limite e fatura
- Orçamento mensal por categoria
- Relatórios por categoria, 12 meses e fluxo de caixa diário
- Carteira de investimentos, aportes e resgates
- Lançamento por texto, importação de extrato (OFX, CSV) e importação do export do Jabu
- Backup e restauração em arquivo JSON

## Como funciona

É um site estático, sem build: tudo está em `index.html`. Os dados ficam no navegador de quem usa (`localStorage`); nada é enviado a servidor. Por isso:

- cada aparelho tem os seus dados; não há sincronização ainda;
- se os dados do navegador forem apagados, os lançamentos se perdem. Use **Ajustes › Backup › Baixar backup** de vez em quando.

Nenhum dado pessoal deve ser gravado neste repositório.

## Publicar

Na Vercel, importe o repositório com o preset **Other**, sem comando de build e sem pasta de saída. O `vercel.json` só define cabeçalhos de segurança.

## Usar no celular

Abra o endereço da Vercel no navegador do celular e adicione à tela de início:

- iPhone (Safari): Compartilhar › Adicionar à Tela de Início
- Android (Chrome): menu ⋮ › Adicionar à tela inicial

## Rodar no computador

Abra `index.html` no navegador ou sirva a pasta com `python3 -m http.server`.
