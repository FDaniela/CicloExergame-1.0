# Avaliação do CicloExergame como um sistema

## _Funcionalidade de Comunicação_

![Tela](/Imagens/tele.png)

Em telerreabilitação, a videoconferência é uma forma interativa de comunicação entre paciente e profissional de saúde, ocorrendo em locais diferentes. Ela inclui comunicação de áudio, visualização de imagens em tempo real e troca de mensagens de texto, permitindo a comunicação com outros participantes da chamada como se estivessem fisicamente presentes. O CicloExergame é um sistema de telerreabilitação que utiliza o WebRTC para transmissão de áudio e imagem em tempo real entre fisioterapeuta e paciente, sem depender de um servidor de banco de dados externo.

### Testes Funcionais

Testes são essenciais para garantir a qualidade de uma aplicação, encontrando erros antes de sua utilização. É impossível testar todas as entradas possíveis, por isso busca-se projetar casos de testes estratégicos e sistemáticos para verificar os requisitos do software.


### Teste Caixa-Preta 

Os testes caixa-preta são projetados para examinar o software a partir da perspectiva do usuário, sem a análise de sua estrutura ou código-fonte. Essa técnica busca identificar erros de comportamento, erros de interface e funções ausentes ou incorretas do software, sendo uma estratégia eficiente para testar os requisitos funcionais.

A técnica de caixa-preta é útil para determinar se um software está funcionando corretamente e atendendo aos requisitos do usuário. Os critérios comuns usados em testes funcionais incluem particionamento de equivalência, análise de valor limite, grafo causa-efeito e Error Guessing. Todos esses critérios se baseiam nas especificações do software para criar casos de teste. Para o Cicloexergame, que lida com comunicação em tempo real e arquiteturas distribuídas, o critério Error Guessing será usado para criar casos de teste baseados em erros comuns.

---

### Estruturação dos Casos de Teste

A escolha das métricas de avaliação é crucial para garantir uma avaliação precisa e abrangente do desempenho do sistema. No caso do CicloExergame, as métricas selecionadas são relacionadas à carga de trabalho e à qualidade da comunicação de áudio, dados e vídeo durante a videochamada. Isso inclui o tamanho dos pacotes enviados e recebidos, a perda de pacotes, o atraso e a variação do atraso (jitter) e a taxa de transmissão dos elementos da aplicação.

Para realizar a avaliação de desempenho, a técnica escolhida foi a medição real, que envolve a operacionalização do protótipo com cargas reais. Isso significa que os testes foram realizados em um ambiente real, com uma conexão de rede limitada e uma personalização da taxa de limitação para a taxa de upload e download em um dos peers.

![Grafico](/Imagens/grafh.png)

Para coletar os dados de avaliação, o navegador Google Chrome foi utilizado em todos os casos, devido às suas ferramentas de monitoramento do WebRTC, incluindo o webrtc-internals [webrtc-internals](chrome://webrtc-internals) e o [DevTools](https://developer.chrome.com/docs/devtools/). A decisão de utilizar o webrtc-internals se deve à sua capacidade de gerar relatórios detalhados sobre o funcionamento do WebRTC e suas métricas de comunicação, que são cruciais para a avaliação do desempenho do CicloExergame.

 ---
 
 
## Resultados

![t1](/Imagens/t1.png)

![t2](/Imagens/t2.png)

---

#### Observações Adicionais

    A aplicação não se encontra funcional do momento devido a plataforma de Cloud Computing em que o servidor de sinalização foi hospedado ter mudado suas politicas de uso gratuito.
    
    
- Exemplos dos arquivos de testes que foram produzidos e analizados durante o teste pode ser encontrado em  [Link](https://github.com/FDaniela/Teleconsulta/tree/main/Arquivos%20Extras)
