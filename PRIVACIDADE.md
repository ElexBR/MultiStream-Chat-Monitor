# Privacidade do MultiStream Chat Monitor (MCM)

O MCM é um app gratuito, para Android e Windows, que junta num lugar só o chat das suas lives na Twitch, no YouTube e no TikTok. Este documento diz, em linguagem simples, o que o MCM pede, o que ele guarda e com quem ele conversa.

**Resumo:** o MCM não tem conta, não tem servidor próprio, não tem anúncios e não coleta nada sobre você. Tudo o que ele guarda fica no seu aparelho.

## O que o MCM não faz

- Não pede cadastro nem conta do MCM.
- Não manda nada para servidores do criador do MCM. Esses servidores não existem.
- Não tem anúncios, estatísticas de uso ou rastreamento.
- Não grava registros (logs) do que você faz.
- Nunca vê a sua senha da Twitch, do YouTube ou do TikTok.
- Não lê seus arquivos, fotos, contatos, câmera, microfone ou localização. As únicas exceções são os arquivos e a pasta que você mesmo escolher: a imagem do seu avatar, a pontuação que você importar de outro programa, os sons que você escolher para os comandos e os alertas, as imagens e vídeos dos alertas, o arquivo do 📦 Exportar e a pasta do 🕒 Backup automático (veja “O que fica guardado” e “📦 Backup, Exportar e Importar”).
- Não escreve no chat da Twitch, do YouTube nem do TikTok. Os comandos (`!pontos`, `!lurk` e os que você criar) e os timers respondem só no seu OBS e no aparelho: pelo MCM Avatar, pela voz do aparelho, com os sons que você escolher e, se você quiser, como uma mensagem do “MCM” no chat do app e no overlay do chat.

## O que o MCM pede

- **Twitch:** uma autorização feita na própria página da Twitch, com um código. Ela dá ao MCM só a permissão de **ler o chat** (`user:read:chat`). O MCM não consegue mandar mensagens, moderar nem mexer na sua conta.
- **YouTube e TikTok:** nada. O MCM lê o chat público da live, como qualquer pessoa que abre a página, sem conta e sem login.
- **StreamElements** (opcional, em 🔗 Integrações): o **Overlay Token** de cada canal, que você copia do painel do StreamElements e cola no MCM. É o código mais limitado do StreamElements, feito para os alertas: com ele, o MCM só recebe os alertas do canal. O MCM nunca pede o JWT Token, que abre a conta inteira.
- **Permissões no Android:**
  - **Internet**, para ler os chats;
  - **serviço em primeiro plano e notificações**, para os chats continuarem ligados com o app minimizado (é a notificação fixa do MCM).
- **Voz do MCM Avatar e 🎙️ Voz (TTS):** o MCM usa o mecanismo de voz que já vem no aparelho (no Android, o do Google ou o do fabricante; no Windows, as vozes do Windows). Isso não é uma permissão.

## O que fica guardado no seu aparelho

- **Preferências:** canais, pessoas silenciadas e as opções da Config (inclusive as do MCM Avatar, as frases dos alertas, os comandos, os áudios, os timers, as metas, a Maratona, as cenas, o estilo do chat, o 💎 Filtro de Chat VIP, o 🪟 Chat sobre o jogo e, no 🕒 Backup automático, a pasta escolhida e a data do último backup).
- **Página Eventos:** os eventos (presentes, bits, Super Chats, gorjetas, inscrições, membros, seguidores, raids e compartilhamentos), com o nome de quem mandou, a plataforma e a mensagem. Guarda até 2000 eventos, e você pode apagar um ou todos.
  - Em cada sessão, também **quem comentou** (o nome, a plataforma e quantas mensagens a pessoa mandou). Só a sessão mais nova guarda os nomes; as antigas guardam só quantas pessoas foram.
  - E o código das lives que aconteceram na sessão, que o MCM usa para começar uma sessão nova sozinho quando outra live começa.
- **Pontos** (só se você ligar): de cada pessoa que participou, a plataforma, a identificação dela na plataforma, o nome, o endereço da foto de perfil, os pontos e quantas mensagens ela mandou na temporada. Também a lista de quem você tirou dos pontos e as 5 últimas temporadas que terminaram: o Top 10 de cada uma (com os mesmos dados), o prêmio de cada posição e o que já foi distribuído ou entregue.
  - **Importar pontuação:** o arquivo que você escolher (por exemplo, o do Mix It Up) é lido só no aparelho e **nunca é guardado nem enviado**. O MCM guarda só uma “impressão digital” dele (SHA-256), para avisar se você importar o mesmo arquivo de novo.
  - A lista de bots conhecidos (que nunca ganham pontos) vem pronta dentro do MCM.
- **Lista 👑 Apoiadores:** o nome, a plataforma e a identificação de quem apoiou ou de quem você adicionou, e a lista anterior (a de antes da última vez que ela foi zerada).
- **Sons dos comandos e dos alertas, e imagens dos alertas:** o MCM guarda só o nome e onde está cada arquivo (som em MP3 ou WAV; imagem ou vídeo em PNG, GIF, WebP ou WebM) que você escolher, nunca uma cópia, e lê o arquivo na hora de tocar ou de mostrar. No Android, ele recebe só a permissão de ler de novo os arquivos que você escolheu, sem ver os outros.
- **📊 Metas e ⏱️ Maratona MCM:** só números (quanto cada meta já contou, por plataforma, e o tempo da Maratona), sem nomes de ninguém.
- **Autorização da Twitch e códigos das 🔗 Integrações** (o Overlay Token do StreamElements): guardados **criptografados**. No Android eles usam o cofre de chaves do sistema; no Windows, a proteção do seu usuário do Windows. Nunca aparecem no diagnóstico nem vão no arquivo do 📦 Exportar.
- **Seu avatar:** se você escolher uma imagem própria para o MCM Avatar, o MCM guarda uma cópia dela na pasta dele. Trocar a imagem apaga a anterior. No Android, o MCM só recebe o arquivo que você escolher na janela do sistema, sem permissão para ver os outros.
- **As mensagens do chat ficam só na memória** (as últimas 200) e somem quando você fecha o MCM.

Onde ficam esses arquivos:
- **Android:** na pasta do app, que outros apps não leem. O backup do Google, se estiver ligado no seu celular, leva só as preferências e os números das metas e da Maratona; a autorização da Twitch, os códigos das 🔗 Integrações, a página Eventos, os pontos, a lista de apoiadores e a imagem do seu avatar ficam de fora.
- **Windows:** em `%LOCALAPPDATA%\MultiStreamChatMonitor`, que só o seu usuário do Windows (e os administradores do PC) conseguem abrir.

## 📦 Backup, Exportar e Importar

O MCM só cria o arquivo quando você toca em Exportar, e ele fica onde você escolher salvar. Ele leva só as partes que você marcar; os pontos, os apoiadores, os silenciados e a página Eventos têm nomes e identificações de pessoas do chat. Nunca vão nele a autorização da Twitch, os códigos das 🔗 Integrações nem a voz. O MCM não manda esse arquivo para lugar nenhum, e importar lê o arquivo só no aparelho.

O **🕒 Backup automático** vem desligado. Quando você escolhe uma pasta e quando fazer:
- o MCM grava nela, sozinho, o mesmo arquivo do Exportar com todas as partes (com os nomes do chat e a imagem do seu avatar, e sem a autorização da Twitch, os códigos e a voz);
- ele guarda os 10 backups mais novos e apaga só os mais antigos dele (os arquivos `MCM-backup-…`), nunca outro arquivo da pasta;
- no Android, a pasta é escolhida na janela do próprio sistema, e o MCM recebe só a permissão de gravar nela, sem ver as outras pastas;
- se a pasta for sincronizada com uma nuvem (OneDrive, Google Drive…), os backups vão junto para ela pelo serviço que você usa. O MCM não manda nada para a internet.

## Com quais sites o MCM conversa

Só com as plataformas e os serviços que você conecta:

- **Twitch** (`twitch.tv`): autorização, chat e as imagens de badges, emotes e avatares. Com o chat conectado, o MCM também pergunta à Twitch, uma vez por minuto, se a sua live está no ar (os pontos só contam com a live no ar);
- **YouTube** (`youtube.com`): a página pública da live e do chat, e as imagens dos avatares e emojis;
- **TikTok** (`tiktok.com`): a página pública da live, o chat e as imagens dos presentes, emotes e avatares. O TikTok exige um código de assinatura dele para abrir o chat. O MCM baixa esse código do próprio site do TikTok, confere se é exatamente o código esperado e o roda isolado, sem acesso aos seus dados. O TikTok entrega ao MCM uma identificação de visitante, que fica só na memória;
- **StreamElements** (`streamelements.com`), só com um canal vinculado em 🔗 Integrações: o MCM se conecta com o Overlay Token e recebe as atividades do canal, mas só usa os seguidores da Twitch, os inscritos novos do YouTube e as gorjetas (como as do LivePix), com o nome de quem mandou, o valor e a mensagem; o resto é descartado na hora. O MCM não manda nada seu para o StreamElements além do código.

Com o **Frankfurter** (`frankfurter.dev`), um serviço gratuito de cotação de moedas, só se os pontos estiverem ligados com “Converter Super Chats de outras moedas para reais” e chegar um Super Chat em outra moeda:
- o MCM manda **só o código da moeda** (por exemplo, `USD`), nunca quem mandou nem o valor;
- pergunta no máximo uma vez a cada 12 horas por moeda.

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

O **overlay de som** é mais uma página do overlay, com as mesmas regras de acesso. Ela toca os sons que você mandou para o OBS; o som que está tocando fica só na memória do MCM.

O **Overlay de Alertas**, as **📊 Metas**, o **Overlay do Rank** (o Top da temporada, com os pontos) e a **⏱️ Maratona MCM** são mais páginas do overlay, com as mesmas regras de acesso. O Overlay de Alertas mostra a imagem que você escolheu (ou a foto de quem mandou) e o alerta que já chegou ao MCM. A **🎬 Cena MCM** é uma página que junta essas mesmas páginas num endereço só, sem nada a mais.

Os **créditos** (a cena 🎞️ Créditos da 🎬 Cena MCM) são mais uma página do overlay, com as mesmas regras de acesso. Ela mostra os nomes da lista de apoiadores, o Top 10 dos pontos da temporada (com os pontos) e quem comentou na sessão: nomes que já apareceram no seu chat. As fontes vêm de dentro do MCM, sem baixar nada de outro site.

## MCM Avatar e a voz

O MCM Avatar é um personagem numa página própria do overlay, com as mesmas regras de acesso descritas acima. Ele mostra os alertas que já chegaram ao MCM.

A voz é opcional e vem desligada. Quando você liga:
- ela é feita pelo mecanismo de voz **do próprio aparelho**, e o MCM só usa vozes que funcionam **sem internet**;
- o texto que vira voz (o nome de quem mandou o alerta, o alerta, as respostas dos comandos, os timers, o que a ação 🎙️ Voz (TTS) fala e o que a pessoa escreveu, este só se você ligar o 🎙️ TTS com a mensagem no grupo de alertas, o comando !ler ou um comando com {mensagem}, ou tocar numa mensagem para ela ser lida) fica dentro do aparelho;
- o áudio fica só na memória. No Android, o mecanismo de voz grava um arquivo temporário na pasta do app, que o MCM apaga na hora.

## 🪟 Chat sobre o jogo (Windows)

Com o 🪟 Chat sobre o jogo ligado, o MCM registra no Windows só os dois atalhos escolhidos (no começo, Ctrl+Shift+M e Ctrl+Shift+L), para eles funcionarem com o jogo na frente. O MCM não lê nenhuma outra tecla. Com “Esconder da live” ligado, o próprio Windows deixa a janela do chat fora das capturas de tela.

## Copiar diagnóstico

O botão “Copiar diagnóstico” (em Config → Ajuda e diagnóstico) só faz algo quando você toca nele. Ele copia um resumo técnico para a área de transferência, e é você quem decide se manda para alguém. O resumo **não leva** senhas, tokens, cookies nem identificações internas das contas. Ele também lista os últimos problemas do próprio MCM (voz, gravação de arquivos, avatar, cotação, sons, imagens dos alertas, fila e backup automático), sem nomes nem dados de ninguém.

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
