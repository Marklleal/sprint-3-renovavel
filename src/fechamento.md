Qual é a emissão de CO2 por paciente por ano?<br>
R: gera algo em torno de \\(0{,}48\ \text{kg de CO₂/ano}\\),<br>
o que dá aproximadamente \\(6\ \text{kWh/ano}\\) e  usando \\(0{,}08\ \text{kg CO₂/kWh}\\).<br>
[Resposta](./parte_2.md#escala-para-1-000-pacientes)
<br>

Qual seria a emissão para 1.000 pacientes simultâneos?<br>
R: Por paciente, o sistema consome em média cerca de \\(0{,}68\ \text{W}\\)<br>
[Resposta](./parte_2.md#escala-para-1-000-pacientes)
<br>

O Wi-Fi representa qual porcentagem do consumo do ESP-32?
A solução é sustentável quando escalada?<br>
[Resposta](./fechamento.md#a-solução-é-sustentável-quando-escalada)
<br>

Como você interpreta que esta solução se compara, do ponto de vista de emissão de CO2, a consultas presenciais semanais?<br>
[Resposta](./parte_2.md#hipóteses-adotadas)
<br>

Por paciente, o sistema consome em média cerca de \\(0{,}68\ \text{W}\\), o que dá aproximadamente \\(6\ \text{kWh/ano}\\) e gera algo em torno de \\(0{,}48\ \text{kg de CO₂/ano}\\) usando \\(0{,}08\ \text{kg CO₂/kWh}\\). Para 1 000 pacientes, isso corresponde a cerca de \\(6\ \text{MWh/ano}\\) e \\(0{,}48\ \text{t de CO₂/ano}\\), muito abaixo das emissões típicas de deslocamentos semanais de carro ou ônibus para consultas presenciais. 

## A solução é sustentável quando escalada?

Pelos números de energia, o sistema IoT é extremamente “leve” em consumo: cerca de \\(6\ \text{kWh/ano}\\) por paciente, equivalente a deixar uma lâmpada de LED de 6 W ligada 1 000 horas em um ano, algo marginal dentro do consumo residencial típico. Em emissões, isso se traduz em aproximadamente \\(0{,}48\ \text{kg CO₂/ano}\\) por paciente, o que é menor que as emissões de uma única viagem curta de carro. 

Quando escalado para 1 000 pacientes, o consumo fica por volta de \\(6\ \text{MWh/ano}\\), com menos de meia tonelada de CO₂, enquanto a alternativa de consultas presenciais semanais gera da ordem de 30 t (ônibus) a 180 t (carro) de CO₂ por ano apenas com deslocamento, sob hipóteses de distância moderada. Em outras palavras, do ponto de vista de emissões operacionais de uso (não estou considerando fabricação dos dispositivos), a solução IoT é fortemente sustentável e ainda reduz emissões globais se substitui consultas presenciais frequentes. 
<br>
## Fontes:

[matriz elétrica brasileira - epe.gov](https://www.epe.gov.br/sites-pt/publicacoes-dados-abertos/publicacoes/PublicacoesArquivos/publicacao-885/topico-767/BEN_S%C3%ADntese_2025_EN.pdf)<br>
[valor típico de emissão para carro de passeio - climatiq](https://www.climatiq.io/data/emission-factor/5cc66c6a-b273-471a-b378-c974ef8a6df4)<br>
[emissões de passageiro (CNT) - revistaautobus.com](https://revistaautobus.com.br/?p=16067)<br>
[especificações da bateria I - openelectronics](https://www.openelectronics.eu/Akumuliatorius-Panasonic-NCR18650B-3400mAh)<br>
[especificações da bateria II - lygte-info](https://lygte-info.dk/review/batteries2012/Panasonic%20NCR18650B%20Protected%203400mAh%20(Green)%20UK.html)
