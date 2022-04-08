# java

## Fundamentos

>Aula 20/21. Variáveis e constantes.

Transformar graus fahrenheit em graus celsius.

Formula do (°F - 32) x 5/9  = °C

A palavra **final** é uma palavra reservada que não da para alterar o valor.

```java
package fundamentos;

public class AreaCircunferencia {
    public static void main(String[] args) {

        final double FATOR = 5.0/9.0;
        final double ajuste = 32;
        
        double fahrenheit  = 86;
        double celsius = (fahrenheit  - ajuste) * FATOR;
        System.out.println("O resultado é " + celsius + "°C.");
        
        fahrenheit  = 100;
        celsius = (fahrenheit  - ajuste) * FATOR;
        System.out.println("O resultado é " + celsius + "°C.");
    }
}

```

>Aula 21. Desafio variáveis e constantes.

Resposta; transformar graus fahrenheit em graus celsius.

```java
package fundamentos;

public class InferênciaDeTipos {
    public static void main(String[] args) {
        double a = 4.5; //o Double tem que ter um ponto e um numero depois
        System.out.println(a);
        
        a = 12; // caso n tenho o ponto e um numero depois ele adiciona o .0
        System.out.println(a);
        
        var b = 6.5; // o var ele indetificar se é numero ou texto
        System.out.println(b);
        
        b = 10; //Quando é numero não pode ser texto
        System.out.println(b);
        
        var c ="texto"; //Quando é texto não pode ser numero
        System.out.println(c);
        
        c = "novo texto";
        System.out.println(c);
        
        double d; // variavel  declarada
        d = 123.77; //variavel inicialziada
        System.out.println(d); //usada
        // Com o Var não é permitido usar esse metodo
    }
}
```

>Aula 24/25 Tipos primitivos.

```java
public class Tipos_Primitivos {
    public static void main(String[] args) {
          byte tipoByte = 127;
          short tipoShort = 32767;
          char tipoChar = 'C';
          float tipoFloat = 2.6f;
          double tipoDouble = 3.59;
          int tipoInt = 2147483647;
          long tipoLong = 9223372036854775807L;
          boolean tipoBooleano = true;
          System.out.println("Valor do tipoByte = " + tipoByte);
          System.out.println("Valor do tipoShort = " + tipoShort);
          System.out.println("Valor do tipoChar = " + tipoChar);
          System.out.println("Valor do tipoFloat = " + tipoFloat);
          System.out.println("Valor do tipoDouble = " + tipoDouble);
          System.out.println("Valor do tipoInt = " + tipoInt);
          System.out.println("Valor do tipoLong = " + tipoLong);
          System.out.println("Valor do tipoBooleano = " + tipoBooleano);
    }
}
```

```java
package fundamentos;

 

public class tiposPrimitivos {
    public static void main(String[] args) {
        // informações do funcionario
        byte anosDeEmpresa =  23;
        short numerosDeVoou = 32766;
        int id = 56789;
        long pontosAcumulados = 4_134_832_223L; // quando vc adiciona o L vc mostra que é um numero longo de long
        
        //tipos numericos reais
        float salario = 11_445.44F; // todos os numeros float tem que terminar com F
        double vendasAcumuladas = 2_991_797_103.01;
        
        // tipos booleano, retorna apenas true ou false
        boolean estadoDeFerias = true; //false
        
        
        //tipos de caractere
        char status = 'A'; //acc apenas uma letra ou caractere ex: ; / = - [ p
        
        
    }
} 
```

>Aula 26. Notação ponto.

```java package Fundamentos;

public class NotaçãoPonto {
    public static void main(String[] args) {
        
        String s = "Bom dia, X!";
        s = s.replace("X", "Luzia"); // Ele faz a substituição do que está escrito 
        s = s.toUpperCase(); //ToUpperCase deixa as letras maiúsculas 
        s = s.concat("!!!!"); /// ele vai concatenar (juntar) o que for escrito.
        System.out.println(s);
        
        //String concatena com String
        String x = "leo".toUpperCase();
        System.out.println(x);
        String y = "Bom dia, X!"
                .replace("X", "phelipe") // Subjstitui uma letra ou ponto por virgula
                .toUpperCase()
                .concat(" Namorado da luzia");
        System.out.println(y);
        
        //tipos primitivos não tem "."

    }

}
```

>Aula 27. Import.

```java
package fundamentos;

import java.util.Date;

//import javax.swing.JButton;



public class Import {
    public static void main(String[] args) {
        String s = "bom dia";
        System.out.println(s);
        
        Date a = new Date();
        System.out.println(a);
        
        
        //JButton botao = new JButton();
    }
}
```

>Aula 28. Tipo  de String.

```java
    package fundamentos;
        
    public class TipoDeString {
        public static void main(String[] args) {
            System.out.println("Olá pessoal".charAt(2)); // o charAt é usado para identificar onde que fica tal letra
            
            String s = "boa tarde"; // vc pode substituir o valor original mas não pode modificar o valor original
            s = "bom dia"; // aqui estou substituindo e não modificando o valor original
            s = s.toUpperCase();
            System.out.println(s.concat("!!!!"));   
            System.out.println(s + "!!!!!!!"); /// MSM COISA DA DE CIMA 
            System.out.println(s.startsWith("boa")); // startsWith, só retorna 2 valores, true ou false
            System.out.println(s.startsWith("BOM")); // LEMBRANDO QUE AQUI USEI toUppercase
            System.out.println(s.length()); // tamanho 
            System.out.println(s.endsWith("DIA")); // pergunta se no final termina com o que vc determinar
            System.out.println(s.equalsIgnoreCase("bom dia"));  //ele ignora no ToUpperCase
            
            var nome = "pedro";
            var sobreNome = "augusto";
            var idade = 23;
            var salario = 12321.13;
            
            System.out.printf("O senhor %s %s tem %d anos e ganha R$: %.2f", nome,sobreNome, idade, salario); 
            
            //    \n quebra a linha
            
            String frase = String.format("\nO senhor %s %s tem %d anos e ganha R$: %.2f", nome,sobreNome, idade, salario);
            System.out.println(frase);
        }
    }

```

>Aula 29. Console.

```java
%d  representa números inteiros

%f  representa números floats

%2f representa números doubles

%b  representa valores booleanos

%c  representa valores char
 ```

```java

package fundamentos;

import java.util.Scanner;

public class Console {
    public static void main(String[] args) {
        System.out.print("bom ");
        System.out.print(" dia");
        
        System.out.println(" bom dia");
        System.out.printf("Megasena: %d %d %d %d %n", 1, 2, 3, 4);
        System.out.printf("Salario: %.1f%n", 1234.567);
        
        Scanner entrada = new Scanner(System.in);
        System.out.print("Digite seu nome: ");
        String nome = entrada.nextLine();
        
        System.out.print("Digite seu sobrenome: ");
        String sobrenome = entrada.nextLine();
        
        System.out.print("Digite sua idade: ");
        int idade = entrada.nextInt();
        
        // %S usa em string  %d em double  %n quebra a linha 
        
        System.out.printf("%s %s tem %d anos.%n", nome, sobrenome, idade);
        
        entrada.close();
    }
}
```

>Aula 31. Objeto vs Primitivo.

```java

package fundamentos;

public class ObjetoVsPrimitivo {
    public static void main(String[] args) {
        String s = new String("texto");
        s = s.toUpperCase();
        System.out.println(s);
        
        //wrappers   são a versão objeto dos tiposprimitivos
        int a = 123;
        System.out.println(a);
    }

}
 ```

>Aula 32. Wrappers.

Tradução: embrulho.

```java
package fundamentos;

public class Wrapper {
    public static void main(String[] args) {
        //byte
        Byte b = 100;
        Short s = 1000;
        // integer.parseInt(entrada.next());
        Integer i = 10000;  //int
        long l = 100000L;
        
        System.out.println(b.byteValue());
        System.out.println(s.toString());
        System.out.println(i * 3);
        System.out.println(l / 2);
        
        Float f = 123.0F;
        System.out.println(f);
        
        Double d = 1234.5678;
        System.out.println(d);
        
        Boolean bo = Boolean.parseBoolean("true");
        System.out.println(bo);
        System.out.println(bo.toString().toUpperCase()); //transformando um boolean em string
        
        
        Character c = '#';
        System.out.println(c +"...");
        
        
    }

}
 ```

> Aula 32 e 33. Conversão de tipos primitivos.

Geralmente usa bastante int e double nos códigos

```java
package fundamentos;

public class ConversaoDeTiposPrimitivosNumericos {
    public static void main(String[] args) {
        double a = 1;
        System.out.println(a);
        /*
         o java não analisa valor e sim os tipos (int, double, float, byte ...)
         então tenho que tomar mt cuidado com a conversão 
         
         */
        
        //  float b = 1f; para acrescentar ponto e numeros logo após eu tenho que fazer o seguinte codigo
        float b = (float) 1.1232; // ele tem um limite após o ponto
        System.out.println(b);
        
        //formula para transformar int em byte, lembrando que há um limite
        
        
        int c = 4;
        byte d = (byte) c;
        System.out.println(d);
    }

}
```

>Aula 34. Conversão de números em String.

```java
package fundamentos;

public class ConversaoNumeroEmString {
    public static void main(String[] args) {
        Integer num1 = 10000;
        System.out.println(num1.toString().length());
        //da para converter int em stgring desde que eu chame o Integer
        
        int num2 = 10000;
        System.out.println(Integer.toString(num2));
        
        System.out.println((""+ num1).length());
    }

}
```

>Aula 35. Conversão de String em Números.

```java
package fundamentos;

import javax.swing.JOptionPane;

public class ConversaoDeStringParaNumeros {
    public static void main(String[] args) {
        String valor1 = JOptionPane.showInputDialog("Digite o primeiro numero ");
        String valor2 = JOptionPane.showInputDialog("Digite o segundo numero ");
        System.out.println(valor1);
        System.out.println(valor2);
        
        double numero1 = Double.parseDouble(valor1);
        double numero2 = Double.parseDouble(valor2);
        
        double soma = numero1 + numero2;
         System.out.println("Soma é " + soma);
         System.out.println("Dividido " +soma / 2);

    }

}
```

>Aula 36/37. Desafio Conversão.

Fazer um scanner com String que apareça 3 salarios, some eles e dividam por 3, tem que usar replace para substituir ponto por virgula.

```java
package fundamentos;

import java.util.Scanner;

public class DesafioConversao {
    public static void main(String[] args) {
        
        Scanner entrada = new Scanner(System.in);
        System.out.print("salario 1: ");
        String valor1 = entrada.next().replace(",", ".");

        System.out.print("salario 2: ");
        String valor2 = entrada.next().replace(",", ".");
        
        System.out.print("salario 3: ");
        String valor3 = entrada.next().replace(",", ".");
        
        double salario1 = Double.parseDouble(valor1);
        double salario2 = Double.parseDouble(valor2);
        double salario3 = Double.parseDouble(valor3);
        
        double media = (salario1 + salario2  + salario3) /3;
        
        System.out.println("A media dos salarios é " + media);
                
        entrada.close();    
    }
}
```

>Aula 42. Operadores Aritméticos.

````java
package fundamentos;

public class OperadoresAritmeticos {
    public static void main(String[] args) {
        System.out.println(2 + 3);
        
        var x = 23.32;
        double y = 2.2;
        System.out.println(x + y);
        System.out.println(x - y);
        System.out.println(x * y);
        System.out.println(x / y);
        
        System.out.println("------");
        
        int a = 8;
        int b = 7;
        System.out.println(a + b);
        System.out.println(a - b);
        System.out.println(a * b);
        System.out.println(a / b);
        System.out.println(a /  (double) b); // podemos usar o cast para converter em um double
        
    }

}
````

>Aula 45/46. Operadores Lógicos

````java
package fundamentos.operadores;

public class OperadoresLogicos {

    public static void main(String[] args) {
        boolean condicao1 = true;
        boolean condicao2 = 3 > 7;
        
        System.out.println(!condicao1);
        System.out.println(!condicao2);
        System.out.println(condicao1 && condicao2);
        System.out.println(condicao1 || condicao2);
        System.out.println(condicao1 ^ condicao2);
        
        System.out.println("---------------");
        //Tabela verdade E (AND)
        System.out.println(true && true); // true
        System.out.println(true && false); // false
        System.out.println(false && true); // falso e qualquer coisa é falso
        
        System.out.println("---------------");
        //Tabela verdade OU (OR)
        
        System.out.println(true || true); // true
        System.out.println(true || false); // true
        System.out.println(false || true); // true
        System.out.println(false || false); //apenas é falso quando as duas forem falsas 
        
        System.out.println("---------------");
        //Tabela verdade Ou exclusivo (XOR)
        
        System.out.println(true ^ true); // false
        System.out.println(true ^ false); // true
        System.out.println(false ^ true); // true
        System.out.println(false ^ false); //false, todas iguais são falsas 
        
    }
} 
````

>Aula 47. Desafio Operadores Lógicos.

````java

package fundamentos.operadores;

public class DesafioLogicos {
    public static void main(String[] args) {
        //Trabalho na Terça (V ou F)
        //Trabalho na Quarta (V ou F)
        
        boolean trabalho1 = true;
        boolean trabalho2 = false;
        
        boolean comprarTvde50 = trabalho1 && trabalho2;
        boolean comprarTvde32 = trabalho1 || trabalho2;
        boolean comprarSorvete = trabalho1 ^ trabalho2;
        
        
        System.out.println("Vamos comprar a tv de 50? "+ comprarTvde50); //false
        System.out.println("Vamos comprar a tv de 32? "+ comprarTvde32); //true
        System.out.println("Vamos comprar sorvete? "+ comprarSorvete); //true
        
        System.out.println("Sorvete é mais saúdavel? "+ !comprarSorvete);
        
    }

}
````

>Aula 49. Operadores Relacionais.

````java
package fundamentos.operadores;

public class Relacionais {
    public static void main(String[] args) {
        
        int a = 97;
        int b = 'a';
        System.out.println(a == b);
        
        System.out.println(3 > 4);
        System.out.println(3 >= 4);
        System.out.println(3 < 7);
        System.out.println(30 <= 7);
        System.out.println(30 != 7); //!= diferente
        
        System.out.println("----------------------");
        
        double nota = 7.4;
        boolean bomComportamento = true;
        boolean passouPorMedia = nota >= 7;
        
        boolean desconto = bomComportamento && passouPorMedia;
        
        System.out.println("Tem desconto? "  + desconto);
        
        
    }

}
````

>Aula 50. Operadores Atribuição.

````java
    package fundamentos.operadores;
        
    public class Atribuicao {
        public static void main(String[] args) {
            int a = 3;
            int b  = a;
            int c = a + b;
            
            c += b;
            c -= b;
            c *= b;
            c /= b;
            c %= 2; //para saber se é par ou impar vai dar 0 ou 1 
            
        }
    }

````

> Aula 51. Operadores Unários.

````java
package fundamentos.operadores;

public class Unarios {
    public static void main(String[] args) {
        int a = 1;
        int b = 2;
        
        a++; //acrescenta +1
        a--; //diminui -1
        
        ++b;
        --b;
        
        System.out.println(a);
        System.out.println(b);
        
        System.out.println(++a == b--);
        System.out.println(a == b);
        System.out.println(a);
        System.out.println(b);
    }
}
````

> Aula 52. Operador Ternário.

````java
package fundamentos.operadores;

public class Ternario {
    public static void main(String[] args) {
        
        double media = 7.6;
        
    String resultadorParcial = media >= 5.0 ? "recuperação" : "Reprovado";  
    String resultadoFinal = media >= 7.0 ? "Aprovado" : resultadorParcial;
        
    System.out.println(resultadoFinal);
        
        
    double nota = 7.4;
    boolean bomComportamento = true;
    boolean passouPorMedia = nota >= 7;
        
    boolean TemDesconto = bomComportamento && passouPorMedia;
        
    String resultado = TemDesconto ? "sim" :  "não";
    System.out.println("Tem desconto? "  + resultado);
    }
}

 ````

 >Aula 57. Desafio, calculadora

````java package Fundamentos;

import java.util.Scanner;

public class calculadora {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        
        System.out.println("Informe o numero: ");
        double num1 = entrada.nextDouble();
        
        System.out.println("Informe a operação: ");
        String op = entrada.next();
        
        System.out.println("Informe o numero: ");
        double num2 = entrada.nextDouble();
        
        
        double resultado = "+".equals(op) ? num1 + num2 : 0;
        resultado = "-".equals(op) ? num1 - num2 : resultado;
        resultado = "*".equals(op) ? num1 * num2 : resultado;
        resultado = "/".equals(op) ? num1 / num2 : resultado;
        resultado = "%".equals(op) ? num1 % num2 : resultado;
        
        System.out.printf("%.2f %s %.2f = %.2f", num1, op, num2, resultado);
        entrada.close();
        
        
    }
}
````

## Estruturas de controles

>Aula 62. IF

````java
package controle;

import java.util.Scanner;

public class If {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        
        System.out.print("Informe a média: ");
        double media = entrada.nextDouble();
        
        //boolean aprovacao = media <= 10 && media >= 7.0;
        if(media <= 10 && media >= 7.0) {
        System.out.println("Aprovado!");
        System.out.println("Parabéns!");
        }
        
        if(media <= 7 && media > 4.5) {
            System.out.println("Recuperação!");}
        
        
        if(media < 4.5 && media >= 0) {
                System.out.println("Reprovado!");
                
        }
        
        if(media >= 11) {
            System.out.println("Ta porra o mlk é um gênio!");
        }
        
        entrada.close();
        
    }
}
````

> Aula 63 Desafio IF/Resposta

````java package controle;

public class DesafioIf {
    public static void main(String[] args) {
        double nota = 1.3;

        //if (nota >= 9.0); tinha um ponto e virgula
        if (nota >= 9.0) {

            System.out.println("Quadro de honra!");
            System.out.println("Você é fera!");
        }

    }
}
````

>Aula 65. IF/ELSE

 If = Se, else =Senao, então o else if é "senao se " ou seja se a condicao anterior não for verdadeira verifique uma nova condicao, "senao se" condicao, já o else é apenas para quando nenhuma das condicoes anteriores foi verdadeira ai ele executa o else sem verificacao de condicao.

 A condicional if é uma estrutura condicional que executa a afirmação, dentro do bloco, se determinada condição for verdadeira. Se for falsa, executa as afirmações dentro de else.

````java package controle;

import javax.swing.JOptionPane;

public class IfElse {
    public static void main(String[] args) {
        String valor = JOptionPane.showInputDialog("Informe o número");
        int numero = Integer.parseInt(valor);
        
        if (numero % 2 == 0) 
            System.out.println("numero par");
        else {
            System.out.println("numero ímpar");
            
        }
            
    }
}
````

>Aula 66. IF/ELSE IF.

Junção dos dois.

````java
package controle;

import java.util.Scanner;

public class IfElseIf {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        System.out.print("Digite sua nota: ");

        double nota = entrada.nextDouble();
        if (nota > 10 || nota < 0) {
            System.out.println("Nota invalida!");
        } else if (nota >= 8) {
            System.out.println("Você tirou um A!");
        } else if (nota >= 6) {
            System.out.println("Você tirou um B!");
        } else if (nota >= 4) {
            System.out.println("Você tirou um C!");
        } else if (nota >= 2) {
            System.out.println("Você tirou um F!");
        }

    }
}

````

>Aula 67/68. Desafio Dia da Semana.

````java
package controle;

import java.util.Scanner;

public class DesafioDiaDaSemana {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        System.out.print("Digite o dia: ");

        String dia = entrada.next();
        if ("Domingo".equalsIgnoreCase(dia)) {
            System.out.println(1);
        } else if ("segunda".equalsIgnoreCase(dia)) {
            System.out.println(2);
        } else if ("terça".equalsIgnoreCase(dia)) {
            System.out.println(3);
        } else if ("quarta".equalsIgnoreCase(dia)) {
            System.out.println(4);
        } else if ("quinta".equalsIgnoreCase(dia)) {
            System.out.println(5);
        } else if ("sexta".equalsIgnoreCase(dia)) {
            System.out.println(6);
        } else if ("sabado".equalsIgnoreCase(dia)) {
            System.out.println(7);
        }else {
            System.out.println("dia invalido");
        }

        entrada.close();

    }
}

````

>Aula 69. WHILE #01.

````java
package controle;

public class WhileDeterminado {
    public static void main(String[] args) {
        
        int contador = 1;
        
        while(contador <= 10) {
        System.out.println("bom dia!");
        contador++;
        }
    }
}
````

>Aula 70. FOR #01.

````java
package controle;

public class For1 {
    public static void main(String[] args) {
        for(int contador = 0;contador <= 20;contador +=2) {
            System.out.printf("i = %d\n", contador);
            
        }
        
    }
}
`````

>Aula 71. WHILE #02.

````java
package controle;

import java.util.Scanner;

public class WhileIndeterminado {
    public static void main(String[] args) {
        Scanner entrada =  new Scanner(System.in);
        String valor = "";
        
        while(!valor.equalsIgnoreCase("Sair")) { //quando n tiver a palavra "sair" ele n para
            System.out.println("Você diz: ");
            valor = entrada.nextLine();
        }
        
        entrada.close();
    }
}
````

>Aula 72. DO/WHILE.

````java
package controle;

import java.util.Scanner;

public class DoWhile {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        String texto = "";
        
        do {
            System.out.println("Você precisa falar "
                    + "as palavras magicas");
            System.out.print("Quer sair?");
            texto = entrada.nextLine();
        }while(!texto.equalsIgnoreCase("por favor"));
        
        System.out.println("Obrigado!");
        entrada.close();
    }
}
````

>Aula  73. Desafio WHILE.

````java
package controle;

import java.util.Scanner;

public class DesafioWhile {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        int quantidadeDeNotas = 0;
        double nota = 0;
        double total = 0;

        while (nota != -1) {
            System.out.print("Informe a nota (ou -1 p/ sair): ");
            nota = entrada.nextDouble();

            if (nota <= 10 && nota >= 0) {
                total += nota;
                quantidadeDeNotas++;
            } else if (nota != -1) {
                System.out.println("Nota inválida!!!! ;D");
            }
        }

        // Calcular a média
        double media = total / quantidadeDeNotas;
        System.out.println("Média = " + media);

        entrada.close();
    }
}

````

>Aula 76. FOR #02.

````java
package controle;

public class For2 {
    public static void main(String[] args) {
        
        for(int contador = 10; contador >= 0; contador -=2) {
        
        System.out.printf("Contador = %d\n", contador);
        }
    }
}
````

>Aula 76. FOR #03.

````java
package controle;

public class For3 {
    public static void main(String[] args) {
        for (int i = 0; i <10; i++) {
            for(int j = 0; j <10; j++)
        System.out.printf("[%d %d]", i, j);
        }
    }
}
````

>Aula 78/77. Desafio FOR + resposta.

````java
package controle;

public class DesafioFor {
    public static void main(String[] args) {
        String  valor = "#";
        
        for(int i = 1; i <=5; i++) {
            System.out.println(valor);
            valor += '#';
        }
            //resposta do desafio
            
            for(String v = "#"; !v.equals("######"); v += "#") {
        System.out.println(v);
            
            }
    }
}
````

>Aula 79. SWITCH #01.

````java
package controle;

public class Switch01 {
    public static void main(String[] args) {
//       if(boolean) ...
//       while(boolean) ...
//       for(;boolean;) ...

        String faixa = "PRETA";
        
        switch (faixa.toLowerCase()) {
        case "preta":
            System.out.println("Sei o Nassai-Dai");
            
        case "marrom":
            System.out.println("Sei o Tekki Shodan ");
            
        case "roxa":
            System.out.println("Sei o Heian Godan");
            
        case "verde":
            System.out.println("Sei o Heian Yodan");
            
        case "laranja":
            System.out.println("Sei o Heian Sandan");
            
        case "vermelha":
            System.out.println("Sei o Heian Niidan");
            
        case "amarela":
            System.out.println("Sei o Heian Shodan");
            break;
            
        default:
            System.out.println("Não sei nada");
        }
        System.out.println("Fim!");
        
        int idade = 3;
        switch (idade) {
        case 3:
            System.out.println("Sabe falar");
        case 2:
            System.out.println("Sabe andar");
        case 1:
            System.out.println("Sabe rirar");
        }
    }
}

````

>Aula 80. SWITCH #02 dedededededededdededed
