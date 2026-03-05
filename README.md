# Laboratório de Análise de Tráfego de Rede com Wireshark

## 📌 Objetivo
Este laboratório tem como objetivo analisar o tráfego de rede gerado durante uma navegação na internet, utilizando a ferramenta Wireshark. A ideia é observar como ocorre a comunicação entre máquinas, identificando protocolos, requisições e respostas dentro da rede.

## 🧪 Ferramenta utilizada
- Wireshark

## 🖥️ Ambiente do laboratório
- Computador pessoal
- Conexão com internet
- Wireshark instalado para captura de pacotes

## 🔍 Experimento
Foi realizada uma captura de tráfego durante a navegação em sites da internet, com o objetivo de identificar os tipos de comunicação que acontecem entre o computador do usuário e os servidores.

## 📊 Protocolos observados
- DNS
- TCP
- HTTP/HTTPS

## 📚 Aprendizados
Durante a análise foi possível observar como diferentes protocolos trabalham juntos para permitir a comunicação na internet.

## Análise de tráfego TCP com Wireshark

Durante este laboratório foi realizada uma captura de tráfego de rede utilizando o Wireshark para observar o processo de estabelecimento de conexões TCP.

Para identificar tentativas de início de conexão foi utilizado o filtro:

tcp.flags.syn == 1

Esse filtro permite visualizar pacotes responsáveis por iniciar conexões TCP (SYN).

A captura mostra o processo conhecido como Three-Way Handshake:

- SYN – solicitação de conexão enviada pelo cliente
- SYN/ACK – resposta do servidor confirmando a solicitação
- ACK – confirmação final do cliente estabelecendo a conexão

Durante a análise também foram observados eventos de **TCP Retransmission**, indicando que alguns pacotes precisaram ser reenviados devido à ausência de resposta dentro do tempo esperado.

## Evidências da captura de tráfego

### 1. Captura de pacotes TCP
Análise inicial do tráfego mostrando diferentes pacotes TCP capturados na rede.

<img width="697" height="669" alt="capture-overview png" src="https://github.com/user-attachments/assets/7dbed6e1-2017-45b4-8e00-ff0bcf38777a" />

### 2. Filtro para identificação de conexões
Aplicação do filtro tcp.flags.syn == 1 para identificar tentativas de início de conexão TCP.

<img width="683" height="642" alt="dns-analysis png" src="https://github.com/user-attachments/assets/35f0d38e-8c3a-406a-a89e-8c0ea23c137f" />

### 3. Identificação de retransmissões
Durante a análise foram observados eventos de TCP Retransmission, indicando que alguns pacotes precisaram ser reenviados.

<img width="881" height="621" alt="tcp-handshake png" src="https://github.com/user-attachments/assets/60e26f8d-79e0-4a9a-a7db-092c58a2f364" />

<img width="1012" height="546" alt="Captura de tela 2026-03-05 155056" src="https://github.com/user-attachments/assets/7db8f8f4-1f7f-4a81-a328-098cb9b7ad75" />

