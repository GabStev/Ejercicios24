Ejercicios24
============

24 ejercicios de Web
<?php // Ejercicio Nº 2

function serie2($x=26,$y=3)
 {
           $contador=0;
           $result=$x;
           $i=1;
           if(($x>255 ||  $x<0  ) || ($y>255 || $y<0))
           {
               echo"</br>". -1;
           }
              else {
                      do  {
                            $result=$result*$i;
                           $contador=$contador+1;
                           $i++;
                           }
                    while($contador!=$y);
                     echo"</br>".$result;
              }                                
    }
    
echo serie2();

?>


<?php //Ejercicio N° 5
  function eliminaduplicados($entrada=array())
  {
    $entrada = array( 2,4,5,6,8,4,6,8,9,10);
    $resultado = array_unique($entrada);   //array_unique elimina valores duplicados de un array
    echo"</br>";
    var_dump ($resultado);                 // var_dump muestra información sobre una variable.
    
  }
  
echo eliminaduplicados();
?>


<?php // Ejercicio N° 8
 
function buscara($cadena)
{ 
    $contador=0;
    for($i=0;$i<=strlen($cadena)-1; $i++)  //strlen devuelve la longitud de una cadena
    {
       if (($cadena[$i] == 'a' ) || ($cadena[$i] == 'A' ))
       {
            $contador++;
       }
    }
    return $contador;
}
    
 $cadena="Hola Ana como estas";
 echo"</br>"."La  " .$cadena.  "    tiene   ". buscara($cadena).  "    a";
?>

<?php //Ejercicio N° 11
function contarelementosrepetidos($array)
{
     $repetido = array();
 
    foreach( (array)$array as $valor )
    {
        $encontrado = false;
 
        foreach( $repetido as $i => $numero )
        {
            if( $numero['numero'] === $valor )
            {
               $encontrado = true;
               $repetido[$i]['repetido']++;
            }
     
        }
 
        if( false === $encontrado )
        {
            $i = count($repetido);
            $repetido[$i] = array();
            $repetido[$i]['numero'] = $valor;
            $repetido[$i]['repetido'] = 1;
        }
   
    }   
return $repetido;
   
}

$matriz = array(1,1,2,3,4,5,6,7,8,9,2,3,45,6);
 
echo"</br>";
echo "Elemente mayormente repetido</br>";

print_r(contarelementosrepetidos($matriz)) ;echo"</br>"; //todavia no esta bien hecho.

?>
<?php //ejercicio N° 14
function invierteserie($x,$y)
{
  
    $contador=0;
    $z=4;
     if(($x>255 ||  $x<0  ) || ($y>255 || $y<0))
     {
        return -1;
     }
    else
    {  
    do{
       $valor=$x.$y;
       $invertido=$y.$x;
       $x=$x+1;
       $y=$y+1; 
       $contador=$contador+1;
    }while($contador!=$z);
      
    }
   
 return$valor .$invertido; 
 
}
$x=10;
$y=12;
echo invierteserie($x,$y);

?>
<?php //Ejercicio Nº 17
function convertiraentero($variable)
{  
    if(($variable=="uno") || ($variable=="UNO") || ($variable=="Uno") )
    {
        return 1;
    }
     if(($variable=="dos") || ($variable=="DOS") || ($variable=="Dos") )
    {
        return 2;
    }
     if(($variable=="tres") || ($variable=="TRES") || ($variable=="Tres") )
    {
        return 3;
    }
     if(($variable=="cuatro") || ($variable=="CUATRO") || ($variable=="Cuatro") )
    {
        return 4;
    }
     if(($variable=="cinco") || ($variable=="CINCO") || ($variable=="Cinco") )
    {
        return 5;
    }
}
$variable="uno";
echo"</br>".  convertiraentero($variable);
?>

<?php //Ejercicio Nº 1
$x = 8; 
$y = 9;

$resultadofinal = calcularnumero($x,$y);
echo "El resultado es ".$resultadofinal;

function calcularnumero($x,$y){
    $numero1 = 0;
    $numero2 = 0;
    $resultado = -1;
    $num1 = 7;
    $num2 = 6;
    if ($x > 255 || $y > 255 || $x <= 0 || $y <= 0) {
        return $resultado;
    } 
    else{
        for ($i = 1; $i <= $x; $i++)
        {
            if ($i == 1)
            {
                $numero1 = $num1;
            }
            if ($i == 2)
            {
                $numero1 = $num2;
            }
            if ($i > 2)
            {
                if ($i % 2 != 0)
                {
                    $num1 = $num1 + 1;
                    $numero1 = $num1;
                }
                else
                {
                    $num2 = $num2 - 2;
                    $numero1 = $num2;
                }
            }
        }
        $num1 = 7;
        $num2 = 6;
        for ($j = 1; $j <= $y; $j++)
        {
            if ($j == 1)
            {
                $numero2 = $num1;
            }
            if ($j == 2)
            {
                $numero2 = $num2;
            }
            if ($j > 2)
            {
                if ($j % 2 != 0)
                {
                    $num1 = $num1 + 1;
                    $numero2 = $num1;
                }
                else
                {
                    $num2 = $num2 - 2;
                    $numero2 = $num2;
                }
            }
        }
        $resultado = $numero1 + $numero2;
        return $resultado;
    }        
}

?>
