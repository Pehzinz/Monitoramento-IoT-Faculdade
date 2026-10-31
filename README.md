# Sistema de Monitoramento IoT - Salas 101 e 202 🌐

Repositório dedicado ao projeto acadêmico da disciplina de Internet das Coisas (IoT). O sistema realiza o monitoramento simulado de duas salas (Sala 101 e Sala 202) utilizando microcontroladores virtuais, integração via MQTT, processamento de fluxos no Node-RED e visualização de dados no Grafana.

## 📺 Apresentação do Projeto
Assista ao vídeo detalhando o funcionamento da arquitetura, os fluxos de dados e os dashboards criados:
- [Vídeo de Apresentação no YouTube](https://youtu.be/jRlgJJYUdMA?si=wTcFC5iyEliEPmyD)

## 📸 Imagens do Projeto
*Abaixo estão as capturas de tela do sistema em funcionamento:*

![Dashboard Grafana](./Imagens/grafana)
![Fluxo Node-RED](./Imagens/nodered)
![Simulação Wokwi](./Imagens/Wokwi)
![Telegram](./Imagens/telegram)

*(Nota: Substitua os nomes dos arquivos acima pelos nomes exatos das imagens que você colocar dentro da pasta `/Imagens`)*

## 🛠️ Tecnologias e Arquitetura

O ecossistema do projeto foi construído utilizando as seguintes ferramentas:

*   **Wokwi:** Simulação do hardware (ESP32) e dos sensores do ambiente.
*   **MQTT (Protocolo):** Mensageria leve para comunicação entre os dispositivos simulados e o servidor.
*   **Node-RED:** Backend visual para orquestração, recebimento dos dados via MQTT e roteamento.
*   **Grafana:** Criação de dashboards dinâmicos para acompanhamento das métricas das salas em tempo real.

## 💻 Dispositivos Virtuais (Wokwi)

Os circuitos simulados podem ser acessados e executados diretamente no navegador através dos links abaixo:

- 🚪 **Sala 101:** [Acessar Simulação Wokwi](https://wokwi.com/projects/471993538215699457)
- 🚪 **Sala 202:** [Acessar Simulação Wokwi](https://wokwi.com/projects/471993598759438337)

## 📁 Estrutura do Repositório

- `/Documentos`: Contém as documentações do projeto (Entregas parciais e manuais).
- `/Grafana`: Arquivos e links de referência para acesso ao dashboard do Grafana.
- `/Imagens`: Capturas de tela do sistema em funcionamento, painéis e diagramas.
- `/Node-RED`: Contém o arquivo `node-red.json` com os fluxos (flows) de integração para importação.
- `/Wokwi`: Códigos-fonte e bibliotecas utilizadas nos microcontroladores ESP32 de cada sala.

## 🚀 Como Executar o Projeto

1. **Simulação dos Dispositivos:** Abra os links do Wokwi listados acima e inicie a simulação (botão "Play"). Os dispositivos começarão a publicar dados no broker MQTT configurado.
2. **Backend (Node-RED):** 
   - Inicie sua instância do Node-RED.
   - Vá no menu superior direito > *Import*.
   - Selecione o arquivo `node-red.json` localizado na pasta `/Node-RED` deste repositório.
   - Faça o *Deploy* para iniciar a recepção dos dados.
3. **Dashboards (Grafana):**
   - Acesse o link do Grafana disponibilizado na pasta `/Grafana`.
   - Certifique-se de que a fonte de dados (Data Source) está conectada ao broker/banco de dados alimentado pelo Node-RED.
