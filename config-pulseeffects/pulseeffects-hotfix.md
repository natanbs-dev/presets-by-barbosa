## Transição entre movies e music
Quando o áudio der uma sensão de estar "estourado", onde as frequências mais agudas e as partes altas da música ficarem distorcidas, existem algumas soluções para este tipo de problema:

**solução 1:**
- diminuir a faixa de áudio do pulseeffects no pavucontrol em *dispositivos de saída*
- para música: 69% - 49% ou menos [sendo 69 o teto; caso acima desse valor, distorce a qualidade do vocal]
- para filmes: abaixo de 90%
- foi notado que a interface **kde** se saiu melhor nos testes quanto as modificações no buffer e latência

**solução 2:**
- rodar o comando para reiniciar o pipewire
- `systemctl --user restart pipewire`

---
## Solução de possíveis travamentos:

O buffer e latências estão entre os pontos que, uma vez modificados, tiveram efeito positivo na solução desses pequenos travamentos em faixas de áudio de filmes [tanto streaming, como local]
Abaixo tantos as configurações originais como as modificadas: 

### configs originais:
**buffer:** 200000
**latência:** 10000

### configuração acerta #1:
**buffer:** 131072
**latência:** 25000

### configuração acerta #2:
**buffer:** 65536
**latência:** 25000


## Erro no gtk 

Caso o erro no gtk sendo que, mesmo com o tema black, o app permaneça com o tema white, troque as configurações do app diretamente no gtk

---
