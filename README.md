# MultiStream Chat Monitor (MCM)

O chat das suas lives na **Twitch**, no **YouTube** e no **TikTok** juntos, numa tela só, no **Android** e no **Windows**. É gratuito, sem anúncios e sem cadastro.

## ⬇️ Baixar

| Dispositivo | Arquivo |
|---|---|
| 📱 **Android** (8.0 ou mais novo) | [MultiStream-Chat-Monitor-Android.apk](https://github.com/ElexBR/MultiStream-Chat-Monitor/releases/latest/download/MultiStream-Chat-Monitor-Android.apk) |
| 💻 **Windows** (10 ou 11, 64 bits) | [MultiStream-Chat-Monitor-Windows.msi](https://github.com/ElexBR/MultiStream-Chat-Monitor/releases/latest/download/MultiStream-Chat-Monitor-Windows.msi) |

Esses links sempre baixam a versão mais nova. As versões anteriores e as novidades de cada uma estão em [Versões (Releases)](https://github.com/ElexBR/MultiStream-Chat-Monitor/releases).

## O que o MCM faz

- Junta o chat da **Twitch**, do **YouTube** e do **TikTok** numa lista só, com avatares, badges e emotes.
- **YouTube e TikTok sem conta:** basta digitar o @ do canal. Na **Twitch**, você autoriza na própria página da Twitch, e o MCM só consegue **ler** o chat.
- **Overlay para o OBS:** o chat na tela da live, o MCM Avatar, os alertas, os sons, as metas, o rank, a Maratona e os créditos, cada um numa fonte ou todos juntos numa **🎬 Cena MCM**, com um endereço só.
- **Alertas** (seguidores, inscrições, membros, presentes, bits, Super Chats, gorjetas, raids) numa área própria, um por vez, com som, voz, **variações pelo valor** e o **Overlay de Alertas** para o OBS, e uma página que guarda todos.
- **StreamElements:** os seguidores da Twitch, os inscritos novos do YouTube e as gorjetas (LivePix e outras) chegam ao MCM.
- Silenciar pessoas, esconder comandos com “!” e o **💎 Filtro de Chat VIP**, que mostra só inscritos, moderadores, VIPs, fã-clube ou apoiadores.
- **Tocar numa mensagem** para o MCM Avatar ou a voz do aparelho ler ela em voz alta.
- **MCM Avatar:** um personagem no OBS que comemora e fala os eventos num balão, com voz se você quiser. Dá para usar um personagem seu: veja [como fazer a folha do seu avatar](avatar/README.md), com o modelo para baixar.
- **Pontos e rank** para quem participa da live (por mensagem, presença, papel e apoios), com importação da pontuação do Mix It Up, e **temporadas com prêmios** para o Top 10.
- **Comandos** como `!pontos`, `!lurk`, `!ler` e os seus, com som e resposta falada pelo MCM Avatar ou pela voz do aparelho, e/ou escrita no chat do app e no overlay do chat (o MCM nunca escreve no chat da plataforma). E mais os **Áudios**, para os memes, e os **Timers**, com avisos durante a live.
- **Créditos** para o OBS, com os apoiadores, o Top 10 e quem comentou, arrumados do seu jeito na 🎬 Cena MCM.
- **📊 Metas**, **Overlay do Rank** e **⏱️ Maratona MCM** (subathon) para o OBS, que também podem aparecer na página Chat.
- **🪟 Chat sobre o jogo** (Windows): o chat numa janela transparente por cima do jogo, para quem tem um monitor só.
- **Testes sem live:** mensagens e eventos de mentira para ver tudo funcionando antes de entrar ao vivo.
- **📦 Backup, Exportar e Importar:** leve a configuração para outro aparelho, e o **🕒 backup automático** guarda cópias numa pasta sua.
- Escolha de fonte, tamanho, direção e **estilo** do chat (Bolhas MCM, Bolhas Compactas MCM ou Compacto YouTube).
- Continua funcionando com o app minimizado.

Dentro do app, o ❓ da página Chat abre o guia “Como usar”.

## 📱 Instalar no Android

1. Baixe o `.apk` pelo navegador do celular.
2. Abra o arquivo. Se o Android pedir, permita **instalar apps desta fonte** (ele leva você à configuração; depois é só voltar).
3. Se aparecer um aviso do Google Play Protect dizendo que o app é desconhecido, toque em **Mais detalhes → Instalar mesmo assim**. O aviso aparece porque o MCM não está na Play Store, não porque tenha algo errado.
4. **Atualizar:** baixe o `.apk` novo e instale por cima. Canais, conta e configurações continuam.

## 💻 Instalar no Windows

1. Baixe o `.msi` e abra.
2. Se aparecer **“O Windows protegeu o computador”**, clique em **Mais informações → Executar assim mesmo**. O aviso aparece porque o instalador não tem um certificado pago, não porque tenha algo errado.
3. Siga o instalador. O MCM aparece no menu Iniciar e na Área de Trabalho.
4. **Atualizar:** abra o `.msi` novo; ele substitui a versão antiga e mantém as suas configurações.

O próprio MCM avisa quando sai uma versão nova.

## 🔍 Como saber se o arquivo é o oficial

Baixe só por esta página. Para conferir o arquivo, compare o código **SHA-256** dele com o que está publicado nas notas da versão (em [Versões](https://github.com/ElexBR/MultiStream-Chat-Monitor/releases)).

No Windows, abra o PowerShell na pasta do arquivo e digite:

```powershell
Get-FileHash .\MultiStream-Chat-Monitor-Windows.msi
```

O código que aparece em `Hash` precisa ser igual ao publicado. Dá para conferir o `.apk` do mesmo jeito, trocando o nome do arquivo.

O APK oficial também é sempre assinado pela mesma chave. Quem conhece as ferramentas do Android pode conferir com `apksigner verify --print-certs`: o SHA-256 do certificado precisa ser este:

`9D:D3:30:AC:32:53:68:67:C9:02:37:E2:AF:DB:50:C2:0A:96:DE:11:07:FB:E7:72:61:B7:84:7D:75:6B:80:51`

## 🔒 Privacidade

O MCM não tem conta, servidor próprio, anúncios nem rastreamento, e tudo o que ele guarda fica no seu aparelho. Os detalhes estão em [PRIVACIDADE.md](PRIVACIDADE.md).

## 🆘 Ajuda e sugestões

- **Dúvidas e sugestões:** [Discussões](https://github.com/ElexBR/MultiStream-Chat-Monitor/discussions).
- **Algo não funcionou:** [relate um problema](https://github.com/ElexBR/MultiStream-Chat-Monitor/issues/new/choose). Antes, toque em **Config → Ajuda e diagnóstico → Copiar diagnóstico** no MCM e cole o texto no relato.

Para escrever, é preciso uma conta no GitHub (gratuita). Tudo o que se escreve aqui é público: nunca coloque senhas, códigos ou dados pessoais.

## 🎨 Créditos

- Ícones da gorjeta (o cofrinho e as notas): [Piggy bank icons created by Magnific - Flaticon](https://www.flaticon.com/free-icons/piggy-bank "piggy bank icons") e [Business and finance icons created by Magnific - Flaticon](https://www.flaticon.com/free-icons/business-and-finance "business and finance icons").

## 💚 Apoie

O MCM é gratuito e sempre vai ser. Se ele ajuda nas suas lives, veja como apoiar em [APOIE.md](APOIE.md).

---

Feito por **ElexBR** · [youtube.com/@elexbrCanal](https://www.youtube.com/@elexbrCanal)
