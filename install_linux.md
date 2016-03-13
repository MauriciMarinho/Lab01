```sh
ARQUIVO CRIADO E ORGANIZADO POR:
MAURICI ELOU MARINHO
RA: B98GBE-8
TURMA: CC5Q41
```
&nbsp;
&nbsp;
---
# INSTALANDO E CONFIGURANDO MAQUINA VIRTUAL COM SLITAZ/LINUX 5.0 RC-3
&nbsp;

    Este arquivo irá lhe guiar na instalação de uma máquina virtual (hospedeira), configuração e instalação do Sistema Operacional Slitaz/Linux 5.0 RC-3.
    Os passos a ser seguidos serão:

  **1 - Download do S.O. Slitaz/Linux 5.0 RC-3**
  
  **2 - Criação a Máquina Virtual**
  
 **3 - Configuração da Máquina Virtual**
 
 **4 -  Instalação do S.O. Slitaz/Linux 5.0 RC-3**
 
  ---
## 1 - Download do S.O. Slitaz/Linux 5.0 RC-3

Faça o *download* do Slitaz 5.0 RC-3 no site http://www.slitaz.org/pt/news/ e armazene o arquivo *.ISO* em um diretório de fácil acesso.

&nbsp;

---
## 2 - Criação da Máquina Virtual
    
Para a *virtualização* iremos utilizar o software da Oracle, o **"VirtualBox"**, que pode ser encontrado no site https://www.virtualbox.org/wiki/Downloads.
   
Após a instalação, a interface principal do VirtualBox se abrirá.
   
 Primeiramente, devemos criar o ambiente virtual (o qual receberá o sistema operacional virtual). 
 
 - Clique no botão ***NOVO***
 
Na tela que será aberta, dê um nome à VM e escolha a plataforma e o sistema operacional:
* Em TIPO selecione: ***LINUX***
* Em Versão selecione: ***Other Linux 32bits***

Depois de escolher o sistema e dar um nome, clique em ***PRÓXIMO***:

Nesta tela, defina a quantidade de memória RAM da *VM* que será de 512 Mb ou superior.

* Clique em ***PRÓXIMO***.

Na sequência, marque a opção **"Criar um disco virtual agora"** e clique em ***CRIAR***.

Na tela seguinte, selecione o item **VDI( VirtualBox Disc Image)** e clique em ***PRÓXIMO***.

Agora teremos que decidir o tipo de armazenamento  do HD virtual. Para esta aplicação iremos utilizar o ítem **"Dinamicamente Alocado"**. Após escolher o tipo, clique em ***PRÓXIMO***

Agora, selecione o tamanho para o HD que será de  *60Gb* e clique em ***CRIAR***.

Ao término, você verá a VM que acabou de criar na tela do VirtualBox.



&nbsp;

---

## 3 - Configuração da Máquina Virtual

* Clique no botão **Configurações** na tela principal do VirtualBox.

> Nesta área você poderá realizar as configurações que julgar necessárias para o funcionamento da sua VM.

> Não entrarei em detalhes acerca de cada opção, apenas informarei as configurações para o nosso caso.

Na guia ***SISTEMA***, defina a ordem de *BOOT* colocando:

- 1° CDROM
- 2° HardDisk

Na guia ***ARMAZENAMENTO***, clique em cima do ícone do *cdrom* e no canto direito selecione o local da  imagem (.ISO) do SLITAZ 5.0 RC-3 que você efetuou o *download*.

Clique em **OK**, e de volta na tela principal do VirtualBox, clique em ***INICIAR***.


>A *distro* Slitaz 5.0 RC-3 é pequena e leve. Este arquivo é um *LIVECD*, ou seja, roda diretamente do CDROM, sendo assim, será necessária a instalação do Slitaz dentro da nossa VM. Veremos isso a seguir.

&nbsp;

---

## 4 - Instalação do S.O. Slitaz/Linux 5.0 RC-3

Com a VM iniciada e o Slitaz operando, abra no menu **APLICATIVOS**, o submenu **Sistema/Instalador do Slitaz**.

Será aberto um arquivo ***DOCUMENTAÇÂO***, onde nele contém todas as informações para a instalação do Slitaz.

> Para a instalação do Slitaz, é necessário que seja criada uma partição para que o sistema possa ser instalado.

Role o arquivo até o botão ***"EXECUTE GPARTED"***.

Será aberto o software que prepara uma partição para que o sistema possa ser instalado.

Na tela principal, vá até a guia **DISPOSITIVO**, e clique em ***CRIAR TABELA DE PARTIÇÃO***.

Aparecerá uma mensagem avisando que seus dados serão apagados. Clique em **OK**. Já que estamos **criando** uma máquina nova do *zero*, não há risco em apagar os dados.

Agora, clique com o *botão direito* em cima da partição selecionada e selecione **NOVO**.

Selecione o tamanho que você deseja para esta partição e defina os ítens como abaixo:
* Criar como: **Partição Primária**
* Sistema de arquivos: **ext04**
* Rótulo: ***"escreva o nome da sua partição"***

Clique em ***ADICIONAR*** e logo em seguida em ***Aplicar***.

O Gparted prepará uma partição para o sistema.

Clique novamente com o botão direito na partição criada,  e desta vez selecione o ítem ***Gerenciar sinalizadores***.

Selecione a opção **boot** e clique em **FECHAR**

Pronto. Agora é só fechar o Gparted e voltar ao documento de instalação.

Role o arquivo até o final, onde você encontrará o botão ***CONTINUE INSTALATION***.

Nesta nova janela aberta, mantenha as configurações como abaixo:

>  *Select Source Media* : **deixe a opção LIVECD marcada**

> *Select Destination*: **install Slitaz to partition**:   *"selecione a sua partição criada"*

> *Formating Option*: **selecione ext04**

> *User*: **Selecione um usuário e senha para você**

> ***Em BOOTLOADER selecione a opção [**Install a Bootloader**]*** . (Se não selecionar esta opção o sistema não se inicializará).

Para finalizar, clique em ***PROCEED TO SLITAZ INSTALLATION***.

O sistema começará a instalar os arquivos necessários na VM.

 Quando aparecer a mensagem **Process Completed**, será necessário reiniciar a VM. Para isto basta clicar no botão ***INSTALLATION COMPLETE. YOU CAN NOW RESTART***.

> Um detalhe importante: Não esqueça de alterar a orderm de **boot** na sua VM, para que o LIVECD não entre antes do HD.
