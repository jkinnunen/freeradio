# FreeRadio — Complemento para o NVDA

FreeRadio é um complemento de rádio pela Internet para o leitor de ecrã NVDA. O seu principal objetivo é dar aos utilizadores acesso fácil a milhares de estações de rádio online. Toda a interface e todas as funcionalidades foram concebidas com total acessibilidade para o NVDA.

## Diretório Radio Browser

FreeRadio utiliza a base de dados aberta Radio Browser para o seu catálogo de estações. O Radio Browser é um diretório gratuito gerido pela comunidade com mais de 50.000 estações de rádio online de todo o mundo. Não é necessário registo e a API é aberta a todos.

Cada estação inclui endereço, país, género, idioma e bitrate; as estações são classificadas por votos dos utilizadores. O FreeRadio liga-se à API através de servidores espelho localizados na Alemanha, Países Baixos e Áustria; se um servidor estiver inacessível, muda automaticamente para o seguinte.

## Requisitos

- NVDA 2024.1 ou posterior
- Windows 10 ou posterior
- Ligação à Internet

## Instalação

Descarregue o ficheiro `.nvda-addon`, prima Enter sobre ele e reinicie o NVDA quando solicitado.

## Atalhos de Teclado

Todos os atalhos podem ser reatribuídos em Menu NVDA → Preferências → Definir comandos → FreeRadio.

- Ctrl+Win+R: abrir navegador de estações
- Ctrl+Win+P: pausar / retomar
- Ctrl+Win+S: parar
- Ctrl+Win+→: próximo favorito
- Ctrl+Win+←: favorito anterior
- Ctrl+Win+↑: aumentar volume
- Ctrl+Win+↓: diminuir volume
- Ctrl+Win+V: adicionar aos favoritos
- Ctrl+Win+I: informação da estação
- Ctrl+Win+M: espelho de áudio
- Ctrl+Win+E: gravação instantânea
- Ctrl+Win+W: abrir pasta de gravações

## Navegador de Estações

A janela aberta com Ctrl+Win+R contém cinco separadores:
- Todas as Estações
- Favoritos
- Gravação
- Temporizador
- Músicas Gostadas

Pode navegar entre separadores com Ctrl+Tab.

Quando o separador Todas as Estações abre, as 1.000 estações mais votadas são carregadas automaticamente a partir do Radio Browser. O campo de pesquisa permite filtrar imediatamente a lista carregada; Enter ou o botão Pesquisar executam uma pesquisa completa na base de dados.

Na parte inferior da janela existem:
- Dispositivo de saída
- Volume (0–200)
- Efeitos
- Botão Reproduzir/Pausar

O botão Detalhes da Estação mostra país, idioma, género, formato, bitrate, website e URL da transmissão.

## Favoritos

A lista de favoritos é uma coleção pessoal guardada permanentemente.

- Alt+V adiciona ou remove favoritos
- Ctrl+Win+→ e Ctrl+Win+← navegam pelos favoritos mesmo com a janela fechada

### Reordenar favoritos

Prima X sobre uma estação para entrar no modo de mover. Use as setas para escolher a nova posição e prima X novamente para confirmar.

### Adicionar estação personalizada

O botão Adicionar Estação Personalizada permite inserir nome da estação e URL da transmissão diretamente nos favoritos.

## Reconhecimento Musical

Premir Ctrl+Win+I três vezes ativa o reconhecimento musical baseado em Shazam quando não existem metadados ICY disponíveis.

Se o reconhecimento for bem-sucedido:
- título
- artista
- álbum
- ano de lançamento

são anunciados pelo NVDA e copiados automaticamente para a área de transferência.

É necessário `ffmpeg.exe`.

## Espelho de Áudio

Ctrl+Win+M duplica a transmissão atual para um segundo dispositivo de saída de áudio.

Exemplos:
- colunas + auscultadores
- gravação externa
- multi-divisão
- monitorização remota

Disponível apenas com o backend BASS.

## Gravação

As gravações são guardadas por predefinição em:

Documents\FreeRadio Recordings\

### Gravação instantânea

Ctrl+Win+E inicia e para a gravação sem interromper a reprodução.

### Gravação agendada

No separador Gravação:
- selecionar estação dos favoritos
- definir hora HH:MM
- definir duração em minutos

Modos:
- Gravar enquanto ouve
- Apenas gravar

## Temporizador

Existem dois tipos:

### Alarme — iniciar rádio

Inicia automaticamente uma estação favorita à hora definida.

### Suspensão — parar rádio

Reduz gradualmente o volume durante 60 segundos e para a reprodução.

## Definições

Principais opções:

- dispositivo de saída de áudio
- volume inicial
- efeito de áudio predefinido
- retomar última estação ao iniciar o NVDA
- anunciar automaticamente mudanças de faixa
- guardar músicas gostadas em ficheiro de texto
- comportamento de Ctrl+Win+P
- caminho do ffmpeg.exe
- caminho do VLC
- caminho do Windows Media Player
- caminho do PotPlayer
- pasta de gravações

## Músicas Gostadas

Quando ativado, o conteúdo copiado com Ctrl+Win+I é também guardado em:

Documents\FreeRadio Recordings\likedSongs.txt

## Separador Músicas Gostadas

Mostra todas as faixas guardadas em likedSongs.txt.

Ações disponíveis:
- Reproduzir no Spotify
- Reproduzir no YouTube (Alt+O)
- Remover (Alt+M)
- Atualizar (Alt+E)

## Reprodução

Ordem de prioridade dos backends:

1. BASS — backend principal e predefinido
2. VLC
3. PotPlayer
4. Windows Media Player

O BASS aparece no misturador de volume do Windows como uma fonte de áudio independente, separada do NVDA.

## Licença

GPL v2
