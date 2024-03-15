# **Rélogio**

## ``Índice``

* [Estrutura do HTML](#estrutura-do-html)

## ``Relógio Digital``

Este é um código simples em JavaScript que cria um relógio digital. Ele exibe a hora atual e atualiza a cada meio segundo.

## ``Como funciona``

* A função startTime() é responsável por obter a hora atual e atualizar a exibição do relógio.
* Dentro de startTime(), um novo objeto Date é criado para obter a data e hora atuais.
* As horas, minutos e segundos são extraídos do objeto Date.
* A função checkTime() é chamada para garantir que horas, minutos e segundos de um único dígito sejam prefixados com '0'.
* A exibição do relógio é atualizada definindo o innerHTML do elemento com o id "txt" para a hora formatada.
* setTimeout() é usado para chamar startTime() recursivamente a cada 500 milissegundos (meio segundo), garantindo que o relógio seja atualizado continuamente.

## ``Funções``

* startTime(): Obtém a hora atual, formata-a e atualiza a exibição do relógio.
* checkTime(i): Adiciona um zero à esquerda se o valor do tempo for menor que 10.

## ``Estrutura do HTML``

```html

<!-- Código HTML -->
<!DOCTYPE html>
<html>
<head>
    <title>Relógio Digital</title>
</head>
<body>

<div id="txt"></div>

<script type="text/javascript">
      <script type="text/javascript">
      function startTime()
      {
      var today=new Date();
      var h=today.getHours();
      var m=today.getMinutes();
      var s=today.getSeconds();
      // add a zero in front of numbers<10
      m=checkTime(m);
      s=checkTime(s);
      document.getElementById('txt').innerHTML=h+":"+m+":"+s;
      t=setTimeout('startTime()',500);
      
      }
      
      function checkTime(i)
      {
      if (i<10)
        {
        i="0" + i;
        }
      return i;
      }
      </script>
      

      <div id="txt">
      <script type="text/javascript">document.write(startTime())</script>
      </div>
</script>

</body>
</html>
```

## ``Nota``
Certifique-se de que o elemento com o id "txt" exista em seu código HTML, caso contrário, o relógio não será exibido corretamente.




