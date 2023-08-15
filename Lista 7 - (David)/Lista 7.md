# Lista 6

## 1. Por que mdc(n, n + 1) = 1 é para dois inteiros consecutivos n e n + 1?

  R: 
    quando consideramos dois inteiros consecutivos n e n + 1, nunca há fatores primos em comum entre eles, exceto o próprio 1. Portanto, o MDC entre eles é 1.

## 2. Usando o teorema de Fermat, encontre 3^201 mod 11.

  R:

   N ≡ 3^201 mod 11
   
   N ≡ (:exclamation:3^10)^20+1 mod 11
   
   N ≡ (:exclamation:3^10)^20 * 3^1 mod 11

   como o teorema de fermat nos diz que a^p-1 ≡ 1 mod p, então vamos fazer a substituição do nosso :exclamation:a^p-1 na conta.

   N ≡ 1^20 * 3^1 mod 11
   
   N ≡ 1 * 3^1 mod 11
   
   N ≡ 3 mod 11

## 3. Use o teorema de Fermat para encontrar um número a entre O e 72, com a congruente a 9794 módulo 73.

  R:
    
  Reutilizar uma chave de cifra de fluxo é altamente indesejável devido a várias razões de segurança. Por exemplo,

  - Previsibilidade e Vulnerabilidade:
        
    Quando uma chave de cifra de fluxo é reutilizada, a sequência de bits gerada será a mesma para as mensagens criptografadas com essa chave. Isso torna o fluxo de bits previsível, o que pode ser explorado por um atacante para decifrar ou manipular múltiplas mensagens criptografadas.

  - Ataques de Texto Cifrado Escolhido:

    Se um atacante tem a capacidade de escolher parte do texto cifrado para ser descriptografado, reutilizar uma chave de cifra de fluxo permite que o atacante observe a mesma sequência de bits sendo usada para diferentes partes do texto cifrado. Isso pode revelar informações sensíveis e enfraquecer a segurança do sistema.

  - Ataques de Conhecimento Nulo:
    
    A reutilização de uma chave de cifra de fluxo pode permitir a realização de ataques de conhecimento nulo, nos quais um atacante pode deduzir informações sobre o texto claro original sem realmente decifrar o texto cifrado.

  - Análise de Padrões:

    Ao reutilizar a mesma chave de cifra de fluxo, padrões podem surgir na sequência de bits gerada. Isso pode ser explorado por atacantes para inferir informações sobre os dados criptografados.

  - Ameaça à Confidencialidade:

    A confidencialidade dos dados criptografados é comprometida quando a mesma chave é usada repetidamente. Ataques que exploram a repetição de chaves podem ser devastadores para a segurança das informações.

  - Ataques de Repetição:

    Reutilizar a mesma chave de cifra de fluxo pode tornar o sistema vulnerável a ataques de repetição, nos quais um adversário captura e retransmite mensagens criptografadas para obter acesso não autorizado a sistemas ou informações.

## 4. Use o teorema de Euler para encontrar um número a entre 0 e 9, tal que a seja congruente a 7^1000 módulo 10. (Observe que isso é o mesmo que o último dígito da expansão decimal de 7^1000.)

  R:

   Swap (Troca);

   A operação de troca envolve a troca de dois elementos em uma matriz ou em um vetor. No contexto do RC4, essa operação é usada para permutar elementos do estado interno do algoritmo (S-box). Isso é feito para embaralhar os elementos e introduzir confusão no processo de geração da sequência de bytes pseudoaleatórios.

   XOR (OU Exclusivo);

   A operação XOR é fundamental no RC4 para combinar o estado interno (S-box) com os dados de entrada (chave e vetor de inicialização) a fim de produzir o fluxo de bits pseudoaleatório. A operação XOR é aplicada para misturar os bits dos elementos do S-box com os bits da chave e do vetor de inicialização, gerando a sequência de saída.

## 5. Use o teorema de Euler para encontrar um número x entre 0 e 28, com x^85 congruente a 6 módulo 35 (Você não precisará usar qualquer pesquisa por força bruta).

R:  
  A sequência terá uma quantidade de elementos limite igual ao tamanho do módulo que nesse caso é 16, e então teremos o período máximo da sequência entre 0 e 15.

## 6. Observe, na Tabela 8.2, que ϕ(n) é par para n > 2. Isso é verdadeiro para todo n > 2. Dê um argumento conciso para explicar por que isso acontece.

R:  
  A sequência terá uma quantidade de elementos limite igual ao tamanho do módulo que nesse caso é 16, e então teremos o período máximo da sequência entre 0 e 15.

## 7. Se n é composto e passa no teste de Miller-Rabin para a base a, então n é chamado de pseudoprimo forte à base a. Mostre que 2047 é um pseudoprimo à base 2.

R:  
  A chave que resultará em um estado interno inalterado durante a inicialização do RC4 é uma sequência de valores de 0 a 255 em ordem crescente.

## 8. O exemplo usado por Sun-Tsu para ilustrar o CRT foi x = 2 (mod 3); x = 3 (mod 5); x = 2 (mod 7) Solucione para x.

R:  
  A chave que resultará em um estado interno inalterado durante a inicialização do RC4 é uma sequência de valores de 0 a 255 em ordem crescente.