# Finanças do Casal — versão aprimorada

Site estático, sem build ou instalação de dependências. Inclui painel mensal, contas a pagar e receber, filtros, status, recorrências, categorias, responsáveis, caixinhas, backup JSON e CSV.

## Publicar no GitHub + Vercel
1. Baixe o ZIP e extraia os arquivos.
2. Abra o repositório do GitHub que já está conectado à Vercel.
3. Faça backup do arquivo atual e envie `index.html` e `vercel.json` para a raiz do repositório (Add file → Upload files → Commit changes).
4. Na Vercel, confira Project → Settings → Build and Deployment: Framework Preset = Other; Root Directory = pasta que contém `index.html`; Build Command em branco e Output Directory em branco para deploy estático de raiz.
5. Abra Deployments e aguarde o novo deploy de produção. Caso o repositório use uma pasta `public`, coloque o `index.html` nela e adapte as configurações.

## Atenção aos dados
O sistema usa `localStorage` no navegador. **Não** sincroniza entre aparelhos, não usa login e não deve ser considerado armazenamento seguro de informações financeiras sensíveis. Faça backups regulares. Publicar na Vercel **não** cria banco de dados.

## Uso
Botões A pagar / A receber abrem o formulário. Em valores, o modo automático interpreta dígitos como centavos; no modo manual, digite `123,45`. Lançamentos recorrentes são gerados como ocorrências independentes. A edição altera somente a ocorrência selecionada. Projetos/caixinhas não alteram o saldo do mês, pois são acompanhamento de objetivos, não transferência bancária.
