## Emissões de CO₂ associadas (kg)

Fator fornecido: \\(0{,}08\ \text{kg CO₂/kWh}\\), compatível com a ordem de grandeza de fatores médios da matriz elétrica brasileira (cerca de 0,055–0,06 kg CO₂/kWh em anos recentes, dependendo da fonte e do ano). 

### Emissões por paciente

\\[
\text{CO}\_{2,\text{pac,ano}} = E\_{\text{pac,ano}} \cdot 0{,}08 \approx 5{,}96 \cdot 0{,}08 \approx 0{,}48\ \text{kg CO}\_2\text{/ano}
\\]

Ou seja, menos de meio quilo de CO₂ por paciente por ano para manter o sistema 24 h/dia.  

### Emissões para 5 pacientes

\\[
\text{CO₂}\_{\text{5,ano}} = 5 \cdot 0{,}48 = 2{,}4\ \text{kg CO₂/ano} 
\\]

### Emissões para 1 000 pacientes

\\[
\text{CO₂}_{\text{1000,ano}} = 1000 \cdot 0{,}48 \approx 480\ \text{kg CO₂/ano} \approx 0{,}48\ \text{t CO₂/ano}
\\]  

***

## Percentual de consumo do Wi‑Fi no ESP32

A pergunta é “O Wi‑Fi representa qual porcentagem do consumo do ESP32?”. Como a tensão é a mesma nos dois modos, a fração pode ser calculada pela potência média em Wi‑Fi sobre a potência média total.  

\\[
\text{fração}\_{\text{wifi}} = \frac{P\_{\text{wifi,med}}}{P\_{\text{ESP,med}}}
= \frac{0{,}2112}{0{,}3102} \approx 0{,}68
\\]

Logo, o Wi‑Fi responde por aproximadamente \\(68\ \%\\) do consumo médio do ESP32, mesmo ficando apenas 40 % do tempo ativo. A parte em idle (60 % do tempo) responde pelos outros \\(32\ \%\\) do consumo do ESP32.  

***

## Autonomia com a bateria NCR18650B

Autonomia em operação contínua: \\(t = \dfrac{E}{P}\\), usando a potência média total do paciente.  

- Com energia nominal (12,2 Wh):  
  \\[
  t_{\text{nom}} = \frac{12{,}2}{0{,}6802} \approx 18\ \text{h}
  \\]  
- Com energia útil (90 %, \\(E_{\text{útil}} \approx 11{,}0\ \text{Wh}\\)):  
  \\[
  t_{\text{útil}} = \frac{11{,}0}{0{,}6802} \approx 16\ \text{h}
  \\]  

Ou seja, com uma única célula NCR18650B o sistema típico (1 ESP32 + 5 wearables) não chega a 24 h de operação contínua; seriam necessárias mais células em paralelo ou recarga antes de um dia completo. Isso é uma implicação direta de \\(P_{\text{total}} \approx 0{,}68\ \text{W}\\) contra \\(E_{\text{útil}} \approx 11\ \text{Wh}\\).  

***

## Comparação com consultas presenciais semanais

Aqui precisamos explicitar hipóteses de deslocamento. Vou usar uma hipótese simples e relativamente conservadora para mostrar a escala de emissões.  

### Hipóteses adotadas

- 1 consulta presencial por semana por paciente.  
- Deslocamento de ida e volta: \\(d = 20\ \text{km}\\) (10 km para ir, 10 km para voltar).  
- Meio de transporte A: carro a gasolina “médio”, com fator de emissão \\(\approx 0{,}174\ \text{kg CO₂/km}\\), valor típico de inventários internacionais para carros de passeio. 
- Meio de transporte B: ônibus urbano, com emissões per capita cerca de 16 % das de um automóvel, segundo estudos da CNT sobre emissões por passageiro. 

Dessa forma, fator de emissão por passageiro‑km no ônibus:  
\\[
f_{\text{bus}} \approx 0{,}16 \cdot 0{,}174 \approx 0{,}028\ \text{kg CO₂/pax}\cdot\text{km}
\\]

### Emissões anuais por paciente – carro

Distância anual:  
\\[
d_{\text{ano}} = d \cdot 52 = 20 \cdot 52 = 1040\ \text{km/ano}
\\]  

Emissões anuais por paciente, carro:  
\\[
\text{CO₂}\_{\text{carro,pac}} = d\_{\text{ano}} \cdot f\_{\text{carro}} 
= 1040 \cdot 0{,}174 \approx 181\ \text{kg CO₂/ano}
\\]

Comparando com o sistema IoT (\\(\approx 0{,}48\ \text{kg CO₂/ano}\\)): o deslocamento semanal de carro emite quase **380 vezes** mais CO₂ por paciente do que manter a solução remota 24 h/dia.  

### Emissões anuais por paciente – ônibus

Emissões anuais por paciente, ônibus:  
\\[
\text{CO₂}\_{\text{bus,pac}} = d\_{\text{ano}} \cdot f\_{\text{bus}} 
\approx 1040 \cdot 0{,}028 \approx 29\ \text{kg CO₂/ano}
\\]

Mesmo usando transporte coletivo, com pegada por passageiro muito menor que a do carro, as emissões ainda são quase duas ordens de grandeza maiores que as da solução IoT (29 kg vs 0,48 kg por ano).

### Escala para 5 pacientes

- Carro:  
  \\[
  \text{CO₂}\_{\text{carro,5}} \approx 5 \cdot 181 = 905\ \text{kg CO₂/ano} = 0{,}905\ \text{t CO₂/ano}
  \\]  
- Ônibus:  
  \\[
  \text{CO₂}\_{\text{bus,5}} \approx 5 \cdot 29 = 145\ \text{kg CO₂/ano} = 0{,}145\ \text{t CO₂/ano}
  \\]  
- Sistema IoT: \\(\approx 2{,}4\ \text{kg CO₂/ano}\\).  

Mesmo no cenário favorável (tudo de ônibus, distância moderada), as consultas presenciais semanais emitem **centenas de quilos de CO₂** por ano para 5 pacientes, contra **menos de meia dezena de quilo de CO₂** da solução IoT contínua.  

### Escala para 1 000 pacientes

- Carro:  
  \\[
  \text{CO₂}_{\text{carro,1000}} \approx 1000 \cdot 181 = 181\,000\ \text{kg CO₂/ano} = 181\ \text{t CO₂/ano}
  \\]  
- Ônibus:  
  \\[
  \text{CO₂}_{\text{bus,1000}} \approx 1000 \cdot 29 = 29\,000\ \text{kg CO₂/ano} = 29\ \text{t CO₂/ano}
  \\]  
- Sistema IoT: \\(\approx 0{,}48\ \text{t CO₂/ano}\\).  

Mesmo no cenário favorável (tudo de ônibus, distância moderada), as consultas presenciais semanais emitem **dezenas de toneladas de CO₂** por ano para 1 000 pacientes, contra **menos de 1 tonelada** da solução IoT contínua.  

***
