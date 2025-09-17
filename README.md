## Hi there 👋

<!--
**mendes0000/mendes0000** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
import random
import time

# Times fictícios
time_a = "Estudantes FC"
time_b = "Futebol Clube Python"

# Placar inicial
placar = {time_a: 0, time_b: 0}

# Função para simular um gol
def simular_gol():
    return random.choice([time_a, time_b, None])  # None = jogada perdida

# Início da partida
print("🏟️ Bem-vindo ao grande clássico estudantil!")
print(f"{time_a} vs {time_b}")
print("🔔 Início da partida!\n")

# Simulação de 10 jogadas
for minuto in range(1, 11):
    print(f"⏱️ Minuto {minuto}...")
    time.sleep(1)  # pausa dramática
    resultado = simular_gol()
    if resultado:
        placar[resultado] += 1
        print(f"⚽ GOOOOOL do {resultado}!")
    else:
        print("🚫 Jogada desperdiçada... a torcida vai à loucura!")
    print(f"Placar parcial: {time_a} {placar[time_a]} x {placar[time_b]} {time_b}\n")

# Fim de jogo
print("🔚 Fim de jogo!")
print(f"🏁 Placar final: {time_a} {placar[time_a]} x {placar[time_b]} {time_b}")

# Resultado
if placar[time_a] > placar[time_b]:
    print(f"🎉 Vitória do {time_a}! Os estudantes comemoram!")
elif placar[time_b] > placar[time_a]:
    print(f"🏆 {time_b} vence! Python mostra que também sabe jogar bola!")
else:
    print("🤝 Empate justo! Que partida emocionante!")
