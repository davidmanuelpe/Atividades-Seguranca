# Lista 7

## 1. Por que mdc(n, n + 1) = 1 é para dois inteiros consecutivos n e n + 1?

  R: 
    
   Isso ocorre porque dois inteiros consecutivos, como n e n + 1, não têm fatores primos em comum, exceto o número 1. Um fator primo é um número primo que divide outro número sem deixar um resto. Como n + 1 é o próximo número após n, ele não pode ser divisível por nenhum dos fatores primos de n (caso contrário, eles não seriam consecutivos).

## 2. Usando o teorema de Fermat, encontre 3^201 mod 11.

  R:

   N ≡ 3^201 mod 11
   
   N ≡ (:red_circle:3^10)^20+1 mod 11
   
   N ≡ (:red_circle:3^10)^20 * 3^1 mod 11

   como o teorema de fermat nos diz que a^p-1 ≡ 1 mod p, então vamos fazer a substituição do nosso :red_circle:a^p-1 na conta.

   N ≡ 1^20 * 3^1 mod 11
   
   N ≡ 1 * 3^1 mod 11
   
   N ≡ 3 mod 11

## 3. Use o teorema de Fermat para encontrar um número a entre O e 72, com a congruente a 9794 módulo 73.

  R:

  

## 4. Use o teorema de Euler para encontrar um número a entre 0 e 9, tal que a seja congruente a 7^1000 módulo 10. (Observe que isso é o mesmo que o último dígito da expansão decimal de 7^1000.)

  R:

  O teorema de Euler diz que para quaisquer 'a' e 'n' tal qual, 'a' e 'n' sejam coprimos, então, a^ϕ(n) ≡ 1(mod n)

  primeiro vou calcular o ϕ(n) da nossa conta, ϕ(10) = 4, nesse caso, (1,3,7,9) então temos que quaisquer um desses 4 números são possíveis candidatos para o nosso a, vamos pegar estratégicamente o número 7 pois é o número usado na nossa equivalência.

  7^4 ≡ 1 mod 10

  e

  7^1000 mod 10

  também pode ser escrito como (:red_circle:7^4)^250 mod 10

  substituindo nosso :red_circle:a^ϕ(n):
  
  temos,  
  
  1^250 mod 10

  = 1 mod 10

  então temos que 7 é um valor válido para a.
    

## 5. Use o teorema de Euler para encontrar um número x entre 0 e 28, com x^85 congruente a 6 módulo 35(29?) (Você não precisará usar qualquer pesquisa por força bruta).

  R:  

  x^85 = (x^28)^3+1 ≡ 6 mod 29

  = 1^3 * x^1 ≡ 6 mod 29

  = x ≡ 6 mod 29

  x = 6

## 6. Observe, na Tabela 8.2, que ϕ(n) é par para n > 2. Isso é verdadeiro para todo n > 2. Dê um argumento conciso para explicar por que isso acontece.

  R:  

  podemos dizer que o resultado de ϕ(n) é a quantidade de numeros x, tal que, 1≤x≤n e mdc(n,x) = 1.

  também é fácil de visualizar que visualizar que se mdc(n,x) = 1 então, o mdc(x,n-x) = 1 já que se mdc(x,n-x) != 1 então n seria múltiplo no próprio x, então podemos dizer que x e n-x formam pares de números coprimos de n, desde que x e n-x sejam números distintos, o caso onde isso é verdadeiro é quando n = 2 e x = 1, oque nunca acontece já que nossa regra base é que n > 2, então todos os números coprimos de n podem ser combinados em pares {x,n-x}. Logo ϕ(n) é par.

## 7. Se n é composto e passa no teste de Miller-Rabin para a base a, então n é chamado de pseudoprimo forte à base a. Mostre que 2047 é um pseudoprimo à base 2.

  R:  
  
  passo 1:
   
   n-1 = 2^k * m
   
   2046 = 2^1 * 1023
  
  passo 2:
    
   2046>a>1; a = 2 escolhido deliberadamente.
  
  passo 3:
    
   b0 = a^m mod n
   
   b0 = 2^1023 mod 2047
   
   b0 = (2^11)^93 mod 2047
   
   2^11 = 2048 ≡ 1 mod 2047
   
   b0 = 1^93 mod 2047 ≡ 1 mod 2047

   já que 2^m mod n = 1 então o teste de Miller-Rabin é inconclusivo para 2047 à base 2

## 8. O exemplo usado por Sun-Tsu para ilustrar o CRT foi x = 2 (mod 3); x = 3 (mod 5); x = 2 (mod 7) Solucione para x.

R:  
  
 x ≡ 2 mod 3

 x ≡ 3 mod 5

 x ≡ 2 mod 7

 chamaremos 2, 3 e 2 de n1, n2 e n3 respectivamente

 passo 1:
  
  N = 3 * 5 * 7 = 105

 passo 2:

  Nx = N/nx

  N1 = 105/3 = 35

  N2 = 105/5 = 21

  N3 = 105/7 = 15

 passo 3:

  calcular o inverso multiplicativo para cada Nx, ou seja um número k, tal que, k * Nx seja ≡ 1 mod nx

  k1 = 35^-1 (mod3) ≡ 2 (mod3)

  k2 = 21^-1 (mod5) ≡ 1 (mod5)

  k3 = 15^-1 (mod7) ≡ 1 (mod7)

 passo 4:

  calcular a soma ponderada dos resíduos originais 

  x ≡ (2 * 35 * 2)+(3 * 21 * 1)+(2 * 15 * 1)(mod 105)
  x ≡ 140 + 63 + 30 ≡ 233 (mod 105)

  que é o mesmo que x ≡ 23 (mod 105)

 para finalizar testamos se o 23 de fato resolve para as três congruências iniciais

  23 ≡ 2 mod 3

  3*7 = 21; r = 2, (verdadeiro)

  23 ≡ 3 mod 5

  5*4 = 20; r = 3, (verdadeiro) 

  23 ≡ 2 mod 7

  7*3 = 21; r = 2, (verdadeiro)