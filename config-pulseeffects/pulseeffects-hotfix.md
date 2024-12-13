## Transição entre movies e music
Quando o áudio der uma sensão de estar "estourado", onde as frequências mais agudas e as partes altas da música ficarem distorcidas, existem algumas soluções para este tipo de problema:

**solução 1:**
- diminuir a faixa de áudio do pulseeffects no pavucontrol em *dispositivos de saída*
- para música: 69% - 59% ou menos [sendo 69 o teto]
- para filmes: abaixo de 90%

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
---