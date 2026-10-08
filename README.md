# ProAccounting — Controle financeiro da feira

Aplicação estática em português para acompanhar produtos, estoque, vendas, despesas, contas a pagar, fluxo de caixa e fechamento de uma feira. Não exige instalação, servidor de aplicação ou conta para funcionar. Criado por Alvaro Monteiro.

## Como utilizar

1. Abra `index.html` no navegador, ou publique esta pasta como um site estático.
2. No primeiro acesso, informe equipe, feira, data e saldo de abertura.
3. Cadastre produtos antes de registrar vendas. O registro da venda atualiza o estoque; o estorno devolve as unidades.
4. Cadastre entradas, despesas e contas a pagar. O dashboard e os relatórios calculam os valores com base nos registros salvos.
5. Para experimentar, use **Backup e dados → Carregar dados de demonstração**. Os exemplos são identificados e podem ser removidos nessa tela.

## Backup e restauração

Em **Backup e dados**, use **Exportar backup agora** para baixar todos os dados e configurações como JSON. Guarde uma cópia fora do dispositivo. Para restaurar, escolha o JSON e confirme a substituição dos dados atuais. O sistema valida a versão do arquivo.

É possível exportar produtos e vendas em CSV. Em **Relatórios**, use **Imprimir / PDF** e escolha “Salvar como PDF” no diálogo de impressão.

## Publicar no GitHub Pages

1. Crie um repositório GitHub vazio e envie o conteúdo desta pasta para a branch `main`.
2. Abra **Settings → Pages** no repositório.
3. Em **Build and deployment**, selecione **Deploy from a branch**, escolha `main` e a pasta `/ (root)` e salve.
4. Aguarde a publicação e abra o endereço indicado pelo GitHub Pages.

O arquivo `.nojekyll` evita processamento Jekyll desnecessário. Para atualizar, envie os novos arquivos para a branch configurada; o Pages publica a versão atualizada automaticamente.

## Armazenamento e limitações

Os dados ficam no `localStorage` do navegador e dispositivo atuais. Não existe sincronização entre dispositivos nem cópia online; limpar os dados do site, usar outro perfil de navegador ou trocar de dispositivo pode tornar os registros indisponíveis. Faça backup JSON regularmente. O navegador limita o espaço disponível. Os gráficos utilizam Chart.js por CDN, portanto precisam de conexão à internet para renderização; os cálculos, cadastros e exportação continuam locais.

Não coloque dados pessoais sensíveis ou credenciais neste sistema. O armazenamento local não fornece controle de acesso nem criptografia.
