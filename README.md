# Football Manager 3.8 — Mega Arena Suprema

O jogo original foi mantido e recebeu uma área opcional de conta e salvamento na nuvem.

## O que mudou
- Mantém o salvamento local original (`construaClubeSave`).
- Adiciona cadastro e entrada por e-mail/senha usando Supabase Auth.
- Salva o progresso completo da conta na tabela privada `player_saves`.
- Permite recuperar o salvamento na nuvem em outro navegador/dispositivo.
- Mantém os recursos anteriores, incluindo ranking global e códigos especiais.

## Configuração obrigatória para nuvem
1. Abra o projeto Supabase que já está configurado no jogo.
2. Entre em **SQL Editor** e execute todo o arquivo `SUPABASE_SETUP.sql`.
3. Em **Authentication > URL Configuration**, configure a URL do site publicado se o Supabase solicitar.
4. Publique `index.html` e `SUPABASE_SETUP.sql` no GitHub Pages (o SQL é executado no Supabase, não no navegador).
5. No jogo, crie uma conta e entre. Use o mesmo e-mail para recuperar o progresso em outro dispositivo.

A conta na nuvem precisa ser criada pelo jogador. Os dados locais antigos não podem ser associados automaticamente a uma pessoa sem ela entrar/criar uma conta nesse dispositivo. Na primeira conta criada naquele dispositivo, o sistema envia o progresso local se ainda não existir um salvamento remoto. Se a confirmação de e-mail estiver ativada, confirme o e-mail antes de entrar.

**Importante:** não apague os dados do navegador antigo antes de entrar na conta e confirmar que o salvamento foi sincronizado. O ranking global continua separado do salvamento pessoal.
