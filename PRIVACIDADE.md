# Privacidade do MultiStream Chat Monitor (MCM)

O MCM é um app gratuito, para Android e Windows, que junta num lugar só o chat das suas lives na Twitch, no YouTube e no TikTok. Este documento diz, em linguagem simples, o que o MCM pede, o que ele guarda e com quem ele conversa.

**Resumo:** o MCM não tem conta, não tem servidor próprio, não tem anúncios e não coleta nada sobre você. Tudo o que ele guarda fica no seu aparelho.

## O que o MCM não faz

- Não pede cadastro nem conta do MCM.
- Não manda nada para servidores do criador do MCM. Esses servidores não existem.
- Não tem anúncios, estatísticas de uso ou rastreamento.
- Não grava registros (logs) do que você faz.
- Nunca vê a sua senha da Twitch, do YouTube ou do TikTok.
- Não lê seus arquivos, fotos, contatos, câmera, microfone ou localização. A única exceção é a imagem que você mesmo escolher para o seu avatar (veja “O que fica guardado”).

## O que o MCM pede

- **Twitch:** uma autorização feita na própria página da Twitch, com um código. Ela dá ao MCM só a permissão de **ler o chat** (`user:read:chat`). O MCM não consegue mandar mensagens, moderar nem mexer na sua conta.
- **YouTube e TikTok:** nada. O MCM lê o chat público da live, como qualquer pessoa que abre a página, sem conta e sem login.
- **Permissões no Android:**
  - **Internet**, para ler os chats;
  - **serviço em primeiro plano e notificações**, para os chats continuarem ligados com o app minimizado (é a notificação fixa do MCM).
- **Voz do MCM Avatar:** o MCM usa o mecanismo de voz que já vem no aparelho (no Android, o do Google ou o do fabricante; no Windows, as vozes do Windows). Isso não é uma permissão.

## O que fica guardado no seu aparelho

- **Preferências:** canais, pessoas silenciadas, contas de eventos e as opções da Config (inclusive as do MCM Avatar e as frases que você escreveu para ele).
- **Página Eventos:** os eventos pagos (presentes, bits, Super Chats, inscrições, membros), com o nome de quem mandou, a plataforma e a mensagem. Guarda até 2000 eventos, e você pode apagar um ou todos.
- **Autorização da Twitch:** guardada **criptografada**. No Android ela usa o cofre de chaves do sistema; no Windows, a proteção do seu usuário do Windows.
- **Seu avatar:** se você escolher uma imagem própria para o MCM Avatar, o MCM guarda uma cópia dela na pasta dele. Trocar a imagem apaga a anterior. No Android, o MCM só recebe o arquivo que você escolher na janela do sistema, sem permissão para ver os outros.
- **As mensagens do chat ficam só na memória** (as últimas 200) e somem quando você fecha o MCM.

Onde ficam esses arquivos:
- **Android:** na pasta do app, que outros apps não leem. O backup do Google, se estiver ligado no seu celular, leva só as preferências; a autorização da Twitch, a página Eventos e a imagem do seu avatar ficam de fora.
- **Windows:** em `%LOCALAPPDATA%\MultiStreamChatMonitor`, que só o seu usuário do Windows (e os administradores do PC) conseguem abrir.

## Com quais sites o MCM conversa

Só com as plataformas que você conecta:

- **Twitch** (`twitch.tv`): autorização, chat e as imagens de badges, emotes e avatares;
- **YouTube** (`youtube.com`): a página pública da live e do chat, e as imagens dos avatares e emojis;
- **TikTok** (`tiktok.com`): a página pública da live, o chat e as imagens dos presentes, emotes e avatares. O TikTok exige um código de assinatura dele para abrir o chat. O MCM baixa esse código do próprio site do TikTok, confere se é exatamente o código esperado e o roda isolado, sem acesso aos seus dados. O TikTok entrega ao MCM uma identificação de visitante, que fica só na memória.

E com o **GitHub** (`github.com`), para saber se há versão nova:
- ao abrir, o MCM pergunta ao GitHub qual é a versão mais nova publicada; se houver uma, ele mostra um aviso com o botão para a página de download;
- nessa pergunta não vai nada sobre você, suas contas ou suas lives. O GitHub só vê o endereço de internet do aparelho, como acontece com qualquer site;
- o MCM **nunca baixa nem instala nada sozinho**: quem baixa e instala a versão nova é você.

Os links que aparecem no chat **só abrem se você tocar e confirmar o endereço**. Os botões de ajuda, do YouTube do criador, do LivePix e dos canais dos personagens do MCM Avatar também só abrem se você tocar.

## Overlay no OBS

O overlay é uma pequena página que o próprio MCM serve para o OBS.
- **Windows:** só o próprio PC consegue abrir.
- **Android:** só aparelhos da mesma rede local (Wi-Fi, ponto de acesso ou cabo USB). Pelos dados móveis, ninguém consegue abrir.

Ele mostra só o que já aparece no seu chat, que é público, e não recebe nada de quem o abre.

## MCM Avatar e a voz

O MCM Avatar é um personagem numa página própria do overlay, com as mesmas regras de acesso descritas acima. Ele mostra os eventos que já aparecem no seu chat.

A voz é opcional e vem desligada. Quando você liga:
- ela é feita pelo mecanismo de voz **do próprio aparelho**, e o MCM só usa vozes que funcionam **sem internet**;
- o texto que vira voz (o nome de quem mandou o evento, o evento e, só se você ligar essa opção, o que a pessoa escreveu) fica dentro do aparelho;
- o áudio fica só na memória. No Android, o mecanismo de voz grava um arquivo temporário na pasta do app, que o MCM apaga na hora.

## Copiar diagnóstico

O botão “Copiar diagnóstico” (em Config → Ajuda e diagnóstico) só faz algo quando você toca nele. Ele copia um resumo técnico para a área de transferência, e é você quem decide se manda para alguém. O resumo **não leva** senhas, tokens, cookies nem identificações internas das contas.

## Como apagar seus dados

- **Twitch:** na página Conexão, “Desconectar conta” apaga a autorização do aparelho e pede à Twitch para cancelá-la. Você também pode tirar o acesso no site da Twitch, em Configurações → Conexões.
- **Android:** desinstalar o MCM apaga tudo.
- **Windows:** desinstale o MCM e apague a pasta `%LOCALAPPDATA%\MultiStreamChatMonitor` (o desinstalador do Windows não apaga essa pasta, para você não perder as configurações ao atualizar).

## Como saber se o APK é o oficial

O APK oficial é assinado pela chave do criador. A impressão digital (SHA-256) do certificado é:

`9D:D3:30:AC:32:53:68:67:C9:02:37:E2:AF:DB:50:C2:0A:96:DE:11:07:FB:E7:72:61:B7:84:7D:75:6B:80:51`

Quem quiser conferir pode usar `apksigner verify --print-certs` no APK: o SHA-256 mostrado precisa ser igual a esse. Um APK com outra assinatura não é o oficial.

## Dúvidas

Pergunte nas [Discussões do MCM no GitHub](https://github.com/ElexBR/MultiStream-Chat-Monitor/discussions). Lá tudo é público: não escreva senhas, códigos ou dados pessoais.
