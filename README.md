<html>
  <head>
    <title>Portadoras y frecuencias de telefonia móvil</title>
    <link type="text/css" rel="stylesheet" id="dark-mode-custom-link" />
    <link type="text/css" rel="stylesheet" id="dark-mode-general-link" />
    <style lang="en" type="text/css" id="dark-mode-custom-style"></style>
    <style lang="en" type="text/css" id="dark-mode-native-style"></style>
    <style lang="en" type="text/css" id="dark-mode-native-sheet"></style>
    <meta http-equiv="content-type" content="text/html; charset=UTF-8" />
    <style class="native-dark-class-modified">
      .Boton_Apagado {
        background-color: grey;

        border-radius: 60px;
        border: none;
        color: SeaShell;
        cursor: pointer;
        display: inline-block;
        font-family: sans-serif;
        font-size: 20px;
        padding: 10px 10px 0px 10px;
        text-align: center;
        text-decoration: none;
        box-shadow: 5px 5px 5px #ccc;
      }
      .Boton_Encendido {
        background-color: #1c87c9;
        -webkit-border-radius: 60px;
        border-radius: 60px;
        border: none;
        color: #eeeeee;
        cursor: pointer;
        display: inline-block;
        font-family: sans-serif;
        font-size: 20px;
        padding: 10px 10px 0px 10px;
        text-align: center;
        text-decoration: none;
      }
      @keyframes glowing {
        0% {
          background-color: #2ba805;
          box-shadow: 0 0 5px #2ba805;
        }
        50% {
          background-color: #49e819;
          box-shadow: 0 0 20px #49e819;
        }
        100% {
          background-color: #2ba805;
          box-shadow: 0 0 5px #2ba805;
        }
      }
      .Boton_Encendido {
        animation: glowing 1300ms infinite;
      }

      ul {
        list-style: none;
      }
      .context-menu {
        position: absolute;
        z-index: 1;
      }
      .menu {
        display: flex;
        flex-direction: column;
        background-color: #555;
        border-radius: 10px;
        padding: 10px 0;
      }
      .menu > li > a {
        font: inherit;
        border: 0;
        padding: 10px 30px 10px 15px;
        width: 110px;
        display: flex;
        align-items: center;
        position: relative;
        text-decoration: unset;
        color: SeaShell;
        font-weight: 500;
        transition: 100ms linear;
      }
      .menu > li > a:hover {
        background: #e5e7e9;
        color: indigo;
      }

      .blink {
        animation: blinker 1.5s linear infinite;
        color: red;
        font-family: verdana;
      }
      @keyframes blinker {
        50% {
          opacity: 0;
        }
      }

      .hide {
        visibility: hidden;
      }

      .Marcada {
        background: indigo;
        color: white;
      }

      .SinMarcar {
        background: white;
      }

      td {
        height: 22px;
        padding: 3px;
        border: 2px dotted black;
        text-align: center;
        width: 70;
        border-radius: 12px;
        box-shadow: 5px 5px 5px #ccc;
      }

      td:hover {
        color: Coral;
        border-radius: 0px;
      }

      .tooltip {
        position: relative;
      }

      .tooltip .tooltiptext {
  visibility: hidden;
  width: 190px;
  background-color: #555;
  color: #fff;
  text-align: center;
  border-radius: 6px;
  padding: 10px;
  position: absolute;
  z-index: 1;
  top: 50%;
  left: 120%;
  transform: translateY(-50%);
  opacity: 0;
  transition: opacity 0.3s;
  display: flex;
  flex-direction: column;
  align-items: center;
}


      .tooltip .tooltiptext img {
        width: 50px;
        height: auto;
        margin-bottom: 5px;
      }

     .tooltip .tooltiptext::after {
  content: "";
  position: absolute;
  top: 50%;
  right: 100%;
  margin-top: -7px;
  border-width: 7px;
  border-style: solid;
  border-color: transparent #555 transparent transparent;
}

      .tooltip:hover .tooltiptext {
        visibility: visible;
        opacity: 1;
      }

      .info-button {
        width: 30px; /* Tamaño pequeño y circular */
        height: 30px;
        border-radius: 50%; /* Forma circular */
        background-color: #4caf50; /* Verde, como ejemplo de color distintivo */
        color: white; /* Texto blanco */
        font-size: 16px; /* Tamaño de la "i" */
        font-weight: bold;
        border: none; /* Sin bordes por defecto */
        cursor: pointer; /* Mano al pasar el ratón */
        margin: auto; /* Centrado como el botón Genera Listado */
        margin-bottom: 10px; /* Espacio entre este botón y Genera Listado */
        display: flex; /* Para centrar la "i" */
        align-items: center;
        justify-content: center;
        transition: background-color 0.3s; /* Transición suave al hover */
      }

      .info-button:hover {
        background-color: #45a049; /* Verde más oscuro al pasar el ratón */
        box-shadow: 0 0 10px #45a049; /* Efecto glowing al hover */
      }

      #infoTable img {
        max-width: 50px; /* Ancho máximo del logotipo */
        max-height: 50px; /* Alto máximo del logotipo */
        width: auto; /* Mantiene la proporción */
        height: auto; /* Mantiene la proporción */
        display: block; /* Asegura que la imagen no tenga espacio adicional */
        margin: 0 auto; /* Centra la imagen horizontalmente */
      }

      #infoTable {
        overflow: auto; /* Añade scroll si el contenido es demasiado grande */
        max-height: 200px; /* Limita la altura máxima de la tabla */
        max-width: 800px; /* Aumenta el ancho máximo de la tabla */
        background-color: transparent; /* Fondo transparente para la tabla */
        border: none; /* Elimina el borde de la tabla */
        padding: 10px;
        box-shadow: none; /* Elimina la sombra de la tabla */
      }

      #infoContent {
        font-size: 14px;
        color: #333;
        background-color: #f9f9f9; /* Fondo sólido para la celda */
        border: 1px solid #ccc; /* Borde para la celda */
        border-radius: 5px; /* Bordes redondeados para la celda */
        padding: 10px; /* Espaciado interno */
        white-space: normal; /* Permite que el texto se ajuste en varias líneas */
        word-wrap: break-word; /* Asegura que el texto no se desborde */
        width: 180px; /* Define un ancho fijo para la celda */
        min-width: 50px; /* Asegura que la celda no sea más pequeña que este valor */
        visibility: hidden;
      }
    </style>
  </head>
  <body style="font-family: verdana; background: SeaShell">
    <div
      id="contextMenu_Movistar"
      class="context-menu"
      style="display: none; left: 327px; top: 25px"
    >
      <ul class="menu">
        <li class="Obligadas">
          <a href="#" onclick="Obligatorias_Movistar()"> Obligatorias</a>
        </li>
		<li class="EV">
          <a href="#" onclick="EV_Movistar()"> EV's</a>
        </li>
        <li class="Todas">
          <a href="#" onclick="Todo('Operador-Movistar')"> Todas</a>
        </li>
        <li class="Limpiar">
          <a href="#" onclick="Borrar('Operador-Movistar')"> Limpiar Tabla</a>
        </li>
      </ul>
    </div>

    <div
      id="contextMenu_Orange"
      class="context-menu"
      style="display: none; left: 727px; top: 25px"
    >
      <ul class="menu">
        <li class="Obligadas">
          <a href="#" onclick="Obligatorias_Orange()"> Obligatorias</a>
        </li>
		<li class="EV">
          <a href="#" onclick="EV_Orange()"> EV's</a>
        </li>
        <li class="Todas">
          <a href="#" onclick="Todo('Operador-Orange')"> Todas</a>
        </li>
        <li class="Limpiar">
          <a href="#" onclick="Borrar('Operador-Orange')"> Limpiar Tabla</a>
        </li>
      </ul>
    </div>

    <div id="contextMenu_Vodafone" class="context-menu" style="display: none">
      <ul class="menu">
        <li class="Obligadas">
          <a href="#" onclick="Obligatorias_Vodafone()"> Obligatorias</a>
        </li>
		<li class="EV">
          <a href="#" onclick="EV_Vodafone()"> EV's</a>
        </li>
        <li class="Todas">
          <a href="#" onclick="Todo('Operador-Vodafone')"> Todas</a>
        </li>
        <li class="Limpiar">
          <a href="#" onclick="Borrar('Operador-Vodafone')"> Limpiar Tabla</a>
        </li>
      </ul>
    </div>

    <div id="contextMenu_Yoigo" class="context-menu" style="display: none">
      <ul class="menu">
        <li class="Obligadas">
          <a href="#" onclick="Obligatorias_Yoigo()"> Obligatorias</a>
        </li>
        <li class="Todas">
          <a href="#" onclick="Todo('Operador-Yoigo')"> Todas</a>
        </li>
        <li class="Limpiar">
          <a href="#" onclick="Borrar('Operador-Yoigo')"> Limpiar Tabla</a>
        </li>
      </ul>
    </div>

    <table
      style="position: absolute; top: 10px; left: 20px"
      id="Titulo_Movistar"
    >
      <tbody>
        <tr>
          <td
            style="
              font-size: 20px;
              height: 10px;
              width: 330px;
              text-align: center;
              background: DodgerBlue;
              font-weight: bold;
              border: 2px solid black;
              color: black;
            "
            title=" Click derecho para opciones"
          >
            Portadoras de Movistar
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 14px 0px;
        position: absolute;
        top: 70px;
        left: 10px;
      "
      id="Cabecera_Movistar"
    >
      <tbody>
        <tr>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="DOSG('Operador-Movistar')"
          >
            2G
          </td>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="TRESG('Operador-Movistar')"
          >
            3G
          </td>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="CUATROG('Operador-Movistar')"
          >
            4G
          </td>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="CINCOG('Operador-Movistar')"
          >
            5G
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 10px 10px;
        position: absolute;
        top: 100px;
        left: 10px;
      "
      id="Operador-Movistar"
    >
      <tbody>
        <tr>
          <td
            style="
              font-size: 12px;
              border: 2px solid green;
              box-shadow: 5px 5px 5px green;
            "
            class="tooltip SinMarcar"
          >
            <b>1-74</b
            ><span class="tooltiptext"
              >2G GSM<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>10788</b>
            <span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>1301</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 1800 B3<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>636576</b
            ><span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (50MHZ)<br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
          <td class="hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>10813</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>1321</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 1800 B3<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            650400<span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (50MHZ)<br />Frecuente
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>10838</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>1347</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 1800 B3<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            651648<span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (50MHZ)<br />
              Frecuente</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>3000</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>2850</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2600 B7<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            651666<span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (50MHZ)<br />Frecuente
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>3011</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>3600</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 900 B8<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>432970</b
            ><span class="tooltiptext"
              >5G NR 2100<br />
              N1 Case B (10/15 MHZ)<br />Obligatoria
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>3031</i
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 900<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>6375</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 800 B20<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            432510<span class="tooltiptext"
              >5G NR 2100<br />
              N1 Case B (10/15 MHZ)<br
            /></span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>3032</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>6400</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 800 B20<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            433450<span class="tooltiptext"
              >5G NR 2100<br />
              N1 Case B (10/15 MHZ)<br />
              Frecuente
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>3034</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>500</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            156600<span class="tooltiptext"
              >5G NR 700<br />
              N28 case A (10/15 MHZ)<br />
              Frecuente</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>550</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>156510</b
            ><span class="tooltiptext"
              >5G NR 700<br />
              N28 case A (10/15 MHZ)<br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>9460</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 700 B28<br />
              Obligatoria</span
            >
          </td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
      </tbody>
    </table>

    <table
      style="position: absolute; top: 10px; left: 410px"
      id="Titulo_Orange"
    >
      <tbody>
        <tr>
          <td
            style="
              font-size: 20px;
              height: 10px;
              width: 355px;
              text-align: center;
              background: orange;
              font-weight: bold;
              border: 2px solid black;
              color: black;
            "
            title=" Click derecho para opciones"
          >
            Portadoras de Orange
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 14px 0px;
        position: absolute;
        top: 70px;
        left: 400px;
      "
      id="Cabecera_Orange"
    >
      <tbody>
        <tr>
          <td
            style="border: 2px solid black; font-size:15px;height:10px;text-align:center;font-weight:bold;background:Moccasin; width:85px; 2px solid black; color: black;"
            onclick="DOSG('Operador-Orange')"
          >
            2G
          </td>
          <td
            style="border: 2px solid black;font-size:15px;height:10px;text-align:center;font-weight:bold;background:Moccasin; width:65px; 2px solid black; color: black;"
            onclick="TRESG('Operador-Orange')"
          >
            3G
          </td>
          <td
            style="border: 2px solid black;font-size:15px;height:10px;text-align:center;font-weight:bold;background:Moccasin; width:65px; 2px solid black; color: black;"
            onclick="CUATROG('Operador-Orange')"
          >
            4G
          </td>
          <td
            style="border: 2px solid black;font-size:15px;height:10px;text-align:center;font-weight:bold;background:Moccasin; width:65px; 2px solid black; color: black;"
            onclick="CINCOG('Operador-Orange')"
          >
            5G
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 10px 10px;
        position: absolute;
        top: 100px;
        left: 400px;
      "
      id="Operador-Orange"
    >
      <tbody>
        <tr>
          <td
            style="
              border: 2px solid green;
              box-shadow: 5px 5px 5px green;
              width: 92px;
              text-align: left;
              font-size: 14px;
            "
            class="tooltip SinMarcar"
          >
            <b>0,975-996</b
            ><span class="tooltiptext"
              >2G GSM<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>10663</b>
            <span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>1849</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 1800 B3<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>642048</b
            ><span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (60MHZ) HUAWEI<br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
		<td
            style="
              border: 2px solid green;
              box-shadow: 5px 5px 5px green;
              width: 92px;
              text-align: left;
              font-size: 9px;
            "
            class="tooltip SinMarcar"
          >
            <b>786-788,883-885</b
            ><span class="tooltiptext"
              >2G GSM<br />
              BANDA 1800<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>10688</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>3050</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2600 B7<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>640704</b
            ><span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (60MHZ) ERICSSON<br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>10638</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            3400<span class="tooltiptext"
              >4G LTE<br />
              BANDA 2600 B7<br />
              Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            640608<span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (50MHZ) ZTE<br />
              Frecuente</span
            >
          </td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>2959</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            3518<span class="tooltiptext"
              >4G LTE<br />
              BANDA 900 B8<br />
              Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>426050</b
            ><span class="tooltiptext"
              >5G NR 2100<br />
              N1 Case B (10/15MHZ)<br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>6200</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 800 B20<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            425084<span class="tooltiptext"
              >5G NR 2100<br />
              N1 Case B (10/15MHZ)<br />Frecuente</span
            >
          </td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>201</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>156750</i
            ><span class="tooltiptext"
              >5G NR 700<br />
              N28 case A (10/15MHZ)<br />Poco Frecuente</span
            >
          </td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>225</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>152690</b
            ><span class="tooltiptext"
              >5G NR 700<br />
              N28 case A (10/15MHZ)<br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>226</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1<br />
              Poco Frecuente</span
            >
          </td>
         
		  
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            <b> 537000</b
            ><span class="tooltiptext"
              >5G NR <br />
              BANDA 2600 N7 <br />
              Frecuente</span
            >
          </td>
		  
		  
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>9260</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 700 B28<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b> 537150</b
            ><span class="tooltiptext"
              >5G NR <br />
              BANDA 2600 N7 <br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td style="width: 90px" class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
      </tbody>
    </table>

    <table
      style="position: absolute; top: 10px; left: 830px"
      id="Titulo_Vodafone"
    >
      <tbody>
        <tr>
          <td
            style="
              font-size: 20px;
              height: 10px;
              width: 335px;
              text-align: center;
              background: red;
              font-weight: bold;
              border: 2px solid black;
              color: #090707;
            "
            title=" Click derecho para opciones"
          >
            Portadoras de Vodafone
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 14px 0px;
        position: absolute;
        top: 70px;
        left: 820px;
      "
      id="Cabecera_Vodafone"
    >
      <tbody>
        <tr>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="DOSG('Operador-Vodafone')"
          >
            2G
          </td>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="TRESG('Operador-Vodafone')"
          >
            3G
          </td>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="CUATROG('Operador-Vodafone')"
          >
            4G
          </td>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="CINCOG('Operador-Vodafone')"
          >
            5G
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 10px 10px;
        position: absolute;
        top: 100px;
        left: 820px;
      "
      id="Operador-Vodafone"
    >
      <tbody>
        <tr>
          <td
            style="
              border: 2px solid green;
              box-shadow: 5px 5px 5px green;
              font-size: 14px;
            "
            class="tooltip SinMarcar"
          >
            <b>75-124</b
            ><span class="tooltiptext"
              >2G GSM<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>10713</b>
            <span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>1480</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 1800 B3<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            645116
            <span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (90/80MHZ)
            </span>
          </td>
        </tr>
        <tr>
          <td class="hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>10738</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>1501</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 1800 B3<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            645020<span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (90/80MHZ)<br />
              Frecuente
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>10763</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>3250</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2600 B7<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            645024<span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (90/80MHZ)<br />Frecuente
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>3062</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>3724</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 900 B8<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            647000<span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (90/80MHZ)
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>3087</b
            ><span class="tooltiptext"
              >3G UMTS<br />
              BANDA 900<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>3749</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 900 B8<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>648384</b
            ><span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (90/80MHZ)<br />Obligatoria
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>3774</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 900 B8<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            650334<span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (90/80MHZ)<br />Frecuente
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>6300</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 800 B20<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>429520</b
            ><span class="tooltiptext"
              >5G NR 2100<br />
              N1 Case B (10/15MHZ)<br />Obligatoria
            </span>
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid red; box-shadow: 5px 5px 5px red"
            class="tooltip SinMarcar"
          >
            <i>376</i
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1<br />
              Poco Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>428890</b
            ><span class="tooltiptext"
              >5G NR 2100<br />
              N1 Case B (10/15MHZ)<br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>401</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            154600<span class="tooltiptext"
              >5G NR 700<br />
              N28 case A (10/15MHZ))</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid gold; box-shadow: 5px 5px 5px gold"
            class="tooltip SinMarcar"
          >
            426<span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1<br />Frecuente</span
            >
          </td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            152600<span class="tooltiptext"
              >5G NR 700<br />
              N28 case A (10/15MHZ)</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>9360</b
            ><span class="tooltiptext"
              >4G LTE<br />
              BANDA 700 B28<br />
              Obligatoria</span
            >
          </td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            367020<span class="tooltiptext"
              >5G NR 1800<br />
              N3 case B <br />(20MHZ)</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>154570</b
            ><span class="tooltiptext"
              >5G NR 700<br />
              N28 case A (10/15MHZ)<br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
      </tbody>
    </table>

    <table
      style="position: absolute; top: 10px; left: 1220px"
      id="Titulo_Yoigo"
    >
      <tbody>
        <tr>
          <td
            style="
              border-spacing: 5px;
              font-size: 20px;
              height: 10px;
              width: 335px;
              text-align: center;
              background: MediumVioletRed;
              font-weight: bold;
              border: 2px solid black;
              color: black;
            "
            title=" Click derecho para opciones"
          >
            Portadoras de Yoigo
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 14px 0px;
        position: absolute;
        top: 70px;
        left: 1210px;
      "
      id="Cabecera_Yoigo"
    >
      <tbody>
        <tr>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="DOSG('Operador-Yoigo')"
          >
            2G
          </td>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="TRESG('Operador-Yoigo')"
          >
            3G
          </td>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="CUATROG('Operador-Yoigo')"
          >
            4G
          </td>
          <td
            style="
              font-size: 15px;
              text-align: center;
              font-weight: bold;
              background: Moccasin;
              width: 65px;
              border: 2px solid black;
              color: black;
            "
            onclick="CINCOG('Operador-Yoigo')"
          >
            5G
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 10px 10px;
        position: absolute;
        top: 100px;
        left: 1210px;
      "
      id="Operador-Yoigo"
    >
      <tbody>
        <tr>
          <td
            style="
              border: 2px solid grey;
              box-shadow: 5px 5px 5px grey;
              font-size: 14px;
            "
            class="tooltip SinMarcar"
          >
            712-785<span class="tooltiptext"
              >2G GSM<br />
              BANDA 1800<br />
              <b>POSIBLEMENTE ANULADAS</b>
            </span>
          </td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            10563
            <span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100</span
            >
          </td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            1650<span class="tooltiptext"
              >4G LTE<br />
              BANDA 1800 B3</span
            >
          </td>
          <td
            style="border: 2px solid green; box-shadow: 5px 5px 5px green"
            class="tooltip SinMarcar"
          >
            <b>634666</b
            ><span class="tooltiptext"
              >5G NR 3500<br />
              N78 case B (40MHZ) <br />
              Obligatoria</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            10588<span class="tooltiptext"
              >3G UMTS<br />
              BANDA 2100</span
            >
          </td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            1691<span class="tooltiptext"
              >4G LTE<br />
              BANDA 1800 B3</span
            >
          </td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            1675<span class="tooltiptext"
              >4G LTE<br />
              BANDA 1800 B3</span
            >
          </td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            101<span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1</span
            >
          </td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td
            style="border: 2px solid grey; box-shadow: 5px 5px 5px grey"
            class="tooltip SinMarcar"
          >
            126<span class="tooltiptext"
              >4G LTE<br />
              BANDA 2100 B1</span
            >
          </td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
        <tr>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
          <td class="tooltip SinMarcar hide"></td>
        </tr>
      </tbody>
    </table>

    <a
      style="
        position: absolute;
        top: 680px;
        left: 10px;
        font-size: 20px;
        font-weight: bold;
        font-family: verdana;
        height: 35;
      "
      id="BotonGenerador"
      ;=""
      class="Boton_Apagado"
      href="#"
      onclick="Generar_Listado_Portadoras()"
      >Genera Listado
    </a>

    <table style="position: absolute; top: 900px; left: 140px" id="Version">
      <tbody>
        <tr>
          <td
            style="
              font-size: 20px;
              height: 10px;
              width: 900px;
              text-align: center;
              background: Beige;
              border: 2px solid black;
              color: black;
            "
          >
            <i
              >Datos de frecuencias/portadoras actualizadas a 18-06-25. Versión
              de web 1.6</i
            >
          </td>
        </tr>
      </tbody>
    </table>

    <button
      style="
        position: absolute;
        height: 22;
        top: 766px;
        left: 10px;
        font-family: verdana;
        box-shadow: 5px 5px 5px #ccc;
      "
      title="Copia las frecuencias 2G al portapapeles"
      onclick="Portapapeles_2G()"
    >
      Gopia 2G
    </button>
    <button
      style="
        position: absolute;
        height: 22;
        top: 796px;
        left: 10px;
        font-family: verdana;
        box-shadow: 5px 5px 5px #ccc;
      "
      title="Copia las portadoras 3G al portapapeles"
      onclick="Portapapeles_3G()"
    >
      Copia 3G
    </button>
    <button
      style="
        position: absolute;
        height: 22;
        top: 826px;
        left: 10px;
        font-family: verdana;
        box-shadow: 5px 5px 5px #ccc;
      "
      title="Copia las portadoras 4G al portapapeles"
      onclick="Portapapeles_4G()"
    >
      Copia 4G
    </button>
    <button
      style="
        position: absolute;
        height: 22;
        top: 856px;
        left: 10px;
        font-family: verdana;
        box-shadow: 5px 5px 5px #ccc;
      "
      title="Copia las portadoras 5G al portapapeles"
      onclick="Portapapeles_5G()"
    >
      Copia 5G
    </button>

    <table
      style="position: absolute; top: 760px; left: 100px; table-layout: auto"
      id="Sumas"
    >
      <tbody>
        <tr>
          <td
            style="
              width: 0;
              padding: 4;
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: black;
              background: yellow;
            "
          >
            0
          </td>
        </tr>
        <tr>
          <td
            style="
              width: 0;
              padding: 4;
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: grey;
            "
            title="Portadoras máximas 
	Scanner MX 16  
	Scanner IBFLEX 16"
          >
            0
          </td>
        </tr>
        <tr>
          <td
            style="
              width: 0;
              padding: 4;
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: grey;
            "
            title="Portadoras máximas
	Scanner MX 16
	Scanner IBFLEX 16"
          >
            0
          </td>
        </tr>
        <tr>
          <td
            style="
              width: 0;
              padding: 4;
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: grey;
            "
            title="Portadoras máximas
	Scanner MX 16
	Scanner IBFLEX 12"
          >
            0
          </td>
        </tr>
        <tr>
          <td
            style="
              width: 0;
              padding: 4;
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: black;
              background: Yellow;
            "
          >
            0
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="position: absolute; top: 884px; left: 2px; table-layout: auto"
      id="Total"
    >
      <tbody>
        <tr>
          <td
            style="
              width: 0;
              padding: 4;
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: black;
              background: yellow;
            "
          >
            P. Totales
          </td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 5px 0px;
        min-height: 25;
        position: absolute;
        top: 763px;
        left: 145px;
        table-layout: auto;
      "
      id="Portadoras_2G"
    >
      <tbody>
        <tr>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: DodgerBlue;
            "
            title="0"
          ></td>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: orange;
            "
            title="0"
          ></td>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: red;
            "
            title="0"
          ></td>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: MediumVioletRed;
            "
            title="0"
          ></td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 5px 0px;
        min-height: 25;
        position: absolute;
        top: 794px;
        left: 145px;
        table-layout: auto;
      "
      id="Portadoras_3G"
    >
      <tbody>
        <tr>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: DodgerBlue;
            "
            title="0"
          ></td>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: orange;
            "
            title="0"
          ></td>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: red;
            "
            title="0"
          ></td>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: MediumVioletRed;
            "
            title="0"
          ></td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 5px 0px;
        min-height: 25;
        position: absolute;
        top: 825px;
        left: 145px;
        table-layout: auto;
      "
      id="Portadoras_4G"
    >
      <tbody>
        <tr>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: DodgerBlue;
            "
            title="0"
          ></td>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: orange;
            "
            title="0"
          ></td>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: red;
            "
            title="0"
          ></td>
          <td
            style="
              height: 4;
              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: MediumVioletRed;
            "
            title="0"
          ></td>
        </tr>
      </tbody>
    </table>

    <table
      style="
        border-spacing: 5px 0px;
        min-height: 25;
        position: absolute;
        top: 856px;
        left: 145px;
        table-layout: auto;
      "
      id="Portadoras_5G"
    >
      <tbody>
        <tr>
          <td
            style="height:8px;padding:4;height:4;white-space:nowrap;text-align:left; border: 1px solid black; color:white;width=%100;background:DodgerBlue"
            title="0"
          ></td>
          <td
            style="
              height: 8px;

              height: 4;

              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: orange;
            "
            title="0"
          ></td>
          <td
            style="
              height: 8px;

              height: 4;

              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: red;
            "
            title="0"
          ></td>
          <td
            style="
              height: 8px;

              height: 4;

              white-space: nowrap;
              text-align: left;
              border: 1px solid black;
              color: white;
              background: MediumVioletRed;
            "
            title="0"
          ></td>
        </tr>
      </tbody>
    </table>

    <!-- Tabla para mostrar el contenido del tooltiptext -->
    <table
      id="infoTable"
      style="
        position: fixed;
        top: 535px;
        left: 300px;
        padding: 10px;
        z-index: 1000;
      "
    >
      <tbody>
        <tr>
          <td
            id="infoContent"
            style="font-size: 14px; color: #333; border: none"
          >
            <!-- Aquí se mostrará el contenido del tooltiptext -->
          </td>
        </tr>
      </tbody>
    </table>

    <!-- Añade esto en el body del HTML -->
    <div style="position: absolute; top: 600px; left: 10px">
      <label>
        <input type="checkbox" id="togglePopUpInfo" /> Desactivar PopUp
      </label>
    </div>

    <a
      href="https://www.antenasmoviles.es"
      target="_blank"
      style="
        position: absolute;
        top: 550px;
        left: 10px;
        font-size: 16px;
        font-family: verdana;
        color: white;
        background-color: #1c87c9;
        padding: 10px 20px;
        border-radius: 5px;
        text-decoration: none;
        box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
        transition: background-color 0.3s ease;
      "
      onmouseover="this.style.backgroundColor='#155f8a'"
      onmouseout="this.style.backgroundColor='#1c87c9'"
    >
      Datos Antenas Moviles
    </a>

    <script type="text/javascript">
      document.onclick = hideMenu;
      document.getElementById("Titulo_Movistar").oncontextmenu = rightClick1;
      document.getElementById("Titulo_Orange").oncontextmenu = rightClick2;
      document.getElementById("Titulo_Vodafone").oncontextmenu = rightClick3;
      document.getElementById("Titulo_Yoigo").oncontextmenu = rightClick4;

      // permite rellenar la celda de la tabla Orange de verde, o de blanco
      var tabla = document.getElementById("Operador-Orange");
      if (tabla) {
        Array.from(tabla.rows).forEach((tr, rowIdx) => {
          Array.from(tr.cells).forEach((cell, cellIdx) => {
            if (cell.innerText != "") {
              cell.addEventListener("click", function () {
                this.className =
                  this.className == "tooltip SinMarcar"
                    ? "tooltip Marcada"
                    : "tooltip SinMarcar";
                Luz_Boton(1);
              });
            } else cell.classList.add("hide");
          });
        });
      }

      // permite rellenar la celda de la tabla Movistar de verde, o de blanco
      var tabla = document.getElementById("Operador-Movistar");
      var old = "";
      if (tabla) {
        Array.from(tabla.rows).forEach((tr, rowIdx) => {
          Array.from(tr.cells).forEach((cell, cellIdx) => {
            if (cell.innerText != "") {
              cell.addEventListener("click", function () {
                this.className =
                  this.className == "tooltip SinMarcar"
                    ? "tooltip Marcada"
                    : "tooltip SinMarcar";
                Luz_Boton(1);
              });
            } else cell.classList.add("hide");
          });
        });
      }

      // permite rellenar la celda de la tabla Vodafone de verde, o de blanco
      var tabla = document.getElementById("Operador-Vodafone");
      if (tabla) {
        Array.from(tabla.rows).forEach((tr, rowIdx) => {
          Array.from(tr.cells).forEach((cell, cellIdx) => {
            if (cell.innerText != "") {
              cell.addEventListener("click", function () {
                this.className =
                  this.className == "tooltip SinMarcar"
                    ? "tooltip Marcada"
                    : "tooltip SinMarcar";
                Luz_Boton(1);
              });
            } else cell.classList.add("hide");
          });
        });
      }

      // permite rellenar la celda de la tabla Yoigo de verde, o de blanco
      var tabla = document.getElementById("Operador-Yoigo");
      if (tabla) {
        Array.from(tabla.rows).forEach((tr, rowIdx) => {
          Array.from(tr.cells).forEach((cell, cellIdx) => {
            if (cell.innerText != "") {
              cell.addEventListener("click", function () {
                this.className =
                  this.className == "tooltip SinMarcar"
                    ? "tooltip Marcada"
                    : "tooltip SinMarcar";
                Luz_Boton(1);
              });
            } else cell.classList.add("hide");
          });
        });
      }

      // Función para actualizar la tabla con el contenido del tooltiptext
      function actualizarInfoTable(tooltipText) {
        const infoContent = document.getElementById("infoContent");
        infoContent.innerHTML = tooltipText; // Actualiza el contenido de la tabla
      }

      // Agregar eventos mouseover a todas las celdas con tooltip
      document
        .querySelectorAll("table[id^='Operador-'] td.tooltip")
        .forEach((celda) => {
          celda.addEventListener("mouseover", function () {
            const tooltip = this.querySelector(".tooltiptext"); // Obtiene el tooltip de la celda
            if (tooltip) {
              actualizarInfoTable(tooltip.innerHTML); // Actualiza la tabla con el contenido del tooltip
            }
          });

          celda.addEventListener("mouseout", function () {
            // Opcional: Limpiar la tabla cuando el ratón sale de la celda
            actualizarInfoTable("");
          });
        });

      function hideMenu() {
        document.getElementById("contextMenu_Movistar").style.display = "none";
        document.getElementById("contextMenu_Orange").style.display = "none";
        document.getElementById("contextMenu_Vodafone").style.display = "none";
        document.getElementById("contextMenu_Yoigo").style.display = "none";
      }
      function rightClick1(e) {
        e.preventDefault();
        hideMenu();
        if (
          document.getElementById("contextMenu_Movistar").style.display ==
          "block"
        ) {
          hideMenu();
        } else {
          var menu = document.getElementById("contextMenu_Movistar");
          menu.style.display = "block";
          menu.style.left = e.pageX + "px";
          menu.style.top = e.pageY + "px";
        }
      }
      function rightClick2(e) {
        e.preventDefault();
        hideMenu();
        if (
          document.getElementById("contextMenu_Orange").style.display == "block"
        ) {
          hideMenu();
        } else {
          var menu = document.getElementById("contextMenu_Orange");
          menu.style.display = "block";
          menu.style.left = e.pageX + "px";
          menu.style.top = e.pageY + "px";
        }
      }

      function rightClick3(e) {
        e.preventDefault();
        hideMenu();
        if (
          document.getElementById("contextMenu_Vodafone").style.display ==
          "block"
        ) {
          hideMenu();
        } else {
          var menu = document.getElementById("contextMenu_Vodafone");
          menu.style.display = "block";
          menu.style.left = e.pageX + "px";
          menu.style.top = e.pageY + "px";
        }
      }

      function rightClick4(e) {
        e.preventDefault();
        hideMenu();
        if (
          document.getElementById("contextMenu_Yoigo").style.display == "block"
        ) {
          hideMenu();
        } else {
          var menu = document.getElementById("contextMenu_Yoigo");
          menu.style.display = "block";
          menu.style.left = e.pageX + "px";
          menu.style.top = e.pageY + "px";
        }
      }

      function Luz_Boton(X) {
        var boton = document.getElementById("BotonGenerador");
        if (X == 1) boton.className = "Boton_Encendido";
        if (X == 0) boton.className = "Boton_Apagado";
      }

      function Todo(O) {
        var tabla = document.getElementById(O);
        Luz_Boton(1);
        if (tabla) {
          Array.from(tabla.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              if (cell.innerText != "") {
                cell.className = "tooltip Marcada";
              }
            });
          });
        }
      }

      function DOSG(O) {
        var tabla = document.getElementById(O);
        var inversa = "";
        if (tabla) {
          Array.from(tabla.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              if (cell.innerText != "" && cellIdx == "0") {
                if (inversa == "") {
                  if (cell.className == "tooltip Marcada")
                    inversa = "tooltip SinMarcar";
                  else inversa = "tooltip Marcada";
                }
                cell.className = inversa;
              }
            });
          });
        }
        Luz_Boton(1);
      }

      function TRESG(O) {
        var tabla = document.getElementById(O);
        var inversa = "";
        if (tabla) {
          Array.from(tabla.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              if (cell.innerText != "" && cellIdx == "1") {
                if (inversa == "") {
                  if (cell.className == "tooltip Marcada")
                    inversa = "tooltip SinMarcar";
                  else inversa = "tooltip Marcada";
                }
                cell.className = inversa;
              }
            });
          });
        }
        Luz_Boton(1);
      }

      function CUATROG(O) {
        var tabla = document.getElementById(O);
        var inversa = "";
        if (tabla) {
          Array.from(tabla.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              if (cell.innerText != "" && cellIdx == "2") {
                if (inversa == "") {
                  if (cell.className == "tooltip Marcada")
                    inversa = "tooltip SinMarcar";
                  else inversa = "tooltip Marcada";
                }
                cell.className = inversa;
              }
            });
          });
        }
        Luz_Boton(1);
      }

      function CINCOG(O) {
        var tabla = document.getElementById(O);
        var inversa = "";
        if (tabla) {
          Array.from(tabla.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              if (cell.innerText != "" && cellIdx == "3") {
                if (inversa == "") {
                  if (cell.className == "tooltip Marcada")
                    inversa = "tooltip SinMarcar";
                  else inversa = "tooltip Marcada";
                }
                cell.className = inversa;
              }
            });
          });
        }
        Luz_Boton(1);
      }

      function EV_Movistar() {
        Borrar("Operador-Movistar");
        var table = document.getElementById("Operador-Movistar");
        table.rows[0].cells[0].className = "tooltip Marcada";

        table.rows[0].cells[1].className = "tooltip Marcada";
        table.rows[1].cells[1].className = "tooltip Marcada";
        table.rows[2].cells[1].className = "tooltip Marcada";
        table.rows[3].cells[1].className = "tooltip Marcada";
        table.rows[4].cells[1].className = "tooltip Marcada";
        table.rows[6].cells[1].className = "tooltip Marcada";
        table.rows[7].cells[1].className = "tooltip Marcada";

        table.rows[0].cells[2].className = "tooltip Marcada";
        //table.rows[3].cells[2].className = "tooltip Marcada";
        table.rows[6].cells[2].className = "tooltip Marcada";
        table.rows[8].cells[2].className = "tooltip Marcada";
        table.rows[9].cells[2].className = "tooltip Marcada";

        table.rows[0].cells[3].className = "tooltip Marcada";
        table.rows[4].cells[3].className = "tooltip Marcada";
        table.rows[8].cells[3].className = "tooltip Marcada";
        Luz_Boton(1);
      }
	  
	  
	  
	  
	  function Obligatorias_Movistar() {
        Borrar("Operador-Movistar");
        var table = document.getElementById("Operador-Movistar");
        table.rows[0].cells[0].className = "tooltip Marcada";
        // table.rows[1].cells[0].className = "tooltip Marcada";

        table.rows[0].cells[1].className = "tooltip Marcada";
        table.rows[1].cells[1].className = "tooltip Marcada";
        table.rows[2].cells[1].className = "tooltip Marcada";
        table.rows[3].cells[1].className = "tooltip Marcada";
        table.rows[4].cells[1].className = "tooltip Marcada";
        table.rows[6].cells[1].className = "tooltip Marcada";
        table.rows[7].cells[1].className = "tooltip Marcada";

        table.rows[0].cells[2].className = "tooltip Marcada";
        table.rows[3].cells[2].className = "tooltip Marcada";
        table.rows[6].cells[2].className = "tooltip Marcada";
        table.rows[8].cells[2].className = "tooltip Marcada";
        table.rows[9].cells[2].className = "tooltip Marcada";

        table.rows[0].cells[3].className = "tooltip Marcada";
        table.rows[4].cells[3].className = "tooltip Marcada";
        table.rows[8].cells[3].className = "tooltip Marcada";
        Luz_Boton(1);
      }
	  
	  

	function EV_Orange() {
        Borrar("Operador-Orange");
        var table = document.getElementById("Operador-Orange");
        table.rows[0].cells[0].className = "tooltip Marcada";
        table.rows[1].cells[0].className = "tooltip Marcada";

        table.rows[0].cells[1].className = "tooltip Marcada";
        table.rows[1].cells[1].className = "tooltip Marcada";
        table.rows[2].cells[1].className = "tooltip Marcada";
        table.rows[3].cells[1].className = "tooltip Marcada";

        table.rows[0].cells[2].className = "tooltip Marcada";
        table.rows[1].cells[2].className = "tooltip Marcada";
		table.rows[2].cells[2].className = "tooltip Marcada";
        table.rows[4].cells[2].className = "tooltip Marcada";
        table.rows[5].cells[2].className = "tooltip Marcada";
        table.rows[6].cells[2].className = "tooltip Marcada";
        table.rows[8].cells[2].className = "tooltip Marcada";

        table.rows[0].cells[3].className = "tooltip Marcada";
        table.rows[1].cells[3].className = "tooltip Marcada";
        table.rows[3].cells[3].className = "tooltip Marcada";
        // ha cambiado a poco frecuente table.rows[5].cells[3].className = "tooltip Marcada";
        table.rows[6].cells[3].className = "tooltip Marcada";
		table.rows[8].cells[3].className = "tooltip Marcada";
        Luz_Boton(1);
      }

      function Obligatorias_Orange() {
        Borrar("Operador-Orange");
        var table = document.getElementById("Operador-Orange");
        table.rows[0].cells[0].className = "tooltip Marcada";
		table.rows[1].cells[0].className = "tooltip Marcada";
       

        table.rows[0].cells[1].className = "tooltip Marcada";
        table.rows[1].cells[1].className = "tooltip Marcada";
        table.rows[2].cells[1].className = "tooltip Marcada";
        table.rows[3].cells[1].className = "tooltip Marcada";

        table.rows[0].cells[2].className = "tooltip Marcada";
        table.rows[1].cells[2].className = "tooltip Marcada";
        table.rows[4].cells[2].className = "tooltip Marcada";
        table.rows[5].cells[2].className = "tooltip Marcada";
        table.rows[6].cells[2].className = "tooltip Marcada";
        table.rows[8].cells[2].className = "tooltip Marcada";

        table.rows[0].cells[3].className = "tooltip Marcada";
        table.rows[1].cells[3].className = "tooltip Marcada";
        table.rows[3].cells[3].className = "tooltip Marcada";
        // ha cambiado a poco frecuente table.rows[5].cells[3].className = "tooltip Marcada";
        table.rows[6].cells[3].className = "tooltip Marcada";
		table.rows[8].cells[3].className = "tooltip Marcada";
        Luz_Boton(1);
      }


	function EV_Vodafone() {
        Borrar("Operador-Vodafone");
        var table = document.getElementById("Operador-Vodafone");
        table.rows[0].cells[0].className = "tooltip Marcada";
        //table.rows[1].cells[0].className = "tooltip Marcada";

        table.rows[0].cells[1].className = "tooltip Marcada";
        table.rows[1].cells[1].className = "tooltip Marcada";
        table.rows[2].cells[1].className = "tooltip Marcada";
        table.rows[3].cells[1].className = "tooltip Marcada";
        table.rows[4].cells[1].className = "tooltip Marcada";

        table.rows[1].cells[2].className = "tooltip Marcada";
        //table.rows[2].cells[2].className = "tooltip Marcada";
		table.rows[5].cells[2].className = "tooltip Marcada";
        table.rows[6].cells[2].className = "tooltip Marcada";
        table.rows[8].cells[2].className = "tooltip Marcada";
        table.rows[10].cells[2].className = "tooltip Marcada";

        table.rows[4].cells[3].className = "tooltip Marcada";
        table.rows[6].cells[3].className = "tooltip Marcada";
        table.rows[7].cells[3].className = "tooltip Marcada";
        table.rows[11].cells[3].className = "tooltip Marcada";
        Luz_Boton(1);
      }
	  
	  
      function Obligatorias_Vodafone() {
        Borrar("Operador-Vodafone");
        var table = document.getElementById("Operador-Vodafone");
        table.rows[0].cells[0].className = "tooltip Marcada";
        //table.rows[1].cells[0].className = "tooltip Marcada";

        table.rows[0].cells[1].className = "tooltip Marcada";
        table.rows[1].cells[1].className = "tooltip Marcada";
        table.rows[2].cells[1].className = "tooltip Marcada";
        table.rows[3].cells[1].className = "tooltip Marcada";
        table.rows[4].cells[1].className = "tooltip Marcada";

        table.rows[1].cells[2].className = "tooltip Marcada";
        table.rows[2].cells[2].className = "tooltip Marcada";
        table.rows[6].cells[2].className = "tooltip Marcada";
        table.rows[8].cells[2].className = "tooltip Marcada";
        table.rows[10].cells[2].className = "tooltip Marcada";

        table.rows[4].cells[3].className = "tooltip Marcada";
        table.rows[6].cells[3].className = "tooltip Marcada";
        table.rows[7].cells[3].className = "tooltip Marcada";
        table.rows[11].cells[3].className = "tooltip Marcada";
        Luz_Boton(1);
      }

      function Obligatorias_Yoigo() {
        Borrar("Operador-Yoigo");
        var table = document.getElementById("Operador-Yoigo");
        table.rows[0].cells[3].className = "tooltip Marcada";
        Luz_Boton(1);
      }

      function Borrar(O) {
        // pone en blanco todas las celdas de ese operador indicado
        var tabla = document.getElementById(O);
        if (tabla) {
          Array.from(tabla.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              cell.className = "tooltip SinMarcar";
              if (cell.innerText == "") cell.classList.add("hide");
            });
          });
        }
        Luz_Boton(1);
      }

      function Contar_Portadoras(S) {
        // le pasas un string con portadoras separadas por comas, y te devuelve el nº de portadoras
        if (S == "") {
          return 0;
        }
        return S.split(",").length - 1;
      }

      function Portadoras_Movistar() {
        // Agrupa y cuenta  portadoras (celdas verdes) de movistar por tecnologia
        var DOSG = "";
        var TRESG = "";
        var CUATROG = "";
        var CINCOG = "";

        var frecuencias = 0;
        var t = document.getElementById("Operador-Movistar");
        if (t) {
          Array.from(t.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              if (cell.innerText != "" && cell.className == "tooltip Marcada") {
                // aqui tengo una celda verde con contenido
                if (cellIdx == 0) {
                  DOSG = DOSG + cell.innerText + ",";
                  if (rowIdx == 0) {
                    // si fila =0 y celda 0 estamos en 2g 1º casilla
                    frecuencias = frecuencias + 74;
                  }
                }
                if (cellIdx == 1) {
                  TRESG = TRESG + cell.innerText + ",";
                }
                if (cellIdx == 2) {
                  CUATROG = CUATROG + cell.innerText + ",";
                }
                if (cellIdx == 3) {
                  CINCOG = CINCOG + cell.innerText + ",";
                }
              }
            });
          });
        }
        var t = document.getElementById("Portadoras_2G");
        t.rows[0].cells[0].innerText = DOSG.slice(0, -1);
        t.rows[0].cells[0].setAttribute("title", frecuencias);
        DOSG = "";

        var t = document.getElementById("Portadoras_3G");
        t.rows[0].cells[0].innerText = TRESG.slice(0, -1);
        t.rows[0].cells[0].setAttribute("title", Contar_Portadoras(TRESG));
        TRESG = "";

        var t = document.getElementById("Portadoras_4G");
        t.rows[0].cells[0].innerText = CUATROG.slice(0, -1);
        t.rows[0].cells[0].setAttribute("title", Contar_Portadoras(CUATROG));
        CUATROG = "";

        var t = document.getElementById("Portadoras_5G");
        t.rows[0].cells[0].innerText = CINCOG.slice(0, -1);
        t.rows[0].cells[0].setAttribute("title", Contar_Portadoras(CINCOG));
        CINCOG = "";
      }

      function Portadoras_Orange() {
        // Agrupa y cuenta  portadoras (celdas verdes) de Orange por tecnologia
        var DOSG = "";
        var TRESG = "";
        var CUATROG = "";
        var CINCOG = "";

        var frecuencias = 0;
        var t = document.getElementById("Operador-Orange");
        if (t) {
          Array.from(t.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              if (cell.innerText != "" && cell.className == "tooltip Marcada") {
                // aqui tengo una celda verde con contenido
                if (cellIdx == 0) {
                  DOSG = DOSG + cell.innerText + ",";
                  if (rowIdx == 0) {
                    // si fila =0 y celda 0 estamos en 2g 1º casilla
                    frecuencias = frecuencias + 23;
                  }
                  //2g 1800 orange 
                  if (rowIdx == 1) {
                  // si fila =1 y celda 0 estamos en 2g 2º casilla
                    frecuencias = frecuencias + 6;
                   }
                }
                if (cellIdx == 1) {
                  TRESG = TRESG + cell.innerText + ",";
                }
                if (cellIdx == 2) {
                  CUATROG = CUATROG + cell.innerText + ",";
                }
                if (cellIdx == 3) {
                  CINCOG = CINCOG + cell.innerText + ",";
                }
              }
            });
          });
        }

        var t = document.getElementById("Portadoras_2G");
        t.rows[0].cells[1].innerText = DOSG.slice(0, -1);
        t.rows[0].cells[1].setAttribute("title", frecuencias);
        DOSG = "";
        var t = document.getElementById("Portadoras_3G");
        t.rows[0].cells[1].innerText = TRESG.slice(0, -1);
        t.rows[0].cells[1].setAttribute("title", Contar_Portadoras(TRESG));
        TRESG = "";
        var t = document.getElementById("Portadoras_4G");
        t.rows[0].cells[1].innerText = CUATROG.slice(0, -1);
        t.rows[0].cells[1].setAttribute("title", Contar_Portadoras(CUATROG));
        CUATROG = "";
        var t = document.getElementById("Portadoras_5G");
        t.rows[0].cells[1].innerText = CINCOG.slice(0, -1);
        t.rows[0].cells[1].setAttribute("title", Contar_Portadoras(CINCOG));
        CINCOG = "";
      }

      function Portadoras_Vodafone() {
        // Agrupa y cuenta  portadoras (celdas verdes) de Vodafone por tecnologia
        var DOSG = "";
        var TRESG = "";
        var CUATROG = "";
        var CINCOG = "";
        var frecuencias = 0;

        var t = document.getElementById("Operador-Vodafone");
        if (t) {
          Array.from(t.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              if (cell.innerText != "" && cell.className == "tooltip Marcada") {
                // aqui tengo una celda verde con contenido
                if (cellIdx == 0) {
                  DOSG = DOSG + cell.innerText + ",";
                  if (rowIdx == 0) {
                    // si fila =0 y celda 0 estamos en 2g 1º casilla
                    frecuencias = frecuencias + 50;
                  }
                }
                if (cellIdx == 1) {
                  TRESG = TRESG + cell.innerText + ",";
                }
                if (cellIdx == 2) {
                  CUATROG = CUATROG + cell.innerText + ",";
                }
                if (cellIdx == 3) {
                  CINCOG = CINCOG + cell.innerText + ",";
                }
              }
            });
          });
        }

        var t = document.getElementById("Portadoras_2G");
        t.rows[0].cells[2].innerText = DOSG.slice(0, -1);
        t.rows[0].cells[2].setAttribute("title", frecuencias);
        DOSG = "";
        var t = document.getElementById("Portadoras_3G");
        t.rows[0].cells[2].innerText = TRESG.slice(0, -1);
        t.rows[0].cells[2].setAttribute("title", Contar_Portadoras(TRESG));
        TRESG = "";
        var t = document.getElementById("Portadoras_4G");
        t.rows[0].cells[2].innerText = CUATROG.slice(0, -1);
        t.rows[0].cells[2].setAttribute("title", Contar_Portadoras(CUATROG));
        CUATROG = "";
        var t = document.getElementById("Portadoras_5G");
        t.rows[0].cells[2].innerText = CINCOG.slice(0, -1);
        t.rows[0].cells[2].setAttribute("title", Contar_Portadoras(CINCOG));
        CINCOG = "";
      }

      function Portadoras_Yoigo() {
        // Agrupa y cuenta  portadoras (celdas verdes) de Yoigo por tecnologia
        var DOSG = "";
        var TRESG = "";
        var CUATROG = "";
        var CINCOG = "";
        var frecuencias = 0;

        var t = document.getElementById("Operador-Yoigo");
        if (t) {
          Array.from(t.rows).forEach((tr, rowIdx) => {
            Array.from(tr.cells).forEach((cell, cellIdx) => {
              if (cell.innerText != "" && cell.className == "tooltip Marcada") {
                // aqui tengo una celda verde con contenido
                if (cellIdx == 0) {
                  DOSG = DOSG + cell.innerText + ",";
                  if (rowIdx == 0) {
                    // si fila =0 y celda 0 estamos en 2g 1º casilla
                    frecuencias = frecuencias + 74;
                  }
                }
                if (cellIdx == 1) {
                  TRESG = TRESG + cell.innerText + ",";
                }
                if (cellIdx == 2) {
                  CUATROG = CUATROG + cell.innerText + ",";
                }
                if (cellIdx == 3) {
                  CINCOG = CINCOG + cell.innerText + ",";
                }
              }
            });
          });
        }

        var t = document.getElementById("Portadoras_2G");
        t.rows[0].cells[3].innerText = DOSG.slice(0, -1);
        t.rows[0].cells[3].setAttribute("title", frecuencias);
        DOSG = "";
        var t = document.getElementById("Portadoras_3G");
        t.rows[0].cells[3].innerText = TRESG.slice(0, -1);
        t.rows[0].cells[3].setAttribute("title", Contar_Portadoras(TRESG));
        TRESG = "";
        var t = document.getElementById("Portadoras_4G");
        t.rows[0].cells[3].innerText = CUATROG.slice(0, -1);
        t.rows[0].cells[3].setAttribute("title", Contar_Portadoras(CUATROG));
        CUATROG = "";
        var t = document.getElementById("Portadoras_5G");
        t.rows[0].cells[3].innerText = CINCOG.slice(0, -1);
        t.rows[0].cells[3].setAttribute("title", Contar_Portadoras(CINCOG));
        CINCOG = "";
      }

      function Suma_Portadoras(p) {
        // suma las portadoras de la tabla que se le indique
        var fila = 0;
        var sum = 0;
        var t = document.getElementById("Sumas");
        var u = document.getElementById(p);
        if (p == "Portadoras_2G") {
          // si son frecuencias de 2G las metemos directamente de los titulos de las celdas y salimos de la funcion
          sum =
            sum +
            Number(u.rows[0].cells[0].title) +
            Number(u.rows[0].cells[1].title) +
            Number(u.rows[0].cells[2].title) +
            Number(u.rows[0].cells[3].title);
          t.rows[fila].cells[0].innerText = sum;
          return;
        }
        if (p == "Portadoras_3G") {
          fila = 1;
        }
        if (p == "Portadoras_4G") {
          fila = 2;
        }
        if (p == "Portadoras_5G") {
          fila = 3;
        }

        for (let i = 0; i < 4; i++) {
          s = u.rows[0].cells[i].innerText;
          if (s != "") {
            sum = sum + s.split(",").length;
          }
          s = "";
        }

        t.rows[fila].cells[0].innerText = sum;
        // vemos si las portadoras de 3G o 4G o 5G puede superar el limite (12 o mas)

        if (fila == 3) {
          //si es 5G vemos si mas que 12
          if (sum > 12) t.rows[fila].cells[0].classList.add("blink");
          else t.rows[fila].cells[0].classList.remove("blink");
        } else {
          // si no es 5G vemos si es mas que 16
          if (sum > 16) t.rows[fila].cells[0].classList.add("blink");
          else t.rows[fila].cells[0].classList.remove("blink");
        }
      }

      function Suma_Totales() {
        // suma todas las portadoras de todas las tecnologias y Operadores
        var u = document.getElementById("Sumas");
        var i = 0;
        i =
          Number(u.rows[1].cells[0].innerText) +
          Number(u.rows[2].cells[0].innerText) +
          Number(u.rows[3].cells[0].innerText);
        u.rows[4].cells[0].innerText = i;
      }

      function Generar_Listado_Portadoras() {
        //Rellena las tablas finales segun las celdas seleccionadas
        Portadoras_Movistar();
        Portadoras_Orange();
        Portadoras_Vodafone();
        Portadoras_Yoigo();
        Suma_Portadoras("Portadoras_2G");
        Suma_Portadoras("Portadoras_3G");
        Suma_Portadoras("Portadoras_4G");
        Suma_Portadoras("Portadoras_5G");
        Suma_Totales();
        Luz_Boton(0);
      }

      function copyToClipboard(textToCopy) {
        var input = document.createElement("input");
        document.body.appendChild(input);
        input.value = textToCopy;
        input.select();
        document.execCommand("Copy");
        input.remove();
      }

      function Portapapeles_2G() {
        var t = document.getElementById("Portadoras_2G");
        var s = "";
        window.alert(
          "Comprobar que la decodificacion del Bsic en el scanner está limitada a -90db"
        );

        if (t) {
          s =
            t.rows[0].cells[0].innerText +
            "," +
            t.rows[0].cells[1].innerText +
            "," +
            t.rows[0].cells[2].innerText +
            "," +
            t.rows[0].cells[3].innerText;
          while (s.indexOf(",,", 0) != -1) {
            s = s.replace(",,", ",");
          }
          // s=s.slice(0,-1);
          if (s.indexOf(",", 0) == 0) {
            s = s.substring(1);
          }
          if (s.substr(-1) == ",") {
            s = s.slice(0, -1);
          }
          copyToClipboard(s);
        }
        s = "";
      }

      function Portapapeles_3G() {
        var t = document.getElementById("Portadoras_3G");
        var s = "";
        if (t) {
          s =
            t.rows[0].cells[0].innerText +
            "," +
            t.rows[0].cells[1].innerText +
            "," +
            t.rows[0].cells[2].innerText +
            "," +
            t.rows[0].cells[3].innerText;
          while (s.indexOf(",,", 0) != -1) {
            s = s.replace(",,", ",");
          }
          //s=s.slice(0,-1);
          if (s.indexOf(",", 0) == 0) {
            s = s.substring(1);
          }
          if (s.substr(-1) == ",") {
            s = s.slice(0, -1);
          }
          copyToClipboard(s);
        }
        s = "";
      }

      function Portapapeles_4G() {
        var t = document.getElementById("Portadoras_4G");
        var s = "";
        if (t) {
          s =
            t.rows[0].cells[0].innerText +
            "," +
            t.rows[0].cells[1].innerText +
            "," +
            t.rows[0].cells[2].innerText +
            "," +
            t.rows[0].cells[3].innerText;
          while (s.indexOf(",,", 0) != -1) {
            s = s.replace(",,", ",");
          }
          //s=s.slice(0,-1);
          if (s.indexOf(",", 0) == 0) {
            s = s.substring(1);
          }
          if (s.substr(-1) == ",") {
            s = s.slice(0, -1);
          }
          copyToClipboard(s);
        }
        s = "";
      }

      function Portapapeles_5G() {
        var t = document.getElementById("Portadoras_5G");
        var s = "";
        window.alert(
          "Haced un Band Scan previo, por si hay alguna que se escape"
        );
        if (t) {
          s =
            t.rows[0].cells[0].innerText +
            "," +
            t.rows[0].cells[1].innerText +
            "," +
            t.rows[0].cells[2].innerText +
            "," +
            t.rows[0].cells[3].innerText;
          while (s.indexOf(",,", 0) != -1) {
            s = s.replace(",,", ",");
          }
          //s=s.slice(0,-1);
          if (s.indexOf(",", 0) == 0) {
            s = s.substring(1);
          }
          if (s.substr(-1) == ",") {
            s = s.slice(0, -1);
          }
          copyToClipboard(s);
        }
        s = "";
      }

      // URLs de los logotipos
      const logos = {
        "Operador-Movistar":
          "https://upload.wikimedia.org/wikipedia/commons/5/55/Movistar_isotype_2020.svg",
        "Operador-Orange":
          "https://upload.wikimedia.org/wikipedia/commons/c/c8/Orange_logo.svg",
        "Operador-Vodafone":
          "https://upload.wikimedia.org/wikipedia/en/archive/c/cc/20180622104752%21Vodafone_2017_logo.svg",
        "Operador-Yoigo":
          "https://upload.wikimedia.org/wikipedia/commons/6/66/Yoigo_morado.svg",
      };

      // Función para agregar logotipos a los tooltips
      function agregarLogotipos() {
        const operadores = [
          "Operador-Movistar",
          "Operador-Orange",
          "Operador-Vodafone",
          "Operador-Yoigo",
        ];
        operadores.forEach((operador) => {
          const tabla = document.getElementById(operador);
          if (tabla) {
            const celdas = tabla.querySelectorAll(".tooltiptext");
            celdas.forEach((tooltip) => {
              const img = document.createElement("img");
              img.src = logos[operador];
              img.alt = `Logo de ${operador.split("-")[1]}`;
              img.style.maxWidth = "50px"; // Limita el ancho máximo
              img.style.maxHeight = "50px"; // Limita el alto máximo
              img.style.width = "auto"; // Mantiene la proporción
              img.style.height = "auto"; // Mantiene la proporción
              tooltip.insertBefore(img, tooltip.firstChild);
            });
          }
        });
      }

      //****************************************

      document.addEventListener("DOMContentLoaded", function () {
        // Configuración personalizada para las celdas de la tabla sombra
        const configuracionSombra = {
          topOffset: -12, // Ajuste vertical (puedes cambiarlo)
          leftOffset: -15, // Ajuste horizontal (puedes cambiarlo)
          widthOffset: 10, // Ajuste de ancho (puedes cambiarlo)
          heightOffset: 10, // Ajuste de alto (puedes cambiarlo)
        };

        // Crear la tabla sombra para una tabla original
        const crearTablaSombra = (tablaOriginal) => {
          const tablaSombra = document.createElement("table");
          tablaSombra.classList.add("tabla-sombra");
          tablaSombra.style.position = "absolute";
          tablaSombra.style.borderSpacing =
            window.getComputedStyle(tablaOriginal).borderSpacing;
          tablaSombra.style.zIndex = "-1"; // Colocar la tabla en una capa inferior
          tablaSombra.style.pointerEvents = "none"; // Evita interferencias
          tablaSombra.style.display = "none"; // Ocultar por defecto

          // Copiar la estructura de la tabla original
          Array.from(tablaOriginal.rows).forEach((filaOriginal) => {
            const filaSombra = document.createElement("tr");
            Array.from(filaOriginal.cells).forEach((celdaOriginal) => {
              const celdaSombra = document.createElement("td");
              celdaSombra.style.border = "none";
              celdaSombra.style.borderRadius = "1px";
              celdaSombra.style.boxShadow = "5px 5px 5px #ccc";
              celdaSombra.style.backgroundColor = " #b3b6b7 ";

              celdaSombra.style.visibility = "hidden"; // Ocultar todas las celdas por defecto

              // Posicionar y ajustar el tamaño de la celda sombra
              const rect = celdaOriginal.getBoundingClientRect();
              celdaSombra.style.position = "absolute";
              celdaSombra.style.top = `${
                rect.top + window.scrollY + configuracionSombra.topOffset
              }px`;
              celdaSombra.style.left = `${
                rect.left + window.scrollX + configuracionSombra.leftOffset
              }px`;
              celdaSombra.style.width = `${
                rect.width + configuracionSombra.widthOffset
              }px`;
              celdaSombra.style.height = `${
                rect.height + configuracionSombra.heightOffset
              }px`;

              filaSombra.appendChild(celdaSombra);
            });
            tablaSombra.appendChild(filaSombra);
          });

          // Insertar la tabla sombra en el DOM, justo después de la tabla original
          tablaOriginal.parentElement.insertBefore(
            tablaSombra,
            tablaOriginal.nextSibling
          );

          return tablaSombra;
        };

        // Asignar eventos a las celdas de la tabla original
        document
          .querySelectorAll("table[id^='Operador-']")
          .forEach((tablaOriginal) => {
            const tablaSombra = crearTablaSombra(tablaOriginal);

            Array.from(tablaOriginal.rows).forEach((filaOriginal, rowIndex) => {
              Array.from(filaOriginal.cells).forEach(
                (celdaOriginal, cellIndex) => {
                  // Obtener el tooltip de la celda original
                  const tooltip = celdaOriginal.querySelector(".tooltiptext");

                  if (tooltip && celdaOriginal.innerText.trim() !== "") {
                    // Asignar eventos de mouseover y mouseout
                    celdaOriginal.addEventListener("mouseover", () => {
                      // Obtener la frecuencia del tooltip
                      const textotooltip = tooltip.textContent.trim();
                      let frecuencia = "";

                      if (/\b2100\b/.test(textotooltip)) {
                        frecuencia = "2100";
                      } else if (/\b1800\b/.test(textotooltip)) {
                        frecuencia = "1800";
                      } else if (/\b900\b/.test(textotooltip)) {
                        frecuencia = "900";
                      } else if (/\b800\b/.test(textotooltip)) {
                        frecuencia = "800";
                      } else if (/\b700\b/.test(textotooltip)) {
                        frecuencia = "700";
                      } else if (/\b3500\b/.test(textotooltip)) {
                        frecuencia = "3500";
                      } else if (/\b2600\b/.test(textotooltip)) {
                        frecuencia = "2600";
                      }
                      // Mostrar solo las celdas de la tabla sombra que coincidan con la frecuencia
                      Array.from(tablaSombra.rows).forEach((filaSombra) => {
                        Array.from(filaSombra.cells).forEach((celdaSombra) => {
                          celdaSombra.style.visibility = "hidden"; // Ocultar todas las celdas primero
                        });
                      });

                      if (frecuencia) {
                        // Mostrar solo las celdas de la tabla sombra que coincidan con la frecuencia
                        Array.from(tablaSombra.rows).forEach(
                          (filaSombra, rowIndexSombra) => {
                            Array.from(filaSombra.cells).forEach(
                              (celdaSombra, cellIndexSombra) => {
                                const tooltipSombra =
                                  tablaOriginal.rows[rowIndexSombra].cells[
                                    cellIndexSombra
                                  ].querySelector(".tooltiptext");
                                if (tooltipSombra) {
                                  const regex = new RegExp(
                                    `\\b${frecuencia}\\b`
                                  );
                                  if (regex.test(tooltipSombra.textContent)) {
                                    // Código si se encuentra la frecuencia exacta
                                    celdaSombra.style.visibility = "visible";
                                  }
                                }
                              }
                            );
                          }
                        );
                      }

                      // Mostrar la tabla sombra
                      tablaSombra.style.display = "table";
                    });

                    celdaOriginal.addEventListener("mouseout", () => {
                      // Ocultar la tabla sombra al salir de la celda
                      tablaSombra.style.display = "none";
                    });
                  }
                }
              );
            });
          });
      });

      //**************************************

      document.addEventListener("DOMContentLoaded", function () {
        const toggleCheckbox = document.getElementById("togglePopUpInfo");
        const infoTable = document.getElementById("infoTable");

        // Función para activar/desactivar popups y tabla de info
        function togglePopUpInfo() {
          const isChecked = toggleCheckbox.checked;

          // Activar/desactivar la tabla de info
          infoTable.style.display = isChecked ? "block" : "none";

          // Desactivar/activar los popups
          document
            .querySelectorAll("table[id^='Operador-'] td.tooltip")
            .forEach((celda) => {
              const tooltip = celda.querySelector(".tooltiptext");
              if (tooltip) {
                if (isChecked) {
                  // Desactivar los popups
                  celda.removeEventListener("mouseover", showtooltip);
                  celda.removeEventListener("mouseout", hidetooltip);
                  tooltip.style.visibility = "hidden"; // Asegurarse de que el tooltip esté oculto
                  infoContent.style.visibility = "visible";
                } else {
                  // Activar los popups
                  celda.addEventListener("mouseover", showtooltip);
                  celda.addEventListener("mouseout", hidetooltip);
                }
              }
            });
        }

        // Función para mostrar el tooltip
        function showtooltip() {
          const tooltip = this.querySelector(".tooltiptext");
          if (tooltip) {
            tooltip.style.visibility = "visible";
            tooltip.style.opacity = "1";
          }
        }

        // Función para ocultar el tooltip
        function hidetooltip() {
          const tooltip = this.querySelector(".tooltiptext");
          if (tooltip) {
            tooltip.style.visibility = "hidden";
            tooltip.style.opacity = "0";
          }
        }

        // Asignar el evento al checkbox
        toggleCheckbox.addEventListener("change", togglePopUpInfo);

        // Inicializar el estado según la casilla
        togglePopUpInfo();

        function moverInfoTable(event, operador) {
          const infoTable = document.getElementById("infoTable");
          if (infoTable) {
            infoTable.style.top = "300px";
            // Ajusta la posición de la infoTable según el operador
            switch (operador) {
              case "Operador-Movistar":
                infoTable.style.left = "380px"; // Posición para Movistar
                break;
              case "Operador-Orange":
                infoTable.style.left = "790px"; // Posición para Orange
                break;
              case "Operador-Vodafone":
                infoTable.style.left = "1190px"; // Posición para Vodafone
                break;
              case "Operador-Yoigo":
                infoTable.style.left = "1490px"; // Posición para Yoigo
                break;
              default:
                infoTable.style.left = "50%"; // Posición por defecto (centrada)
            }
          }
        }

        // Asignar eventos a las tablas de operadores
        const operadores = [
          "Operador-Movistar",
          "Operador-Orange",
          "Operador-Vodafone",
          "Operador-Yoigo",
        ];
        operadores.forEach((operador) => {
          const tabla = document.getElementById(operador);
          if (tabla) {
            tabla.addEventListener("mouseover", (event) =>
              moverInfoTable(event, operador)
            );
          }
        });
      });

      // Ejecutar al cargar la página
      window.onload = function () {
        agregarLogotipos();
      };
    </script>
  </body>
</html>
