# Seu próprio avatar no MCM

Além dos quatro personagens que vêm no MultiStream Chat Monitor (Elex, Dready, Demaciana e Anna), você pode usar um personagem seu no **MCM Avatar**: o personagem que fica no OBS e comemora e fala os eventos da live.

No app: **Config → 🧑‍🎤 MCM Avatar → Seu avatar → Escolher arquivo**. O MCM confere a imagem na hora e diz o que precisa acertar.

## ⬇️ Modelo

[**modelo-folha-avatar.png**](modelo-folha-avatar.png) (1536 × 1280): a grade pronta, com o nome de cada linha, a margem e o chão. O mesmo modelo também pode ser baixado dentro do app.

Coloque o modelo numa **camada de fundo**, desenhe por cima e **esconda a camada do modelo antes de exportar**.

## As regras da folha

O avatar é uma **folha de sprites**: uma imagem só, **PNG ou WebP**, com **fundo transparente**, dividida numa grade de **casas quadradas**.

**5 linhas**, de cima para baixo:

| Linha | Animação | |
|---|---|---|
| 1 | Parado (repete o tempo todo) | **obrigatória** |
| 2 | Falando (repete enquanto o balão está na tela) | **obrigatória** |
| 3 | Comemorando (uma vez, no começo de cada evento) | opcional |
| 4 | Entrando | opcional |
| 5 | Saindo | opcional |

Sem as linhas 3, 4 e 5, o avatar não comemora e aparece e some aos poucos.

- **Quadros:** até **6 por linha** é o recomendado (pode ter até 12), um por casa, da esquerda para a direita. Quadros vazios no fim da linha são ignorados. A animação roda a **8 quadros por segundo** (6 quadros = 0,75 s).
- **Casas:** quadradas, todas do mesmo tamanho, **de 16 a 512 px**. A altura da imagem dividida por 5 é o tamanho da casa, e a largura precisa ser um número inteiro de casas. Exemplo: casas de 256 px com 6 quadros por linha = imagem de **1536 × 1280**.
- **O personagem:**
  - **olhando para a direita** (o MCM espelha quando ele olha para a esquerda);
  - **do mesmo tamanho em todas as linhas**;
  - com os **pés na mesma altura** (a linha do chão do modelo);
  - com uma **margem** dentro de cada casa: nada pode encostar na borda nem passar para a casa vizinha.
- **Arquivo:** até **20 MB**.
- **Pixel art:** com casas pequenas (até 128 px), a opção **“Arte pixelada”** já vem marcada e o desenho aumenta sem borrar.

Nas linhas parado e falando, o MCM ainda corrige sozinho pequenas diferenças na posição dos pés entre um quadro e outro.

## O que o MCM guarda

O MCM guarda uma cópia da imagem na pasta dele, no seu aparelho (fora do backup do Google). Trocar a imagem apaga a anterior. Mais detalhes em [PRIVACIDADE.md](../PRIVACIDADE.md).
