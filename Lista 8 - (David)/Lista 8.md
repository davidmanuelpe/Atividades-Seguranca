# Lista 8

## 1. Quais são os principais elementos de um criptossistema de chave pública?

  R: 
   Os principais elementos de um criptossistema de chave pública incluem:

  - Chave Pública e Chave Privada: 
  
  No RSA, cada entidade possui um par de chaves: uma chave pública e uma chave privada. A chave pública é usada para criptografar mensagens e a chave privada é usada para descriptografá-las. A chave pública é compartilhada com todos, enquanto a chave privada deve ser mantida em segredo.

  - Algoritmo de Geração de Chaves: 
  
  Um algoritmo é usado para gerar o par de chaves (pública e privada). No caso do RSA, o processo envolve a escolha de dois números primos grandes, a computação do produto desses primos para obter um número chamado módulo, e a seleção de um expoente de criptografia e um expoente de descriptografia adequados.
 
  - Algoritmo de Criptografia: 
  
  O algoritmo de criptografia é utilizado para transformar uma mensagem original em um texto cifrado, utilizando a chave pública. No caso do RSA, isso envolve a elevação da mensagem a uma potência (expoente de criptografia) e a redução do resultado pelo módulo.
 
  - Algoritmo de Descriptografia: 
  
  O algoritmo de descriptografia é usado para reverter o processo de criptografia e obter a mensagem original a partir do texto cifrado, utilizando a chave privada. No RSA, isso é feito elevando o texto cifrado à potência do expoente de descriptografia e novamente reduzindo pelo módulo.
 
  - Módulo: 
  
  O módulo é um número grande e público que é parte essencial do processo de criptografia e descriptografia. Ele é gerado durante a geração das chaves e é usado tanto para a criptografia quanto para a descriptografia.
 
  - Expoentes de Criptografia e Descriptografia: 
  
  No RSA, os expoentes de criptografia e descriptografia são números escolhidos durante a geração das chaves. O expoente de criptografia é usado para cifrar mensagens, enquanto o expoente de descriptografia é usado para decifrar mensagens.
 
  - Segurança dos Números Primos: 
  
  A segurança do sistema depende em grande parte da dificuldade de fatorar o módulo em seus dois primos componentes. Quanto maiores forem os primos escolhidos, mais difícil será quebrar a criptografia.
   

## 2. Quais são os papéis da chave pública e da privada?

  R:
   
  - Chave Pública: Usada para criptografar mensagens e verificar assinaturas digitais. É compartilhada amplamente.

  - Chave Privada: Usada para descriptografar mensagens e criar assinaturas digitais. Deve ser mantida em segredo absoluto pelo proprietário.
   

## 3. Que requisitos os criptossistemas de chave pública precisam cumprir para serem um algoritmo seguro?


  R:

  - Confidencialidade: O algoritmo deve ser capaz de proteger a confidencialidade das informações transmitidas. Isso significa que, mesmo que um adversário intercepte os dados cifrados e conheça a chave pública, não deve ser possível determinar a mensagem original sem a chave privada correspondente.

  - Integridade: O algoritmo deve garantir a integridade dos dados, de modo que qualquer modificação não autorizada nos dados cifrados seja detectável. Isso é especialmente importante em sistemas que utilizam assinaturas digitais para autenticação.
 
  - Autenticidade: Um criptossistema seguro deve permitir a autenticação das partes envolvidas na comunicação. Isso pode ser alcançado através do uso de assinaturas digitais, onde a chave privada é usada para assinar mensagens, garantindo que apenas a parte com a chave privada correspondente possa assinar.
 
  - Não Repúdio: O algoritmo deve prevenir a negação posterior das ações realizadas. Isso é obtido através do uso de assinaturas digitais, onde uma assinatura autêntica pode ser usada como prova de que a mensagem foi de fato enviada pela parte que possui a chave privada correspondente.
 
  - Resistência a Ataques: O criptossistema deve ser resistente a diversos tipos de ataques, incluindo ataques de força bruta (tentativas repetidas de adivinhar a chave) e ataques de análise criptográfica (tentativas de explorar fraquezas matemáticas no algoritmo).
 
  - Dificuldade em Deduzir Chaves: Mesmo que um atacante tenha acesso às chaves públicas e cifrados, não deve ser possível deduzir a chave privada a partir dessas informações. Isso é conhecido como "problema de inversão", e sua resolução é um dos princípios fundamentais dos criptossistemas seguros.
 
  - Dificuldade em Fatorar Números: Muitos criptossistemas de chave pública, como o RSA, são baseados na dificuldade de fatorar grandes números compostos em seus fatores primos. Portanto, a segurança do sistema depende da impossibilidade prática de fatorar números grandes em tempo razoável.
 
  - Aleatoriedade: A geração de chaves e números aleatórios é essencial para a segurança dos criptossistemas. Sequências previsíveis ou padrões podem ser explorados por atacantes.
 
  - Eficiência: Embora a segurança seja fundamental, os criptossistemas também precisam ser eficientes em termos de desempenho para tornar a criptografia e a descriptografia viáveis em aplicações do mundo real.
 
  - Análise Pública: Os algoritmos de chave pública devem ser publicamente conhecidos e passíveis de análise por especialistas em segurança. Isso permite que a comunidade avalie sua robustez e identifique possíveis vulnerabilidades.
  

## 4. Descreva, em termos gerais, um procedimento eficiente para se escolher um número primo

  R:
   
   - Intervalo de Seleção: Determine um intervalo adequado para buscar números primos. Quanto maior o intervalo, maior a probabilidade de encontrar um número primo, mas também mais intensivo em termos de recursos computacionais.

   - Geração Aleatória: Selecione um número aleatório dentro do intervalo determinado. Isso pode ser feito utilizando um gerador de números aleatórios confiável.
 
   - Verificação da Primalidade: Aplique um teste de primalidade para verificar se o número escolhido é primo. Existem vários testes de primalidade disponíveis, como o Teste de Miller-Rabin, que é amplamente usado na prática. Esse teste verifica se o número passado é composto ou provavelmente primo.
 
   - Repetição ou Refinamento: Dependendo da qualidade do teste de primalidade utilizado, pode ser necessário repetir o processo algumas vezes até encontrar um número que passe no teste. Quanto mais vezes o teste for executado, maior a probabilidade de o número ser realmente primo.
 
   - Verificação Adicional (Opcional): Em alguns casos, pode ser útil aplicar um teste de primalidade mais rigoroso, como o Teste de Primalidade de Agrawal-Kayal-Saxena (AKS), para garantir uma maior certeza da primalidade.
 
   - Validação e Uso: Após encontrar um número que passe nos testes de primalidade, verifique sua adequação para sua aplicação específica e seu tamanho em relação à segurança desejada. Em sistemas criptográficos, números primos maiores são geralmente preferidos.


## 5.  Antes da descoberta de quaisquer esquemas de chave pública especificas, como RSA, uma prova de existência foi desenvolvida, cuja finalidade era demonstrar que a encriptação de chave pública é possível em teoria. 

Considere as funções f1(x1) = z1; f2(x2, y2) = z2; f3(x3, y3) = z3, onde todos os valores são inteiros com 1 ≤ xi, yi, zi ≤ N. A função f1, pode ser representada por um vetor M1 de tamanho N, em que a k-ésima entrada é o valor de f1(k). De modo semelhante, f2 e f3 podem ser representados pelas matrizes M2 e M3 de tamanho N × N.

A intenção é indicar o processo de encriptação/decriptação por pesquisas de tabela para aquelas com valores muito grandes de N. 
Essas tabelas seriam impraticavelmente grandes, mas, a princípio, poderiam
ser construídas. 

O esquema funciona da seguinte forma: construa M1 com uma permutação
aleatória de todos os inteiros entre 1 e N; ou seja, cada inteiro aparece exatamente uma vez em M1. Construa M2, de modo que cada linha contenha uma permutação aleatória dos primeiros
N inteiros. Finalmente, preencha M3 para satisfazer a seguinte condição:
f3(f2(f1(k), p), k) = p para todo k, p com 1 ≤ k, p ≤ N 

Resumindo,

1. M1 toma uma entrada k e produz uma saída x.

2. M2 toma as entradas x e p, dando a saída z.

3. M3 toma as entradas z e k e produz p.

As três tabelas, uma vez construídas, se tornam públicas.

a) Deverá ficar claro que é possível construir M3 para satisfazer a condição anterior. Como um
exemplo, preencha M3 para o caso simples a seguir:

M1 = [[5],[4],[3],[2],[1]]

M2 = [[5,2,3,4,1], [4,2,5,1,3], [1,3,2,4,5], [3,1,4,2,5], [2,5,3,4,1]]

M3 = [[a1,a2,a3,a4,a5], [b1,b2,b3,b4,b5], [c1,c2,c3,c4,c5], [d1,d2,d3,d4,d5], [e1,e2,e3,e4,e5]]

Convenção: o i-ésimo elemento de M1 corresponde a k = i. A i-ésima linha de M2 diz respeito ax = i; a j-ésima coluna de M2 equivale a p = j. A i-ésima linha de M3 indica z = i; a j-ésima coluna de MB relaciona-se a k = j.

(a) Descreva o uso desse conjunto de tabelas para realizar a encriptação e decriptação entre
dois usuários.

(b) Demonstre que esse é um esquema seguro

  R: 

## 6. Realize a encriptação e decriptação usando o algoritmo RSA, como na Figura 9.5, para o seguinte:

(a) p = 3; q = 11, e = 7; M = 5;

  1.

    n = p*q = 3*11 = 33;

    φ(n) = (p-1) * (q-1) = 2*10 = 20;

  2.

    d = e^-1 % φ(n)
    
    7*3 % 20 ≡ 1 % 20

    d = 3

  encriptação:

    C = M^e % n = 5^7 % 33 = 14

  decriptação:

    M = C^d % n = 14^3 % 33 = 5

(b) p = 5; q = 11, e = 3; M = 9;

  n = 5*11 = 55;

  φ(n) = 4*10 = 40;

  d = e^-1 % φ(n)
    
  3*13 % 40 ≡ 1 % 40

  d = 13

  encriptação:

    C = 9^3 % 55 = 14

  decriptação:

    M = 14^13 % 55 = 9

(c) p = 7; q = 11, e = 17; M = 8;

  n = 7*11 = 77;

  φ(n) = 6*10 = 60;

  d = e^-1 % φ(n)
    
  17*53 % 60 ≡ 1 % 60

  d = 53

  encriptação:

    C = 8^17 % 77 = 57

  decriptação:

    M = 50^53 % 77 = 8

(d) p = 11; q = 13, e = 11; M = 7;

  n = 11*13 = 143;

  φ(n) = 10*12 = 120;

  d = e^-1 % φ(n)
    
  11*11 % 120 ≡ 1 % 120

  d = 11

  encriptação:

    C = 7^11 % 143 = 106

  decriptação:

    M = 106^11 % 143 = 7

(e) p = 17; q = 31, e = 7; M = 2.

  n = 17*31 = 527;

  φ(n) = 16*30 = 480;

  d = e^-1 % φ(n)
    
  7*137 % 480 ≡ 1 % 480

  d = 137

  encriptação:

    C = 2^7 % 527 = 128

  decriptação:

    M = 128^137 % 527 = 2

Dica: a decriptação não é tão difícil quanto você pensa; use alguma sutileza.


  R:  


## 7. Em um sistema de chave pública usando RSA, você intercepta o texto cifrado C = 10 enviado a um usuário cuja chave pública é e = 5, n = 35. Qual é o texto claro M?

  R:

   Geralmente não seria possível alcançar essa chave mas devido à uma má escolha dos números primos e dos pequenos valores nesse caso é possível, temos que encontrar dois primos distintos p e q, tais que, p*q = 35 e (p-1) * (q-1) = 24 já que φ(35) = 24, vamos primeiro fatorar o 35 em números primos obtendo 5*7, vamos assumir p = 5 e q = 7, agora vamos tentar chegar no resultado do φ(35):
 
   4*6 = 24
 
   agora calculamos o d
 
   d = e^-1 % φ(n)
 
   5*d ≡ 1 % 24
 
   5*5 ≡ 1 % 24
 
   d = 5
 
   agora temos a Chave Privada {5,35}
 
   por fim,
 
   M = 10^5 % 35 = 5
