# Tony Jonas

# Projeto Tradutor Transformer Local

> Este projeto demonstra a implementação de um tradutor utilizando a arquitetura Transformer com TensorFlow. O objetivo é mostrar que é possível desenvolver, treinar e utilizar um tradutor local, sem depender de serviços externos, mesmo que os resultados não sejam perfeitos.

## Resultados e Métricas
- **Desempenho:**
  - GPU: Cada época foi executada em média em 105 segundos.
  - CPU: O treinamento foi cerca de 30 vezes mais lento, levando aproximadamente 3000 segundos por época.

## Pontos Positivos
- Acessibilidade Local: Temos acesso a um tradutor de forma local. Se pensarmos há 50 anos, a maioria diria que seria impossível, mas hoje pessoas comuns conseguem implementar e utilizar essa tecnologia em casa.
- Resultados Promissores: Mesmo com um número reduzido de épocas, os resultados foram bastante interessantes. Por exemplo:
  - **Input**: “os meus vizinhos ouviram sobre esta ideia.”
  **Prediction**: “my neighbors heard about this idea .”
  **Ground truth**: “and my neighboring homes heard about this idea”
  - **Input**: “este é um problema que temos que resolver.”
  **Prediction**: “this is a problem that we need to solve .”
  **Ground truth**: “this is a problem that we have to solve .”
- Privacidade e Flexibilidade: Ao usar um tradutor local, não é necessário enviar dados para servidores externos, o que aumenta a privacidade e permite maior controle sobre o fluxo dos dados.
- Potencial de Aperfeiçoamento: A arquitetura Transformer é altamente escalável e permite várias melhorias. Com mais tempo de treinamento, dados de maior qualidade e ajustes finos nos hiperparâmetros, os resultados podem se tornar ainda mais precisos. Junto a isso, achei bem interessante os checkpoints para poder continuar o processamento de onde paramos, não precisando rodar tudo do 0 novamente.

## Pontos Negativos
- Tempo de Treinamento Elevado: O tempo necessário para treinar o modelo é bastante alto. Enquanto a GPU executa uma época em torno de 105 segundos (o que pra mim já foi alto, pois foi 105 segundos na T4 da Google, onde no meu pessoal tava dando cerca de 250 segundos), a CPU pode levar até 3000 segundos por época, o que é inviável para muitos experimentos ou aplicações em tempo real.
- Exigência de Recursos Computacionais: Para um desempenho razoável, é necessário o uso de uma GPU. Usuários sem acesso a hardware adequado podem encontrar dificuldades para treinar ou até mesmo utilizar o modelo de forma eficiente.
- Qualidade Limitada com Treinamento Reduzido: Devido ao número reduzido de épocas do meu caso, a qualidade da tradução não foi chegou perto de ser 100% fiel.
- Complexidade do Modelo: Mesmo o código estando todo pronto, tive que alterar diversas linhas.
