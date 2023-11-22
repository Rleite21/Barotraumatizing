
                                            WIKI ESPECIAL DO BAROTRAUMA SOBRE O FUNCIONAMENTO DO JOGO
/////////////////////////////////                    https://regalis11.github.io/BaroModDoc/                /////////////////////////////////////////////////////////
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
Olé!
    Esta pasta (Barotraumatizing) vai ser o lugar onde TODOS os ficheiros do mod necessários serão colocados (pelo menos por agora). O mod irá trabalhar principalmente com ficheiros no formato XML.
Para algumas dicas sobre como funciona a linguagem é melhor seguires te pelos ficheiros exemplo criados como o G3.xml. Alternativamente também há explicações mais profundas na wiki no link ali em cima!! Vai ver crl

/////////////////////////////////////////////////////////// Aqui dentro teremos diferentes tipos de ficheiros e pastas aqui explicadas: ///////////////////////////////////////////////////////////////////////

    "filelist.xml": Provavelmente um dos ficheiros mais importantes para o funcionamento do mod
        O filelist tem a simples função de apontar ao jogo quais são os ficheiros importantes para o nosso mod, ou seja: Mesmo que seja criada alguma coisa nova, se ela não for referida neste ficheiro, não irá aparecer no jogo
        Dentro do filelist, para ser invocado um dado ficheiro faz-se a seguinte linha do código (podendo ser alterada de acordo com a situação):
    
    <Item file="%ModDir%/G3.xml"/>

    Nesta linha temos as seguintes informações: 
        "Item file" ----- enuncia o tipo de ficheiro, neste caso temos um ficheiro que adiciona Itens para o jogo
        "%ModDir%/G3.xml" -------- é a localização do ficheiro XML


/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

As pastas de Assets: Assets são todo o género de ficheiro necessário para representar os nossos mods e outros afins in-game: Sprites (imagens em formato PNG) e OGG's (ficheiros de som);
Estas pastas devem estar num lugar de fácil acesso uma vez que vai ser invocadas dentro dos nossos ficheiros xml como por exemplos aqui:

    Nós queremos que a nossa arma "G3" tenha a imagem "G3.png". O nosso código do xml irá ter esta linha eventualmete (com uma outra mixórdia de merdas):

    <Sprite texture="%ModDir%/Barotraumatizing/Weapons Assets/Textures/G3 Magazine.png" depth="0.54" sourcerect="0,0,76,128" origin="0.5,0.5" />

    "Sprite texture" (a textura do sprite, que é essencialmente a imagem que será vista in-game)
    "%ModDir%/Barotraumatizing/Weapons Assets/Textures/G3 Magazine.png": é a localização do nosso G3.png (%ModDir% == pasta do mod em questão, que neste caso é a pasta Barotraumatizing)

    O uso de %ModDir" é ABSOLUTAMENTE OBRIGATÓRIO senão habilitamo-nos a desorganizar o projeto e a criar bugs desnecessários e se querem palhaçada vão ao Circo Vivaldi

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////