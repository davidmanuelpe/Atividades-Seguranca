# Lista 4

## 1. Qual foi o conjunto original de critérios usados pelo NIST para avaliar as cifras AES candidatas?

  No conjunto original publicado em 1997 houveram 10 critérios dividos em 3 categorias distintas Segurança, Custo e Características de Implementação e são dividos da seguinte forma:
    
    Segurança:
    
        ● Segurança geral (comparado aos outros candidatos)
        
        ● Aleatoriedade
        
        ● Solidez Matemática
        
        ● Outros Fatores de Segurança (levantados pelo público durante o processo de avaliação)
        
    Custo:
        ● Requerimentos de Licenciamento (algoritmos candidatos devem estar disponíveis mundialmente, sem exclusividade e royalty-free)
        
        ● Eficiência Computacional
        
        ● Requerimentos de Memória
        
    Características de Implementação:
    
        ● Flexibilidade
        
        ● Aptidão para Software e Hardware
        
        ● Simplicidade

## 2. Qual foi o conjunto final de critérios usados pelo NIST para avaliar as cifras AES candidatas?
   
  ● Segurança Geral (baseado na analise de segurança conduzida pela comunidade de criptografia de maneira pública que se preocupa especificamente com ataques cryptoanalíticos que exploram propriedades matemáticas.)

  ● Implementação em Software (agilidade de desenvolvimento, performance inter-plataforma, etc.)

  ● Ambientes de Espaço Restrito (representações de objetos de dados usados no algorítmo devem ser capazes de serem armazenados em pequenas quantidades de ROM e/ou RAM)

  ● Implementação em Hardware

  ● Ataques em Implementação (critério que involve análises para outros tipos de ataques diferentes dos analisados no primeiro critério)

  ● Criptografia versus Descriptografia (Caso o algoritmo seja diferente entre as duas funcionalidades então o espaço extra é necessário, além disso o tempo pode diferir entre os dois)

  ● Agilidade de Chave (Habilidade de trocar chaves de forma rápida e com mínimo recurso)

  ● Outras Versatilidades e Flexibilidades

  ● Potencial para paralelismo à nível de instrução

## 3. Qual é a diferença entre Rijndael e AES?

  AES (Advanced Encryption Standard) é o Padrão de criptografia que a NIST, Agência Americana, acredita que deva ser adotado por todos para uma melhor segurança

  Rijndael é o algoritmo que foi candidato à se tornar o AES e venceu, então hoje o Rijndael é considerado o AES, mas nada garante que o será para sempre.

## 4. Responda:

### (a) Qual é a finalidade do array Estado?

### (b) Como é construída a S-box?

### (c) Descreva rapidamente o estágio SubBytes, ShiftRows, MixColumns, AddRoundKey, e o algoritmo de expansão de chave.

a) Armazenar os dados para serem manipulados à cada etapa da criptografia ou descriptografia do algorítmo

b) 1. A S-box é iniciada com valores de byte em sequência crescente linha à linha de maneira que o valor do byte da linha y, coluna x é {yx}

   2. Depois é mapeado cada byte com seu inverso multiplicativo em GF(2^8)
    
   4. é aplicado uma transformação específica em cada bit de cada byte da S-box

c) 
   + SubBytes:
    Nesta etapa, cada byte do array Estado passa por uma substituição não linear utilizando a S-box, que é uma tabela de substituição especial. A S-box mapeia cada byte de entrada para um byte de saída correspondente. Essa substituição não linear confunde os dados.
   
   + ShiftRows:
    faz uma rotação circular à esqueda de bytes linha á linha a quantidade de rotações é diretamente ligado a qual o número da linha, ex: linha 0: nenhuma rotação, linha 3: três rotações.
   
   + MixColumns:
    Cada byte de uma coluna é mapeado para um novo valor através da multiplicação do Estado por uma Matriz, combinando linearmente os bytes de cada coluna, aumentando a difusão nos dados.
   
   + AddRoundKey:
     Através de uma operação XOR, cada byte do array Estado é combinado com um byte correspondente da chave da rodada bit a bit.
   Expansão de chave: Como o nome diz, gera uma lista expandida de sub-chaves a partir da chave de entrada que de 4 palavras iniciais, 


## 5. Quantos bytes em Estado são afetados por ShiftRows?
  
  Todos os bytes menos os da linha 0

## 6. Use a chave 1010 0111 0011 1011 para encriptar o texto claro "ok"conforme expresso em ASCII, ou seja, 0110 1111 0110 1011. Os projetistas do S-AES obtiveram o texto cifrado 0000 0111 0011 1000. E você?


## 7. Compare AES com DES. Para cada um dos seguintes elementos do DES, indique o elemento comparável no AES ou explique por que ele não é necessário no AES.

(a) XOR do material da subchave com a entrada da função f.

(b) XOR da saída da função f com a metade esquerda do bloco.

(c) função f.

(d) permutação P.

(e) troca de metades do bloco.


a) O elemento comparável em AES é o AddRoundKey

b) Não é necessário no AES, no AES não há necessidade de uma estrutura de rede Feistel onde é necessário divisão de metades e permutação entre as mesmas, em vez disso em várias das etapas de AES há permutações byte á byte ou bit á bit

c) Levando em consideração que a funcão f de DES seja a função com todas as etapas exceto a de manipulação de chave, podemos dizer que a função f de AES consiste em todos os passos tirando o passo de Expansão de Chave.

d) Não há um elemento de comparação direta em AES, pois de novo esse elemento está diretamente ligado à estrutura de rede Feistel do DES fazendo uma reorganização dos bits da metade direita, entretanto temos em AES o ShiftRows e o MixColumns que também fazem uma reorganização.

e) Não é necessário em AES cada passo de AES faz alterações em todo o bloco, não há uma divisão de metades como na estrutura Feistel.
