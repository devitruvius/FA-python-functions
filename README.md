# Estruturas de Funções em Python

Neste repositório há uma variedade de exemplos de código em Python que ilustram a aplicação das estruturas de funções. Esses códigos foram desenvolvidos como parte das atividades da disciplina de Fundamentos de Algoritmos do curso de Análise e Desenvolvimento de Sistemas (ADS) pela Universidade Federal do Cariri (UFCA). O objetivo principal dessas atividades é oferecer uma prática sólida e consolidar os conceitos essenciais relacionados às estruturas de funções em Python, promovendo uma compreensão aprofundada e aprimorando as habilidades de programação.

## Estrutura do Repositório

A estrutura do repositório foi organizada para proporcionar uma experiência de navegação eficiente e facilitar a revisão dos códigos. Cada bloco de atividade está representada por um tópico, dentro do qual você encontrará os códigos referentes às atividades desenvolvidas.

## Atividades

1. **Escreva uma função para verificar se um número é par. Um número é par quando o resto da divisão dele por 2 é 0.**

   ```python
    # Verificador de Paridade
    # Declaração de Variáveis
    
    def verificar_par(numero):
        if numero % 2 == 0:
            return True
        else:
            return False
    
    # Teste
    num = int(input("Digite um número: "))
    if verificar_par(num):
        print(f"O número {num} é par.")
    else:
        print(f"O número {num} é ímpar.")
   ```
<br>

2. **Modifique a função acima para verificar e retornar se o número é par ou ímpar.**
 
   ```python
    # Verificador de Paridade 2.0
    # Declaração de Variáveis
    
    def verificar_par_ou_impar(numero):
        if numero % 2 == 0:
            return "par"
        else:
            return "ímpar"
    
    # Teste
    num = int(input("Digite um número: "))
    resultado = verificar_par_ou_impar(num)
    print(f"O número {num} é {resultado}.")
   ```
<br> 

3. **Escreva uma função que retorne o maior de dois números.**

   ```python
    # Verificador de Maior Número
    # Declaração de Variáveis
    
    def maior_numero(num1, num2):
        if num1 > num2:
            return num1
        else:
            return num2
    
    # Teste
    num1 = int(input("Digite o primeiro número: "))
    num2 = int(input("Digite o segundo número: "))
    maior = maior_numero(num1, num2)
    print(f"O maior número é: {maior}")
   ```
<br>
 
4. **Escreva uma função que recebe dois números e retorna True se o primeiro for múltiplo do segundo.**

   ```python
    # Verificador de Múltiplos
    # Declaração de Variáveis
    
    def verificar_multiplo(num1, num2):
        if num1 % num2 == 0:
            return True
        else:
            return False
    
    # Teste
    num1 = int(input("Digite o primeiro número: "))
    num2 = int(input("Digite o segundo número: "))
    if verificar_multiplo(num1, num2):
        print(f"{num1} é múltiplo de {num2}.")
    else:
        print(f"{num1} não é múltiplo de {num2}.")
   ```
<br>

5. **Escreva uma função que recebe o lado de um quadrado e retorna sua área.**

   ```python
    # Calculadora de Área do Quadrado
    # Declaração de Variáveis
    
    def calcular_area_quadrado(lado):
        area = lado * lado
        return area
    
    # Teste
    lado = float(input("Digite o lado do quadrado: "))
    area = calcular_area_quadrado(lado)
    print(f"A área de um quadrado com lado {lado} é {area}.")
   ```
<br>

6. **Escreva uma função que recebe a base e altura de um triângulo e retorna sua área.**

   ```python
    # Calculadora de Área do Triângulo
    # Declaração de Variáveis
    
    def calcular_area_triangulo(base, altura):
        area = (base * altura) / 2
        return area
    
    # Teste
    base = float(input("Digite a base do triângulo: "))
    altura = float(input("Digite a altura do triângulo: "))
    area = calcular_area_triangulo(base, altura)
    print(f"A área do triângulo com base {base} e altura {altura} é {area}.")
   ```
<br>

7. **Defina uma função recursiva que calcule o maior divisor comum (M.D.C.) entre dois números a e b.**

   ```python
    # Calculadora de MDC
    # Declaração de Variáveis
    
    def mdc(a, b):
        if b == 0:
            return a
        else:
            return mdc(b, a % b)
    
    # Teste
    a = int(input("Digite o primeiro número (a): "))
    b = int(input("Digite o segundo número (b): "))
    
    if a > b:
        resultado_mdc = mdc(a, b)
        print(f"O MDC entre {a} e {b} é {resultado_mdc}.")
    else:
        print("Por favor, garanta que a > b para calcular o MDC.")
   ```
<br>

8. **Usando a função mdc definida no exercício anterior, defina uma função para calcular o menor múltiplo comum (M.M.C.) entre dois números.**
    
   ```python
    # Calculadora de MMC
    # Declaração de Variáveis
    
    def mdc(a, b):
        if b == 0:
            return a
        else:
            return mdc(b, a % b)
    
    def mmc(a, b):
        return abs(a * b) // mdc(a, b)
    
    # Teste
    a = int(input("Digite o valor de a: "))
    b = int(input("Digite o valor de b: "))
    
    resultado = mmc(a, b)
    print(f"O M.M.C. de {a} e {b} é {resultado}.")
   ```
<br>

9. **Defina uma função recursiva para calcular a sequência Fibonacci. A sequência em questão começa com dois números 0 e 1. Os números seguintes são a soma dos dois anteriores. A sequência ficaria assim: 0, 1, 1, 2, 3, 5, 8, 13, 21, ...**

   ```python
    # Calculadora de Sequência Fibonacci
    # Declaração de Variáveis
    
    def fibonacci(n):
        if n <= 1:
            return n
        else:
            return fibonacci(n - 1) + fibonacci(n - 2)
    
    # Teste
    termo = int(input("Digite o termo da sequência Fibonacci que deseja calcular: "))
    
    if termo <= 0:
        print("Por favor, insira um número inteiro positivo.")
    else:
        print(f"O {termo}º termo da sequência Fibonacci é: {fibonacci(termo)}")
   ```
<br>

10. **Escreva uma função recursiva para calcular a função de Ackerman para dois inteiros positivos m e n.**

    ```python
     # Calculadora da Função de Ackermann
     # Declaração de Variáveis
    
     def ackermann(m, n):
         if m == 0:
             return n + 1
         elif n == 0:
             return ackermann(m - 1, 1)
         else:
             return ackermann(m - 1, ackermann(m, n - 1))
    
     # Teste
     m = int(input("Digite o valor de m (m >= 0): "))
     n = int(input("Digite o valor de n (n >= 0): "))
    
     resultado = ackermann(m, n)
     print(f"A função de Ackermann para m={m} e n={n} é {resultado}.")
    ```
