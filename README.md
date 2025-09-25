# Hey
<!DOCTYPE html>
<html lang="el">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Greetings with Web Speech API</title>
<style>
  body {
    font-family: Arial, sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 15px;
    height: 100vh;
    margin: 0;
    background-color: #f4f4f4;
  }
  button {
    padding: 12px 20px;
    font-size: 18px;
    cursor: pointer;
  }
</style>
</head>
<body>
<h2>Say Hello in Different Languages</h2>
<button onclick="speak('Hello', 'en-US')">Αγγλικά: Hello ▶️ Άκου</button>
<button onclick="speak('Ciao', 'it-IT')">Ιταλικά: Ciao ▶️ Άκου</button>
<button onclick="speak('Hola', 'es-ES')">Ισπανικά: Hola ▶️ Άκου</button>
<button onclick="speak('Hej', 'sv-SE')">Σουηδικά: Hej ▶️ Άκου</button>
<button onclick="speak('Здравей', 'bg-BG')">Βουλγαρικά: Здравей ▶️ Άκου</button>
<button onclick="speak('سلام', 'ar-SA')">Αραβικά: سلام ▶️ Άκου</button>

<script>
function speak(text, lang) {
    const utterance = new SpeechSynthesisUtterance(text);
    utterance.lang = lang;
    speechSynthesis.speak(utterance);
}
</script>
</body>
</html>
