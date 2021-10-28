# factura
crear una factura con php y css
<!DOCTYPE html>
<html>
    <head>

        <title>Formulario</title>

        <meta charset="UTF-8">

        <style>

           .contenedor{
               position: relative;
               width: 69%;
               height: 70%;
               padding-left: 20px;
               padding-top: 15px;
               background-color: hsl(175, 77%, 66%);
               margin: auto;
            }

                table{
                    border: 2px solid #000000;
                    margin-bottom: 10px;
                    border-collapse: collapse;
                    color: #000000;
                    background-color: #75ffa3;
                    width: 95%;
                }

                th{
                    background-color: hsl(352, 83%, 72%);
                    font-family: Georgia, Times, 'Times New Roman', serif;
                    height:10px;
                }


           textarea{
               resize: none;
           }

           input[type=submit]{
               position: relative;
               width: 150px;
               height: 40px;
               margin-left: 430px;
           }
        </style>

    </head>

    <body>

        <div class="contenedor">

        <form action="proceso.php" method="POST">
            
            <table>
                
        <tr>

            <th colspan="4" align="right" style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);">ORDEN DE COMPRA</th>
    
            </tr>
    
            <tr>

                    <td> Nombre de Empresa  :</td><td><input type="text"  name="empresa"  placeholder="Nombre de la Empresa"></td>
                    <td> FECHA : </td><td><input type="date"  name="fecha"></td>
            
                </tr>
                
        <tr>

            <td>Logo De Empresa : </td><td><input type="file" id="logo" name="logo"></td>
            <td>Número de Orden :</td><td><input type="number" id="orden" name="orden"placeholder="Ingrese cuatro digitos"></td>
        
        </tr>

        <tr>

        <td> Dirección : </td><td colspan="3"><input type="text"  name="direccion"  placeholder="Ingrese la Dirección"></td>
    
        </tr>

        <tr>

        <td> Teléfono : </td><td colspan="3"><input type="tel" id="telefono" name="telefono"  placeholder="(+56)956981323"></td>
    
        </tr>

    <tr>

        <td> E-mail : </td><td colspan="3"><input type="email"id="mail" name="mail"placeholder="correo electrónico"></td>
    
    </tr>

    <tr>

        <td> Sitio Web : </td><td colspan="3"><input type="url"id="sitioweb" name="sitioweb" placeholder="¿Tienes un sitio web?"></td>
    
    </tr>

    </table>
    
    <table  class="tabla_2">

        <tr>

            <th colspan="2" style="border-right:2px solid rgba(0,0,0);"> VENDEDOR </th>
            <th colspan="2" style="border-right:2px solid rgba(0,0,0);"> ENVIAR A </th> 
       
        </tr>

        <tr>
            
            <td> Nombre De Empresa : </td><td style="border-right:2px solid rgba(0,0,0);"><input type="text" id="empresa_vendedor" name="empresa_vendedor"  placeholder="Nombre de la Empresa"></td>
            <td > Nombre  : </td><td style="border-right:2px solid rgba(0,0,0);"><input type="name" id="nombre_de_envio" name="nombre_de_envio"  placeholder="Nombre completo"></td>
        
        </tr>

        <tr>

            <td> Contacto o Departamento : </td><td style="border-right:2px solid rgba(0,0,0);"><input type="text" id="contacto_vendedor" name="contacto_vendedor" placeholder="Contacto"></td>
            <td> Nombre De Empresa : </td><td style="border-right:2px solid rgba(0,0,0); "><input type="text" id="empresa_envio" name="empresa_envio"  placeholder="Nombre de la Empresa"></td>
        
        </tr>

        <tr>

            <td> Dirección : </td><td style="border-right:2px solid rgba(0,0,0);"><input type="text" id="direccion_de_vendedor" name="direccion_de_vendedor"  placeholder="Ingrese la Dirección"></td>
            <td> Dirección : </td><td style="border-right:2px solid rgba(0,0,0);"><input type="text" id="direccion_envio" name="direccion_envio"  placeholder="Ingrese la Dirección"></td>
        
        </tr>

        <tr>
            
            <td> Teléfono : </td><td style="border-right:2px solid rgba(0,0,0);"><input type="tel" id="telefono_vendedor" name="telefono_vendedor"  placeholder="(+56)956981323"></td>
            <td> Teléfono : </td><td style="border-right:2px solid rgba(0,0,0);"><input type="tel" id="telefono_envio" name="telefono_envio"  placeholder="(+56)956981323"></td>
        
        </tr>

        <tr>

            <td> E-mail : </td><td style="border-right:2px solid rgba(0,0,0);"><input type="email"id="mail_vendedor" name="mail_vendedor"placeholder="correo electrónico"></td>
            <td> E-mail : </td><td style="border-right:2px solid rgba(0,0,0);"><input type="email"id="mail_envio" name="mail_envio"placeholder="correo electrónico"></td>
        
        </tr>
    
    </table>
    
    <table class="tabla_3">

        <tr>

        <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Enviado Mediante </th>
        <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> F.O.B</th>
        <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Condiciones de Envío </th>
    
    </tr>

    <tr>

        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><textarea name="texto1"  rows="6" cols="37"placeholder="Escriba algo"></textarea></td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><textarea name="texto2"  rows="6" cols="37"placeholder="Escriba algo"></textarea></td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><textarea name="texto3"   rows="6" cols="37"placeholder="Escriba algo"></textarea></td>
    
    </tr>

    </table>

    <table class="tabla_4">

        <tr>

            <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> ARTICULO # </th>
            <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> DESCRIPCIÓN</th>
            <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> CANTIDAD </th>
            <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> P/U </th>
            <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> TOTAL </th>
        
        </tr>

        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>

        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>

        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>
        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>
        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>
        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>
        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>
        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>
        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>
        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="articulo[]" placeholder="Nombre del Articulo"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="text" name="descripcion[]" placeholder="Descripción"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="cantidad[]" placeholder="Cantidad"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><input type="number" name="precio[]" placeholder="Precio"></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
        
        </tr>
    <tr>
        
        <th colspan="3" style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Condiciones o Instrucciones Especiales </th>
        <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Subtotal </th>
        <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> </th>
    
    </tr>

    <tr>

     <td colspan="3" rowspan="4" style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><textarea name="condiciones" rows="6" cols="67"placeholder="Escriba algo"></textarea></td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> % Iva </td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
    
    </tr>

    <tr>

        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Envio</td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
    </tr>

    <tr>

        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Otro </td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
    
    </tr>

    <tr>

        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> TOTAL </td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
    
    </tr> 

    </table>

                      <input type="submit" value="Enviar">
                      
                      <p> Si tiene alguna duda sobre esta orden de compra , por favor ,pónganse en contacto con :katalinasepulvedalopez@gmail.com</p>
            
        </form>
    
    </div>

    </body>

</html>
