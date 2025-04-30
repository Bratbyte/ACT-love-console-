# ACT-love-console-
I love you.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ACT LOVE CONSOLE</title>
  <style>
    body {
      background-color: black;
      color: #00ff99;
      font-family: monospace;
      padding: 20px;
      overflow: hidden;
    }
    #terminal {
      white-space: pre-line;
      height: 90vh;
      overflow-y: auto;
    }
    #input {
      width: 100%;
      border: none;
      background: black;
      color: #00ff99;
      font-family: monospace;
      font-size: 1em;
      outline: none;
    }
  </style>
</head>
<body>
  <div id="terminal">ACT LOVE CONSOLE v1.0\nConnected to: GF-Flight-Tower ❤\nType 'help' for commands.</div>
  <input id="input" autofocus />

  <script>
    const terminal = document.getElementById('terminal');
    const input = document.getElementById('input');

    const responses = {
      help: `Available commands:\nSTATUS\nSEND_LOVE\nLAUNCH_HEART\nCLEARANCE\nLOGBOOK\nHELP`,
      status: `HEARTBEAT: Stable\nALTITUDE: High on love\nCOORDINATES: Locked on you ❤`,
      send_love: `\nTransmitting message...\n"My love for you is cruising at 36,000 feet and only going higher." 💌`,
      launch_heart: `
       .-.    
     __|=|__
    (_/"""\\_)   ❤❤❤
    /_______\\   
     _\\___/_\\_  
     /_/   \\_\\  `,
      clearance: `\nRequesting permission to land...\nClearance GRANTED.\nWelcome to Gate: H-E-A-R-T ❤`,
      logbook: `\nFLIGHT LOG:
- 2023-02-14: First flight together
- 2023-07-01: Turbulence, but love held strong
- 2024-01-01: New year, new adventures
- Today: Still flying together ❤`
    };

    input.addEventListener('keydown', (e) => {
      if (e.key === 'Enter') {
        const cmd = input.value.trim().toLowerCase();
        terminal.innerText += `\n> ${cmd}`;
        const res = responses[cmd] || `Unknown command. Type 'help' for list.`;
        terminal.innerText += `\n${res}`;
        input.value = '';
        terminal.scrollTop = terminal.scrollHeight;
      }
    });
  </script>
</body>
</html>
