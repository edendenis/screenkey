# Como configurar/instalar/usar o `screenkey` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `screenkey` no `Linux Ubuntu`.

## _Abstract_

_In this document are contained the main commands and settings to set up/install the `screenkey` on `Linux Ubuntu`._


## Revisão(ões)/Versão(ões)

| Revisão número | Data da revisão | Descrição da revisão                                    | Autor da revisão                                |
|:--------------:|:---------------:|:--------------------------------------------------------|:------------------------------------------------|
| 0              | 06/03/2024      | <ul><li>Revisão inicial/criação do documento.</li></ul> | <ul><li>Eden Denis F. da S. L. Santos</ul></li> |


## Controle de configuração/instalação nos Sistemas Operacionais (SO) vs. Computador

| Numero | Computador          | Sistema Operacional (SO) | Tipo de sistema | Status da configuração/instalação |
|:------:|:-------------------:|:------------------------:|:---------------:|:---------------------------------:|
| 1      | Dell Precision 7520 | Kali Linux               | Debian          | OK                                |
| 2      | Dell Precision 7520 | Linux Ubuntu             | Ubuntu          | Pendente                          |
| 3      | Dell Precision 7520 | Linux Xubuntu            | Ubuntu          | Pendente                          |
| 4      | Dell Precision 7520 | Windows 10               | Windows         | OK                                |
| 5      | Asus                | Kali Linux               | Debian          | Pendente                          |
| 6      | Asus                | Linux Ubuntu             | Ubuntu          | Pendente                          |
| 7      | Asus                | Linux Xubuntu            | Ubuntu          | OK                                |
| 8      | Asus                | Windows 10               | Windows         | Pendente                          |

### Legenda

- **N/A:** **NOT** apllicable/**NÃO** aplicável
- **OK:** Zero killed

## Descrição [2]

### `screenkey`

O `screenkey` é uma ferramenta de código aberto para sistemas Linux que exibe as teclas pressionadas no momento em uma sobreposição na tela, funcionando como uma ajuda visual especialmente útil em apresentações, tutoriais em vídeo ou durante sessões de compartilhamento de tela, onde é importante mostrar aos espectadores quais comandos estão sendo digitados. Depois de ser iniciado, o screenkey captura a entrada do teclado e a exibe de forma discreta e legível, permitindo personalizar aspectos como posição na tela, duração da exibição, fontes, cores e transparência. Isso ajuda a tornar demonstrações ou tutoriais mais compreensíveis, garantindo que os espectadores possam acompanhar comandos específicos ou sequências de teclas sem perder o contexto da tela principal que está sendo compartilhada.


## 1. Como configurar/instalar/usar o `screenkey` no `Linux Ubuntu` [1]

Para configurar/instalar/usar o `screenkey` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes APT. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo APT e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update -y`

    2.5 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.6 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update -y`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`

    2.7 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.8 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

## 1.2 Usar o `screenkey`

1. **Instale o screenkey utilizando o gerenciador de pacotes apt:** `sudo apt install screenkey -y`

    Após a instalação, você pode iniciar o `screenkey` diretamente do terminal digitando `screenkey` ou procurando por ele no menu de aplicativos.

    O screenkey é uma ferramenta útil para demonstrações ou gravações de tela, pois exibe as teclas pressionadas em tempo real, facilitando o entendimento de comandos e atalhos utilizados durante a sessão. Se desejar personalizar as configurações, como posição, tamanho e duração da exibição das teclas, você pode acessar as opções através de um menu de configuração ou via linha de comando.

Lembre-se de que, dependendo da versão do seu Ubuntu e dos repositórios disponíveis, pode ser necessário adicionar um repositório específico ou baixar o screenkey de outra fonte. No entanto, na maioria das versões recentes do Ubuntu, o comando acima deve funcionar sem problemas.

### 1.3 Configurar o tamanho da letra no `screenkey`

No `screenkey`, o tamanho da fonte não é definido por um valor numérico específico, mas sim por categorias relativas: `'large'` (grande), `'medium'` (médio) ou `'small'` (pequeno). Para configurar o tamanho da letra, você deve utilizar a opção `-s` ou `--font-size` seguida de uma dessas palavras-chave. Aqui está como você pode fazer isso:

1. **Para definir o tamanho da fonte como grande, use:** `screenkey -s large`

2. **Para um tamanho médio:** `screenkey -s medium`

3. **E para um tamanho pequeno:** `screenkey -s small`

Portanto, escolha o tamanho conforme sua necessidade e inicie o `screenkey` com o comando correspondente.

### 1.4 Para ajustar a transparência da cor de fundo no `screenkey`

Para ajustar a transparência da cor de fundo no screenkey, você pode usar a opção `--opacity` quando iniciar o aplicativo. O valor de opacidade pode variar de 0.0 (completamente transparente) a 1.0 (completamente opaco).

1. Por exemplo, se você deseja definir a opacidade para um valor intermediário, como 0.5, você usaria o seguinte comando: `screenkey --opacity 0.5`

    Isso iniciará o `screenkey` com a faixa de fundo tendo uma transparência média. Ajuste o valor conforme a necessidade de transparência que você deseja. Quanto menor o número, mais transparente será a faixa.

2. Lembre-se de que essa configuração será aplicada juntamente com qualquer outra configuração que você definir, então se você também quiser definir o tamanho da fonte ao mesmo tempo, por exemplo, você pode combinar os argumentos: `screenkey -s small --opacity 0.5`

Este comando iniciará o screenkey com fonte grande e uma transparência de 50% no fundo.

## 1.5 Personalizar a cor da fonte no `screenkey`

No `screenkey`, você não tem uma lista específica de tons de amarelo pré-definidos para escolher diretamente através de argumentos de linha de comando. No entanto, você pode especificar a cor usando nomes de cores básicos ou utilizando códigos de cores hexadecimais (HTML color codes).

1. Para o amarelo básico, você simplesmente usaria: `screenkey --font-color yellow`

2. Para um tom de amarelo dourado, você poderia usar: `screenkey --font-color '#FFD700'`

Você pode encontrar diversos tons de amarelo com seus respectivos códigos hexadecimais em recursos online ou ferramentas de design gráfico. Esses códigos começam sempre com uma cerquilha (#) seguida por seis caracteres (números e letras de A a F) que definem a intensidade das cores vermelha, verde e azul no sistema RGB.

Lembrando que essas cores podem variar um pouco dependendo do monitor e do ambiente de exibição, mas o uso de códigos hexadecimais permite uma escolha muito mais ampla e precisa de cores em comparação com os nomes de cores básicos.

### 1.6 Usar o padrão adotado

1. Para (a) um tamanho de letra pequena, uma transparÊncia pela metade e para um tom de amarelo dourado, você poderia usar: `screenkey --mouse -s small --opacity 0.5 --font-color '#FFD700'`


## 2. Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `screenkey` no `Linux Ubuntu`sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean
    sudo apt autoclean
    sudo apt autoremove
    sudo apt update -y
    sudo apt autoclean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install screenkey -y
    screenkey -s small --opacity 0.5 --font-color '#FFD700'
    ```


## Referências

[3] OPENAI. ***Instale o screenkey Ubuntu.*** Disponível em: <https://chat.openai.com/c/58aa3f5f-c2cb-4a22-9f2b-11c4554c32a7> (texto adaptado). Acessado em: 06/03/2024 13:47.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 06/03/2024 13:48.


