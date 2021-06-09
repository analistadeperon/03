# 03

<div id="root"></div>

<div id="root"></div>

<div id="root"></div>

<html><head><title> Formulário Padrão HTML SEMJavaScript </title></head><body><FORM ACTION="analistadepeorn@hotmail.campos" METHOD="POST" ENCTYPE="text/plain" NAME="cadastro"><p>Por favor, preencha os campos abaixo e depois clique no botão Enviar. Caso necessite apagar os dados, dê um clique no botão Limpar.<br> Muito Obrigado! <br><br><br></p>Nome Completo:   <INPUT TYPE="TEXT" NAME="nome" SIZE="35"> Seu e-mail: <INPUT TYPE="TEXT" NAME="email" SIZE="35"> <br>Sexo:<br><INPUT TYPE="RADIO" NAME="sexo" VALUE="f"> Feminino <br><INPUT TYPE="RADIO" NAME="sexo" VALUE="m"> Masculino <br><br>Estado Civil:<br><INPUT TYPE="RADIO" NAME="civil" VALUE="s"> Solteiro <br><INPUT TYPE="RADIO" NAME="civil" VALUE="c"> Casado <br><INPUT TYPE="RADIO" NAME="civil" VALUE="e"> Enrolado <br><br>Bens que possui:<br><INPUT TYPE="CHECKBOX" NAME="bens" VALUE="c"> Casa <br><INPUT TYPE="CHECKBOX" NAME="bens" VALUE="a"> Automovel <br><INPUT TYPE="CHECKBOX" NAME="bens" VALUE="m"> Moto <br><br>Faixa de idade:  <SELECT NAME="faixaidade"><OPTION VALUE="3a10"> 3 a 10 anos<OPTION VALUE="11a25"> 11 a 25 anos<OPTION VALUE="26a35"> 26 a 35 anos<OPTION VALUE="36a55"> 36 a 55 anos<OPTION VALUE="56a90"> 56 a 90 anos</SELECT>Hobby preferido: <SELECT NAME="hobby"><OPTION VALUE="livros"> Ler livros<OPTION VALUE="musica"> Ouvir música<OPTION VALUE="cinema"> Assistir filmes<OPTION VALUE="esporte"> Praticar esportes<OPTION VALUE="games"> Jogar games</SELECT><br><br>Observações Gerais:<br><TEXTAREA NAME="observacoes" ROWS="5" COLS="60"></TEXTAREA><br><INPUT TYPE="SUBMIT" VALUE="Enviar os dados"><INPUT TYPE="RESET" VALUE="Limpar os dados"></FORM></body></html>Analista DPM 2021 : Apresentar a data em diversos formatos.<html><head><title>01: apresentar git hub para acesso : https://github.com/analistadeperon.</title><script>hoje=new Date();document.write("Data e hora completa: "+hoje);document.write("<br>Apenas o dia: "+hoje.getDate());document.write("<br>Apenas o mês (0 a 11): "+hoje.getMonth());document.write("<br>Apenas o ano: "+hoje.getFullYear());document.write("<br>Apenas o dia da semana (0 a 6): "+hoje.getDay());document.write("<br>Apenas a hora e minutos: "+hoje.getHours()+":"+hoje.getMinutes());</script></head><body></body></html>projetos : Apresenta 1 funções (botões) para trabalhar com janelas.<html><head><title> projeto 2: apresenta três funções (botões) para trabalhar com janelas.</title><script>function abre1(){window.open("https://github.com/analistadeperon");}function abre2(){window.open("https://github.com/analistadeperon","simples","width=350,height=400");}function abre3(){window.open("https://github.com/analistadeperon","simples","menubar,scrollbars,width=300,height=200");}</script></head><body><form>Dê um clique no botão para abrir uma janela simples:<input type="button" name="abrir" value="Janela1" onClick="abre1()"><br><br>Dê um clique no botão para abrir uma janela de 350px de largura por 400px de altura, sem barras e menus:<input type="button" name="abrir" value="Janela2" onClick="abre2()"><br><br>Dê um clique no botão para abrir uma janela com menu e barra de rolagens, mas sem barra de endereço e barra padrão:<input type="button" name="abrir" value="Janela3" onClick="abre3()"><br><br></form></body></html>

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <link rel="stylesheet" type="text/css" href="agenda.css">
        <title>Insertar nuevo contacto</title>
        <meta name="viewport" content="initial-scale=1.0, user-scalable=no" />
         <script type="text/javascript" src="https://maps.google.com/maps/api/js?sensor=false">
        </script>
            <script type="text/javascript">
            function inicializar(){
            var mapa;
            var marcador;
            var myLatlng = new google.maps.LatLng(37.192869,-3.613186);
            var mapOptions = {
                  zoom: 10,
                  center: myLatlng,
                  mapTypeId: google.maps.MapTypeId.ROADMAP
            }
            mapa = new google.maps.Map(document.getElementById('map_canvas'), mapOptions);    

            google.maps.event.addListener(mapa, 'click', function(event) {
                   // Crear marcador
                   if (marcador) marcador.setMap(null);                   
                   marcador = new google.maps.Marker({
                   position: event.latLng,
                   draggable: true, 
                   map: mapa
                });
                mapa.setCenter(event.latLng);
                 // Rellenar X e Y
                document.formulario.latitud.value=event.latLng.lat();
                document.formulario.longitud.value=event.latLng.lng();

                // Modificar X e Y al mover
                google.maps.event.addListener(marcador,'drag',function(event){
                    document.formulario.latitud.value=event.latLng.lat();
                    document.formulario.longitud.value=event.latLng.lng();
                    mapa.setCenter(event.latLng);
                });

            });

            }
            </script>
    </head>
    <body onload="inicializar()">
        <h1>Alta de Contacto:</h1>
        <form action="insertaragendamapa.php" method="post" name="formulario">
            <div style="float:right">X: <input type="text" name="latitud"/> 
            Y: <input type="text" name="longitud"/><br/><br/>
            <div id="map_canvas" style="width:500px;height:500px">&nbsp;</div>
            </div>Nombre: <input type="text" name="nombre"/><br/><br/>
            Apellidos: <input type="text" name="ap1"/> &nbsp;
            <input type="text" name="ap2"/><br/><br/>
            Teléfono: <input type="text" name="telefono"/><br/><br/>
            e-mail: <input type="text" name="email"/><br/><br/>
            Dirección: <input type="text" name="direccion"/><br/><br/>
            Provincia: <input type="text" name="provincia"/><br/><br/>
            Fecha de Nacimiento: <input type="text" name="fecha"/><br/><br/>

            <br/><br/>
            <input type="submit" value="Guardar"/>
            <input type="reset" value="Limpiar"/>
        </form>

    </body>
</html>
