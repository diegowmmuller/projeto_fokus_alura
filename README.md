# ⏱️ Fokus - Timer Pomodoro com JavaScript

## 📌 Descrição

O **Fokus** é uma aplicação web de temporizador baseada na técnica Pomodoro, que alterna entre períodos de foco e descanso. O projeto foi desenvolvido com o objetivo de praticar conceitos fundamentais de **JavaScript**, manipulação de DOM e controle de tempo com `setInterval`.

---

## 🚀 Funcionalidades

- Alternar entre modos:
  - 🧠 Foco (25 minutos)
  - ☕ Descanso curto (5 minutos)
  - 🌴 Descanso longo (15 minutos)

- Iniciar e pausar o temporizador
- Exibição do tempo em formato `mm:ss`
- Reprodução de:
  - Música ambiente durante o foco
  - Som ao iniciar
  - Som ao pausar
  - Alerta ao finalizar o tempo

- Alteração dinâmica de:
  - Texto
  - Imagem
  - Estado visual dos botões

---

## 🧠 Conceitos praticados

### 📍 Manipulação do DOM

- `document.querySelector`
- `classList.add/remove`
- `setAttribute`
- `innerHTML` e `textContent`

### ⏱️ Controle de tempo

- `setInterval`
- `clearInterval`
- Lógica de contagem regressiva

### 🎧 Manipulação de áudio

- Objeto `Audio`
- Métodos:
  - `.play()`
  - `.pause()`
  - `.loop`
  - `.currentTime`

### 🎯 Eventos

- `addEventListener`
- Eventos de clique (`click`)
- Eventos de mudança (`change`)

### 🔄 Controle de estado

- Uso de variáveis globais para:
  - Tempo (`tempoDecorridoEmSegundos`)
  - Controle do intervalo (`intervaloId`)

---

## 🏗️ Estrutura da lógica

### ▶️ Inicialização

- Define o tempo inicial (foco por padrão)
- Atualiza o display com `mostrarTempo()`

### 🔁 Contagem regressiva

- Executada a cada 1 segundo com `setInterval`
- Decrementa o tempo
- Atualiza a tela
- Para quando chega a 0

### ⏯️ Controle de execução

- `iniciarOuPausar()`:
  - Inicia o timer se estiver parado
  - Pausa se já estiver rodando

- `zerar()`:
  - Interrompe o intervalo
  - Reseta o estado do botão
  - Toca áudio de pausa

---

## 🧮 Formatação do tempo

O tempo é convertido usando:

```js
new Date(tempoDecorridoEmSegundos * 1000);
```

E formatado com:

```js
toLocaleTimeString('pt-br', {
	minute: '2-digit',
	second: '2-digit',
});
```

---

## 📁 Estrutura esperada do projeto

```
📂 projeto
 ├── 📂 imagens
 ├── 📂 sons
 ├── index.html
 ├── style.css
 └── script.js
```

---

## ⚙️ Como executar

1. Clone o repositório:

```bash
git clone https://github.com/diegowmmuller/projeto_fokus_alura.git
```

2. Abra o projeto:

```bash
cd projeto_fokus_alura
```

3. Execute o `index.html` no navegador

---

## 📚 Objetivo do projeto

Este projeto foi desenvolvido com foco em consolidar conhecimentos básicos de JavaScript, especialmente:

- Controle de fluxo
- Manipulação de elementos da página
- Interatividade com o usuário
- Organização de código

---

## 👨‍💻 Autor

Desenvolvido por Diego Maglia durante estudos de JavaScript na trilha de front-end da Alura.
