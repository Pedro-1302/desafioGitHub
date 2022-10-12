# Git e GitHub 👨‍💻



## Como tudo começou?



O Git é um sistema distribuído de controle de versões, extremamente seguro e muito utilizado no mundo do desenvolvimento de software. Ele foi concebido pelo mesmo criador do Linux, o engenheiro de software Linus Torvalds, que o criou pois tinha aversões aos sistemas que tentavam fazer as mesmas funções naquela época. 



## Git e Github são a mesma coisa?



A resposta é **não**, ambos são ferramentas diferentes, que possuem funções de se complementarem. O **Git** é uma ferramenta que está mais relacionada ao CLI (Command Line Interface), ou seja, por meio de códigos há a possibilidade de navegação entre branches, de serem feitos novos commits e de diversas outras funções. Já o **Github** possui uma GUI (Graphical User Interface), ou seja, uma interface visual. Além disso o Github se porta como um local para que desenvolvedores de softwares possam armazenar seus repositórios. 



## Por que o Git é tão seguro?



O Git possui muita segurança e isso se deve a como as coisas são feitas dentro dessa ferramenta. A segurança está quase toda relacionada ao **SHA1**, uma função de criptografia Ela se resume em alguns pontos:

+ **Blobs**

  - São os tipos de objetos utilizados para armazenar o conteúdo de cada arquivo de um repositório, ou seja, o bloco básico da composição. Cada Blob possui seu próprio SHA1.

    ![img](https://lh6.googleusercontent.com/ozNMHb3B1G2NqctyF7pY4jRthcR9i8ye6ye-6lQ6aigt6TjmC3QXC_qm12XQwMCsHjRXFFZ5VultD_XY5tohV29N_myTkgBPJl08snlerwDNJ1IrsoyQ5Qw8x2D0rqzwXYdHMIS5YRkAHX1d2B1Y4B46wKHyo4OxRF5mUqGMWHHA0TkSsDYg00ISvw)

    _Exemplo Bloco Blob_

+ **Trees**

  - Armazenam os Blobs, onde podem apontar para Blobs ou para outras Trees, pois existe a possibilidade de diretórios estarem dentro de outros diretórios. Tambem Possuem um SHA1, que muda caso o SHA1 do Blob sejá alterado, uma vez que estão inter-relacionados

    ![img](https://lh5.googleusercontent.com/gyDGR_gIIKtFPprEwV8No42vwGK3uRYsldWylVngTYib4h_OvJ97QaalC2K46eSrvXTvYE4DXBgYKDmZXmt240LNi7llgIAWPjC_GzC8AUMby3-Kwe1mY9dlhZ7JPk8CctoLZC43M64jk_bLo_ikpkGDKo5jkDENjXT3h5qw3sa8B5WEI8fUr126_g) 

    _Exemplo inter-relacionamento entre Trees e Bobs_

+ **Commits**

  - Os Commits apontam para arvores que apontam para Blobs que contem arquivos. Além disso ele também possui seu próprio SHA1. O Commit sempre aponta para os seus parentes, ou seja, aos Commits mais antigos e possuem o nome do autor do Commit, a mensagem de alteração, e o carimbo de tempo da alteração. Seu SHA1 é o Hash de toda a informação.

    

## Os primeiros passos com o Git



#### Chave SSH



Para estabelecer uma conexão entre o Git e o Github existem duas possibilidades: através de uma chave SSH ou de um token de acesso pessoal. A forma mais segura e facilitada de fazer isso é através da Chave SSH, que é uma forma de estabelecer uma conexão segura e encriptada entre duas maquias. Ela se resume ao uso de alguns comandos simples e de alguns passos dentro da plataforma Github. 

> O primeiro passo para estabelecer uma conexão com Chave SSH é acessar as configurações da sua conta, que podem ser encontradas ao clicar no canto superior direito do Github.

![chrome_OAx8KU3XTy](C:\Users\mrcra\Documents\ShareX\Screenshots\2022-10\chrome_OAx8KU3XTy.png)

> Após entrar nas configurações é importante acessar no menu lateral esquerdo a opção "SSH and GPC keys". Depois de entrar nessas configurações é importante cliclar em <span style="color:green">**New SSH key**</span>. 

![chrome_k59wkBjJDZ](C:\Users\mrcra\Documents\ShareX\Screenshots\2022-10\chrome_k59wkBjJDZ.png)

> Então é necessário gerar uma chave SSH a partir do CLI (Git Bash), através dos seguintes comandos:
>
> $ <span style="color:green">**ssh-keygen -t ed25519 -C "aqui vai seu email"**</span>   // Cria sua chave Pública
>
> $ <span style="color:green">**cat id_ed25519.pub   **</span>//Mostra sua chave Publica
>
> $ <span style="color:green">**pwd**</span>   // Mostra o caminho do diretório onde você se encontra
>
> Com esse comando você mostra sua chave Publica que será colocada no Github. Você também possui uma outra chave privada, que é utilizada em outros processos. Após gerar a chave é necessário inseri-la. 

![chrome_GeWFiQG8EW](C:\Users\mrcra\Documents\ShareX\Screenshots\2022-10\chrome_GeWFiQG8EW.png)
