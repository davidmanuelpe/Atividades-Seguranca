# Lista 6

## 1. Qual é a diferença entre aleatoriedades estatísticas e imprevisibilidade?

  R: 
    A diferença entre aleatoriedade estatística e imprevisibilidade está relacionada à capacidade de prever os próximos valores gerados em um processo aleatório. A aleatoriedade estatística se concentra na distribuição dos valores gerados, enquanto a imprevisibilidade se concentra na dificuldade de prever os valores futuros, mesmo com conhecimento do algoritmo e dos valores anteriores. Tanto para PRNGs quanto para cifras de fluxo, a imprevisibilidade é essencial para garantir a segurança e proteção dos dados sensíveis.

## 2. Liste considerações de projeto importantes para uma cifra de fluxo.

  R:

   - Segurança Criptográfica:
        
      A segurança é a principal preocupação. A cifra deve ser resistente a ataques criptográficos conhecidos, como ataques de força bruta, análise diferencial, ataques de canal lateral, entre outros.
        
   - Imprevisibilidade:

      A geração de sequências de bits deve ser imprevisível para um adversário que conhece o algoritmo subjacente. A previsibilidade pode levar à quebra da cifra.
        
   - Eficiência Computacional:
    
      A cifra deve ser projetada para ser eficiente em termos de processamento e recursos computacionais, a fim de ser usada em dispositivos com recursos limitados, como dispositivos móveis ou sistemas embarcados.

  - Resistência a Ataques de Canal Lateral:

      A cifra deve ser projetada para minimizar vazamentos de informações através de ataques de canal lateral, como análise de tempo, análise de consumo de energia e análise de radiação eletromagnética.

  - Algoritmo de Geração de Chave Seguro:

      O algoritmo usado para gerar a chave de cifração a partir da chave mestra deve ser seguro e robusto, impedindo a inferência da chave mestra a partir das chaves de cifração geradas.

  - Distribuição de Chaves:

      Um sistema de distribuição de chaves seguro é essencial para garantir que as chaves usadas na cifra de fluxo sejam compartilhadas apenas com as partes autorizadas.

  - Avaliação de Testes de Aleatoriedade:

      As sequências geradas pela cifra devem passar em testes de aleatoriedade estatística para garantir que se assemelhem a sequências verdadeiramente aleatórias.

  - Rotação de Chave e Não-Repetição:

      A cifra deve ser projetada para evitar a repetição de sequências de bits, o que poderia tornar a cifra vulnerável a ataques de repetição.

  - Tamanho da Chave e Tamanho do Vetor de Inicialização (IV):

      O tamanho da chave e do IV (caso a cifra use um) influencia diretamente a segurança da cifra. Um tamanho inadequado pode resultar em vulnerabilidades.

  - Análise de Impacto de Ataques Conhecidos:

      É importante considerar como a cifra resiste a diferentes tipos de ataques criptográficos conhecidos, como ataques de texto cifrado escolhido, ataques de texto claro escolhido, entre outros.

  - Ataques em Estado Parcial:

      A cifra deve ser projetada para resistir a ataques em estado parcial, onde um adversário pode ter acesso apenas a uma parte do fluxo de bits.

  - Implementação Correta e Segura:

      A implementação da cifra em software ou hardware deve ser cuidadosa e segura, evitando vulnerabilidades como buffer overflows, vazamentos de informações, etc.

  - Flexibilidade e Adaptabilidade:

      A cifra deve ser projetada para ser adaptável a diferentes cenários e requisitos de segurança, permitindo a configuração de parâmetros relevantes.

  - Revisão por Pares e Avaliação Externa:

      O design da cifra deve ser revisado por pares e também ser sujeito a avaliações independentes e auditorias de segurança.

  - Padronização e Compatibilidade:

      Se a cifra for destinada a uso em padrões criptográficos, deve atender aos requisitos de padronização e ser compatível com outros sistemas criptográficos.

## 3. Por que não é desejável reutilizar uma chave de cifra de fluxo?

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

## 4. Que operações primitivas são usadas no RC4?

  R:

   Swap (Troca):

    A operação de troca envolve a troca de dois elementos em uma matriz ou em um vetor. No contexto do RC4, essa operação é usada para permutar elementos do estado interno do algoritmo (S-box). Isso é feito para embaralhar os elementos e introduzir confusão no processo de geração da sequência de bytes pseudoaleatórios.

   XOR (OU Exclusivo):

    A operação XOR é fundamental no RC4 para combinar o estado interno (S-box) com os dados de entrada (chave e vetor de inicialização) a fim de produzir o fluxo de bits pseudoaleatório. A operação XOR é aplicada para misturar os bits dos elementos do S-box com os bits da chave e do vetor de inicialização, gerando a sequência de saída.

## 6. 

### (a) Qual é o período máximo que pode ser obtido do seguinte gerador? Xn+1 = (a*Xn) mod 2^4

R:  
  A sequência terá uma quantidade de elementos limite igual ao tamanho do módulo que nesse caso é 16, e então teremos o período máximo da sequência entre 0 e 15.

### (b) Qual deverá ser o valor de a?

R:  
  O valor de a poderá ser qualquer valor desde 0 <= a < m, para o a que atinge o maior período possível para esse módulo temos, 3 e 11 atingindo 4 valores antes de começar a se repetir.

### (c) Que restrições são exigidas na semente?

R:  
  Que a seja um valor inteiro no intervalo 0 <= a <= m - 1.

## 7. Que valor de chave RC4 deixará S inalterado durante a inicialização? Ou seja, após a permutação inicial de S, as entradas de S serão quais aos valores de 0 a 255 na ordem crescente.

R:  
  A chave que resultará em um estado interno inalterado durante a inicialização do RC4 é uma sequência de valores de 0 a 255 em ordem crescente.