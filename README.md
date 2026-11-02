# Acoplamento XR

Experiência WebXR sobre rendezvous e acoplamento (docking) entre espaçonaves, ambientada na rota da Terra até a Lua.

O objetivo é entender como a interação entre duas naves acontece e quanto controle é preciso para alinhá-las: a dinâmica orbital relativa (equações de Clohessy-Wiltshire / Hill), os seis graus de liberdade do RCS, o corredor de aproximação, o envelope de velocidade e as tolerâncias de captura.

## Missões

1. **Estação em órbita baixa** (400 km): aproximação pela V-bar com a mecânica orbital forte. Acelerar para frente faz a nave subir e ficar para trás.
2. **Depósito de combustível** (rede de reabastecimento perto de L1): quase sem dinâmica orbital, puro controle de seis eixos. Depois do contato, transferência de propelente.
3. **Acoplamento giratório** (órbita lunar baixa): estação que gira para gerar gravidade artificial; é preciso igualar a rolagem antes do contato.

Modos **Física real** e **Treino** (sem dinâmica orbital, mais combustível). Piloto automático disponível para observar a técnica.

## Plataformas

- **VR** (Quest, Pico, Vision Pro): cabine com HUD e retícula; analógicos para translação e rotação.
- **Desktop**: teclado (WASD + R/F translação, setas ou IJKL + Q/E rotação, Espaço estabiliza).
- **Celular**: dois bastões virtuais e botões de subida, descida e rolagem.

## Técnica

Um único `index.html`, sem build. Three.js 0.160 via import map (jsDelivr). Terra, Lua e texturas geradas proceduralmente no carregamento; áudio sintetizado com Web Audio.

Para rodar localmente:

```bash
python -m http.server 8792
```

WebXR exige HTTPS fora de `localhost`, por isso a versão para headset roda pelo GitHub Pages.
