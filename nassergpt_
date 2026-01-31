<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NasserGPT</title>
<style>
body { font-family: Arial; background: #f6f6f6; margin:0; display:flex; flex-direction:column; height:100vh; }
#messages { flex:1; overflow-y:auto; padding:20px; }
.message { padding:10px; margin:5px 0; border-radius:5px; max-width:80%; }
.user { background:#007bff; color:white; align-self:flex-end; }
.bot { background:#e5e5e5; color:black; align-self:flex-start; }
#inputArea { display:flex; padding:10px; background:white; }
#input { flex:1; padding:10px; border:1px solid #ccc; border-radius:5px; }
button { padding:10px 20px; margin-left:10px; border:none; border-radius:5px; background:#007bff; color:white; }
body::before { content:'به ناسر چی پی تی خوش امدید.'; position:fixed; top:10px; right:10px; font-size:20px; color:#ccc; }
</style>
</head>
<body>
<div id="messages">
<div class="message bot">Willkommen bei NasserGPT! Schreib mir was…</div>
</div>
<div id="inputArea">
<input type="text" id="input" placeholder="Schreibe etwas...">
<button onclick="sendMessage()">Senden</button>
</div>

<script>
const messages = document.getElementById('messages');
const input = document.getElementById('input');

function generateReply(text){
  const t = text.toLowerCase();
  if(t.includes('hallo')||t.includes('hi')) return 'Hallo 👋 Wie kann ich dir helfen?';
  if(t.includes('wer bist')) return 'Ich bin NasserGPT – ein KI-ähnlicher Chat (Demo).';
  if(t.includes('hilfe')) return 'Sag mir einfach, wobei du Hilfe brauchst.';
  return 'Interessant. Erzähl mir mehr darüber.';
}

function sendMessage(){
  const text = input.value.trim();
  if(!text) return;
  const userMsg = document.createElement('div');
  userMsg.className = 'message user';
  userMsg.textContent = text;
  messages.appendChild(userMsg);
  input.value='';
  messages.scrollTop = messages.scrollHeight;

  const typing = document.createElement('div');
  typing.className='message bot';
  typing.textContent='NasserGPT schreibt…';
  messages.appendChild(typing);
  messages.scrollTop = messages.scrollHeight;

  setTimeout(()=>{
    typing.remove();
    const botMsg = document.createElement('div');
    botMsg.className='message bot';
    botMsg.textContent = generateReply(text);
    messages.appendChild(botMsg);
    messages.scrollTop = messages.scrollHeight;
  },800);
}
</script>
</body>
</html>
