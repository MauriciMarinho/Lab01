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

    Este arquivo ir� lhe guiar na instala��o de uma m�quina virtual (hospedeira), configura��o e instala��o do Sistema Operacional Slitaz/Linux 5.0 RC-3.
    Os passos a ser seguidos ser�o:

  **1 - Download do S.O. Slitaz/Linux 5.0 RC-3**
  
  **2 - Cria��o a M�quina Virtual**
  
 **3 - Configura��o da M�quina Virtual**
 
 **4 -  Instala��o do S.O. Slitaz/Linux 5.0 RC-3**
 
  ---
## 1 - Download do S.O. Slitaz/Linux 5.0 RC-3

Fa�a o *download* do Slitaz 5.0 RC-3 no site http://www.slitaz.org/pt/news/ e armazene o arquivo *.ISO* em um diret�rio de f�cil acesso.

&nbsp;

---
## 2 - Cria��o da M�quina Virtual
    
Para a *virtualiza��o* iremos utilizar o software da Oracle, o **"VirtualBox"**, que pode ser encontrado no site https://www.virtualbox.org/wiki/Downloads.
   
Ap�s a instala��o, a interface principal do VirtualBox se abrir�.
   
 Primeiramente, devemos criar o ambiente virtual (o qual receber� o sistema operacional virtual). 
 
 - Clique no bot�o ***NOVO***
 
Na tela que ser� aberta, d� um nome � VM e escolha a plataforma e o sistema operacional:
* Em TIPO selecione: ***LINUX***
* Em Vers�o selecione: ***Other Linux 32bits***

Depois de escolher o sistema e dar um nome, clique em ***PR�XIMO***:

Nesta tela, defina a quantidade de mem�ria RAM da *VM* que ser� de 512 Mb ou superior.

* Clique em ***PR�XIMO***.

Na sequ�ncia, marque a op��o **"Criar um disco virtual agora"** e clique em ***CRIAR***.

Na tela seguinte, selecione o item **VDI( VirtualBox Disc Image)** e clique em ***PR�XIMO***.

Agora teremos que decidir o tipo de armazenamento  do HD virtual. Para esta aplica��o iremos utilizar o �tem **"Dinamicamente Alocado"**. Ap�s escolher o tipo, clique em ***PR�XIMO***

Agora, selecione o tamanho para o HD que ser� de  *60Gb* e clique em ***CRIAR***.

Ao t�rmino, voc� ver� a VM que acabou de criar na tela do VirtualBox.



&nbsp;

---

## 3 - Configura��o da M�quina Virtual

* Clique no bot�o **Configura��es** na tela principal do VirtualBox.

> Nesta �rea voc� poder� realizar as configura��es que julgar necess�rias para o funcionamento da sua VM.

> N�o entrarei em detalhes acerca de cada op��o, apenas informarei as configura��es para o nosso caso.

Na guia ***SISTEMA***, defina a ordem de *BOOT* colocando:

- 1� CDROM
- 2� HardDisk

Na guia ***ARMAZENAMENTO***, clique em cima do �cone do *cdrom* e no canto direito selecione o local da  imagem (.ISO) do SLITAZ 5.0 RC-3 que voc� efetuou o *download*.

Clique em **OK**, e de volta na tela principal do VirtualBox, clique em ***INICIAR***.


>A *distro* Slitaz 5.0 RC-3 � pequena e leve. Este arquivo � um *LIVECD*, ou seja, roda diretamente do CDROM, sendo assim, ser� necess�ria a instala��o do Slitaz dentro da nossa VM. Veremos isso a seguir.

&nbsp;

---

## 4 - Instala��o do S.O. Slitaz/Linux 5.0 RC-3

Com a VM iniciada e o Slitaz operando, abra no menu **APLICATIVOS**, o submenu **Sistema/Instalador do Slitaz**.

Ser� aberto um arquivo ***DOCUMENTA��O***, onde nele cont�m todas as informa��es para a instala��o do Slitaz.

> Para a instala��o do Slitaz, � necess�rio que seja criada uma parti��o para que o sistema possa ser instalado.

Role o arquivo at� o bot�o ***"EXECUTE GPARTED"***.

Ser� aberto o software que prepara uma parti��o para que o sistema possa ser instalado.

Na tela principal, v� at� a guia **DISPOSITIVO**, e clique em ***CRIAR TABELA DE PARTI��O***.

Aparecer� uma mensagem avisando que seus dados ser�o apagados. Clique em **OK**. J� que estamos **criando** uma m�quina nova do *zero*, n�o h� risco em apagar os dados.

Agora, clique com o *bot�o direito* em cima da parti��o selecionada e selecione **NOVO**.

Selecione o tamanho que voc� deseja para esta parti��o e defina os �tens como abaixo:
* Criar como: **Parti��o Prim�ria**
* Sistema de arquivos: **ext04**
* R�tulo: ***"escreva o nome da sua parti��o"***

Clique em ***ADICIONAR*** e logo em seguida em ***Aplicar***.

O Gparted prepar� uma parti��o para o sistema.

Clique novamente com o bot�o direito na parti��o criada,  e desta vez selecione o �tem ***Gerenciar sinalizadores***.

Selecione a op��o **boot** e clique em **FECHAR**

Pronto. Agora � s� fechar o Gparted e voltar ao documento de instala��o.

Role o arquivo at� o final, onde voc� encontrar� o bot�o ***CONTINUE INSTALATION***.

Nesta nova janela aberta, mantenha as configura��es como abaixo:

>  *Select Source Media* : **deixe a op��o LIVECD marcada**

> *Select Destination*: **install Slitaz to partition**:   *"selecione a sua parti��o criada"*

> *Formating Option*: **selecione ext04**

> *User*: **Selecione um usu�rio e senha para voc�**

> ***Em BOOTLOADER selecione a op��o [**Install a Bootloader**]*** . (Se n�o selecionar esta op��o o sistema n�o se inicializar�).

Para finalizar, clique em ***PROCEED TO SLITAZ INSTALLATION***.

O sistema come�ar� a instalar os arquivos necess�rios na VM.

 Quando aparecer a mensagem **Process Completed**, ser� necess�rio reiniciar a VM. Para isto basta clicar no bot�o ***INSTALLATION COMPLETE. YOU CAN NOW RESTART***.

> Um detalhe importante: N�o esque�a de alterar a orderm de **boot** na sua VM, para que o LIVECD n�o entre antes do HD.
