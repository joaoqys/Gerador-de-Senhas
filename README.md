### Gerador de Senhas

Este é um exemplo de código para um gerador de senhas com diversos recursos para criar e gerenciar senhas fortes.

### Elementos HTML:

- #password: Campo de entrada onde a senha gerada é exibida.
- #uppercase-check: Caixa de seleção para incluir letras maiúsculas na senha.
- #number-check: Caixa de seleção para incluir números na senha.
- #symbol-check: Caixa de seleção para incluir símbolos na senha.
- #security-indicator-bar: Elemento que representa a força da senha visualmente (como uma barra).
- #password-length: Campo de entrada para especificar o comprimento desejado da senha.
- #password-length-text: Exibe o comprimento atual da senha.
- #copy-1 e #copy-2: Botões para copiar a senha gerada para a área de transferência.
- #renew: Botão para gerar uma nova senha.
  
###Funções JavaScript:

- generatePassword():
- Define conjuntos de caracteres para letras minúsculas, letras maiúsculas, números e símbolos.
- Concatena conjuntos de caracteres com base nas seleções de caixa de seleção (maiúsculas, números, símbolos).
- Gera uma senha aleatória com o comprimento especificado iterando através do conjunto de caracteres combinado.
- Define o valor do campo de entrada #password para a senha gerada.
- Chama calculateQuality() para atualizar o indicador de força da senha.
- Chama calculateFontSize() para ajustar o tamanho da fonte com base no comprimento da senha.
- calculateQuality():
- Calcula uma pontuação com base no comprimento da senha (25%), inclusão de maiúsculas (15%), inclusão de números (25%) e inclusão de símbolos (35%).
- Define a largura do elemento #security-indicator-bar com base na pontuação calculada.
- Atribui classes CSS ao elemento #security-indicator-bar para representar visualmente a força da senha (crítica, aviso, segura).
- Adiciona uma classe "completed" se a pontuação atingir 100%.
- calculateFontSize():
- Atribui classes CSS ao campo de entrada #password para ajustar o tamanho da fonte com base no comprimento da senha (extra pequeno, pequeno, médio) para melhor legibilidade.
- copy():
- Usa a função navigator.clipboard.writeText() para copiar o valor da senha para a área de transferência.
- Eventos de Escuta:

- Entrada #password-length: Dispara generatePassword() em qualquer alteração para atualizar a senha com base no novo comprimento.
- Caixas de seleção #uppercase-check, #number-check, #symbol-check: Disparam generatePassword() ao clicar para atualizar a senha com base na seleção do conjunto de caracteres.
- Botões #copy-1 e #copy-2: Disparam copy() para copiar a senha gerada.
- Botão #renew: Dispara generatePassword() para gerar uma nova senha.
