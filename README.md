<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>For Saumya, from Ram 🤍</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont,
        "Segoe UI", sans-serif;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: radial-gradient(circle at top, #ffe6ff 0%, #ffcfe9 30%, #0a0b22 100%);
      overflow: hidden;
      color: #fff;
    }

    /* floating hearts background */
    .floating-heart {
      position: fixed;
      width: 18px;
      height: 18px;
      background: #ff7bbf;
      transform: rotate(45deg);
      opacity: 0.6;
      animation: floatUp 10s linear infinite;
      pointer-events: none;
      z-index: 0;
    }
    .floating-heart::before,
    .floating-heart::after {
      content: "";
      position: absolute;
      width: 18px;
      height: 18px;
      background: #ff7bbf;
      border-radius: 50%;
    }
    .floating-heart::before {
      top: -9px;
      left: 0;
    }
    .floating-heart::after {
      left: -9px;
      top: 0;
    }
    @keyframes floatUp {
      0% {
        transform: translateY(0) rotate(45deg);
      }
      100% {
        transform: translateY(-120vh) rotate(45deg);
      }
    }

    .glow-orb {
      position: fixed;
      width: 260px;
      height: 260px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(255, 166, 255, 0.7), transparent 70%);
      filter: blur(4px);
      opacity: 0.6;
      z-index: 0;
    }

    .wrapper {
      position: relative;
      z-index: 2;
      width: min(900px, 95vw);
      padding: 26px 26px 30px;
      background: rgba(10, 10, 25, 0.9);
      border-radius: 22px;
      box-shadow: 0 24px 70px rgba(0, 0, 0, 0.8);
      backdrop-filter: blur(18px);
      border: 1px solid rgba(255, 255, 255, 0.18);
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 22px;
    }

    @media (max-width: 750px) {
      .wrapper {
        grid-template-columns: 1fr;
      }
    }

    .tag {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-size: 11px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      padding: 5px 11px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.06);
      color: #ffd6f2;
      margin-bottom: 12px;
    }
    .tag-dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: #ff5fa3;
      box-shadow: 0 0 12px #ff5fa3;
    }

    h1 {
      font-size: 28px;
      line-height: 1.25;
      margin-bottom: 6px;
    }

    .subtitle {
      font-size: 13px;
      color: #e7c9ff;
      margin-bottom: 18px;
    }

    .chips {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 20px;
    }
    .chip {
      font-size: 11px;
      padding: 4px 10px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.06);
      color: #ffdff9;
      display: inline-flex;
      align-items: center;
      gap: 5px;
    }

    .chip span {
      font-size: 13px;
    }

    .notes-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 10px;
      margin-bottom: 12px;
    }

    @media (max-width: 600px) {
      .notes-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }

    .note-button {
      border: none;
      outline: none;
      cursor: pointer;
      border-radius: 14px;
      padding: 10px 12px;
      font-size: 13px;
      font-weight: 500;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      gap: 4px;
      color: #160617;
      background: linear-gradient(135deg, #ff7fbc, #ffd0f1);
      box-shadow: 0 10px 25px rgba(255, 105, 180, 0.55);
      transition: transform 0.15s ease, box-shadow 0.15s ease, filter 0.2s ease;
      position: relative;
      overflow: hidden;
    }

    .note-button span.small {
      font-size: 11px;
      opacity: 0.85;
      color: #4b0421;
    }

    .note-button .badge {
      position: absolute;
      right: 9px;
      top: 7px;
      font-size: 10px;
      padding: 2px 7px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.75);
      color: #b10057;
      font-weight: 600;
    }

    .note-button:hover {
      transform: translateY(-2px);
      filter: brightness(1.02);
      box-shadow: 0 14px 32px rgba(255, 105, 180, 0.65);
    }

    .note-button:active {
      transform: scale(0.96);
      box-shadow: 0 6px 16px rgba(255, 105, 180, 0.4);
    }

    .hint {
      font-size: 11px;
      color: #e2c6ff;
      opacity: 0.9;
      margin-top: 4px;
    }

    .love-meter {
      margin-top: 16px;
      font-size: 11px;
      color: #f8d7ff;
      display: flex;
      align-items: center;
      gap: 6px;
    }
    .meter-bar {
      flex: 1;
      height: 6px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.14);
      overflow: hidden;
      position: relative;
    }
    .meter-fill {
      position: absolute;
      inset: 0;
      background: linear-gradient(90deg, #ff4f9a, #ffceff, #ff4f9a);
      animation: pulseBar 2.4s ease-in-out infinite;
    }
    @keyframes pulseBar {
      0%,
      100% {
        transform: scaleX(0.9);
        transform-origin: left;
      }
      50% {
        transform: scaleX(1);
        transform-origin: right;
      }
    }

    /* Right side: letter area */
    .letter-card {
      margin-top: 4px;
      padding: 18px 18px 20px;
      background: radial-gradient(circle at top left, rgba(255, 182, 255, 0.16), transparent 60%),
        radial-gradient(circle at bottom right, rgba(132, 94, 255, 0.2), transparent 60%),
        linear-gradient(135deg, rgba(19, 7, 51, 0.9), rgba(37, 0, 70, 0.95));
      border-radius: 18px;
      border: 1px solid rgba(255, 255, 255, 0.18);
      position: relative;
      overflow: hidden;
    }

    .letter-card::before {
      content: "";
      position: absolute;
      inset: 0;
      background-image: radial-gradient(circle at 10% 0%, rgba(255, 255, 255, 0.12) 0, transparent 45%);
      opacity: 0.7;
      pointer-events: none;
    }

    .letter-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 10px;
      position: relative;
      z-index: 1;
    }

    .letter-to {
      font-size: 13px;
      color: #ffe8ff;
    }

    .letter-to span {
      font-weight: 600;
      color: #ffb6e6;
    }

    .tiny-heart {
      font-size: 20px;
      filter: drop-shadow(0 0 9px rgba(255, 118, 177, 1));
      animation: beat 1.3s infinite ease-in-out;
    }

    @keyframes beat {
      0%,
      100% {
        transform: scale(1);
      }
      30% {
        transform: scale(1.2);
      }
      60% {
        transform: scale(0.96);
      }
    }

    .note-title-pill {
      position: relative;
      z-index: 1;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 4px 10px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.06);
      color: #ffd9ff;
      font-size: 11px;
      margin-bottom: 6px;
    }

    .note-title-pill span.index {
      width: 16px;
      height: 16px;
      border-radius: 50%;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      background: rgba(255, 255, 255, 0.85);
      color: #b00054;
      font-size: 10px;
      font-weight: 700;
    }

    .note-title-pill small {
      opacity: 0.9;
    }

    .letter-body {
      position: relative;
      z-index: 1;
      font-size: 13px;
      line-height: 1.65;
      color: #ffe9ff;
      max-height: 250px;
      overflow-y: auto;
      padding-right: 4px;
      white-space: pre-wrap;
    }

    .letter-body::-webkit-scrollbar {
      width: 4px;
    }
    .letter-body::-webkit-scrollbar-thumb {
      background: rgba(255, 255, 255, 0.3);
      border-radius: 999px;
    }

    .typing {
      border-right: 2px solid #ffd0f3;
    }

    .typing.done {
      border-right: none;
      animation: blinkCaret 0.9s step-end infinite;
    }

    @keyframes blinkCaret {
      0%,
      100% {
        border-color: transparent;
      }
      50% {
        border-color: #ffd0f3;
      }
    }

    .signature {
      margin-top: 16px;
      font-size: 12px;
      color: #ffdff7;
    }

    .signature span {
      font-weight: 600;
      color: #ff9dd4;
    }

    .bottom-row {
      margin-top: 14px;
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      align-items: center;
      justify-content: space-between;
      font-size: 11px;
      color: #e9caff;
    }

    .soft-btn {
      border: none;
      outline: none;
      cursor: pointer;
      border-radius: 999px;
      padding: 7px 13px;
      font-size: 11px;
      display: inline-flex;
      align-items: center;
      gap: 5px;
      background: rgba(255, 255, 255, 0.06);
      color: #ffeafc;
      transition: transform 0.15s ease, background 0.15s ease;
    }

    .soft-btn:hover {
      background: rgba(255, 255, 255, 0.12);
      transform: translateY(-1px);
    }

    .soft-btn:active {
      transform: scale(0.97);
    }
  </style>
</head>
<body>
  <!-- glowy background orbs -->
  <div class="glow-orb" style="top:-40px; left:-40px;"></div>
  <div class="glow-orb" style="bottom:-60px; right:-10px; background: radial-gradient(circle, rgba(180,172,255,0.7), transparent 70%);"></div>

  <!-- random floating hearts -->
  <script>
    for (let i = 0; i < 20; i++) {
      const h = document.createElement("div");
      h.className = "floating-heart";
      h.style.left = Math.random() * 100 + "vw";
      h.style.bottom = -10 - Math.random() * 30 + "vh";
      h.style.animationDelay = Math.random() * 8 + "s";
      h.style.animationDuration = 8 + Math.random() * 6 + "s";
      h.style.opacity = 0.25 + Math.random() * 0.4;
      document.body.appendChild(h);
    }
  </script>

  <div class="wrapper">
    <!-- Left panel: intro + notes -->
    <div>
      <div class="tag">
        <span class="tag-dot"></span>
        FOR SAUMYA • FROM RAM
      </div>
      <h1>Ek chotu sa website, sirf tumhare naam 🤍</h1>
      <p class="subtitle">
        Unexpectedly mile the, par jo bond bana, woh bilkul intentional tha — pure dil se.
      </p>

      <div class="chips">
        <div class="chip"><span>💌</span> Dil se likha letter</div>
        <div class="chip"><span>✨</span> Soft love vibes</div>
        <div class="chip"><span>🤍</span> Quiet but forever</div>
      </div>

      <p style="font-size: 12px; color:#f3d2ff; margin-bottom:8px;">
        Neeche wale cute notes pe click karo, har ek mein Ram ka alag emotion tumhare liye type hoke aayega.
      </p>

      <div class="notes-grid">
        <button class="note-button" data-note="1">
          <span>Note 1 • How it all started</span>
          <span class="small">Unexpectedly mile… unexpectedly close ho gaye.</span>
          <span class="badge">NEW</span>
        </button>
        <button class="note-button" data-note="2">
          <span>Note 2 • Distance & love</span>
          <span class="small">Doori aayi, par feelings clear hi rahi.</span>
          <span class="badge">✨</span>
        </button>
        <button class="note-button" data-note="3">
          <span>Note 3 • Sorry & truth</span>
          <span class="small">Agar kabhi hurt kiya ho, toh dil se sorry.</span>
          <span class="badge">🤍</span>
        </button>
        <button class="note-button" data-note="4">
          <span>Note 4 • Forever space</span>
          <span class="small">Bas ek request: strangers kabhi na banein.</span>
          <span class="badge">∞</span>
        </button>
      </div>

      <p class="hint">
        Tip: Agar kabhi mood off ho, bas kisi bhi note pe click karke padhna — Ram hamesha yahin rahega, quietly & respectfully. 
      </p>

      <div class="love-meter">
        Love level from Ram:
        <div class="meter-bar">
          <div class="meter-fill"></div>
        </div>
        100%
      </div>
    </div>

    <!-- Right panel: active letter -->
    <div>
      <div class="letter-card">
        <div class="letter-header">
          <p class="letter-to">
            To: <span>Saumya</span>
          </p>
          <span class="tiny-heart">💗</span>
        </div>

        <div class="note-title-pill" id="noteTitlePill">
          <span class="index">1</span>
          <small id="noteTitleText">How it all started</small>
        </div>

        <div class="letter-body typing" id="letterBody"></div>

        <p class="signature">
          Hamesha tumhara, <span>Ram (tumhara chotu Ram 🤍)</span>
        </p>
      </div>

      <div class="bottom-row">
        <button class="soft-btn" id="replayBtn">
          🔁 Phir se padhun?
        </button>
        <span id="statusText">
          Note 1 playing softly...
        </span>
      </div>
    </div>
  </div>

  <script>
    // Saare notes ka content (pure tera text split karke)
    const notes = {
      1: {
        title: "How it all started",
        text:
          "Unexpectedly hum mile,
" +
          "unexpectedly baatein hui,
" +
          "aur bina soche-samjhe ek gehra sa bond ban gaya.
" +
          "Kab attachment ho gayi, pata hi nahi chala.

" +
          "Meri life mein log zyada nahi hain jo truly matter karte hain.
" +
          "Family ke baad, tum unmein se ho.
" +
          "Isiliye tumse baat karna — chahe chhoti si ho —
" +
          "mere liye hamesha special raha hai."
      },
      2: {
        title: "Distance, respect & pyaar",
        text:
          "Life ne thoda distance la diya,
" +
          "par ek baat aaj bhi bilkul clear hai —
" +
          "main tumse bahut pyaar karta hoon, aur dil se karta hoon.

" +
          "Main tumhare decisions aur tumhari space ka poora respect karta hoon.
" +
          "Main kuch demand nahi kar raha,
" +
          "na hi tumhe force karna chahta hoon.

" +
          "Bas itni si baat hai —
" +
          "jab bhi hum baat karein,
" +
          "thodi si warmth aur care ho,
" +
          "wahi jo hum pehle feel karte the.

" +
          "Aur agar kabhi milna ho,
" +
          "toh woh meeting pyaar, samajh aur pure intentions ke saath ho."
      },
      3: {
        title: "Sorry, if I ever hurt you",
        text:
          "Agar kabhi tum busy ho ya space chahiye, main samajhta hoon.
" +
          "Bas jab possible ho, mujhe avoid ya ignore mat karna…
" +
          "kyunki sach kahun toh thoda sa hurt hota hai.
" +
          "Ek simple reply bhi mere liye kaafi hota hai.

" +
          "Agar past mein meri kisi baat se tum hurt hui ho,
" +
          "toh mujhe dil se maafi chahiye.
" +
          "Jo bhi emotions the, woh immaturity se nahi,
" +
          "sirf pyaar se aaye the.

" +
          "Kabhi-kabhi zyada care karna insaan ko vulnerable bana deta hai —
" +
          "bas wahi tha."
      },
      4: {
        title: "Forever, quietly & respectfully",
        text:
          "Main chahta hoon tum khush raho, grow karo, successful bano.
" +
          "Aur itna yaad rakhna —
" +
          "main hamesha tumhara hi rahunga, quietly aur respectfully.

" +
          "Main yeh nahi keh raha ki tum par koi pressure ho,
" +
          "bas dil se yahi chahta hoon ki
" +
          "tum bhi mujhe apna samjho, jaise main tumhe maanta hoon.

" +
          "Main tumse kuch nahi maangta.
" +
          "Bas yeh chahta hoon ki
" +
          "jo feelings humne kabhi share ki thi,
" +
          "woh tumhare dil mein hamesha zinda rahein.

" +
          "Aur chahe life humein jahan bhi le jaaye,
" +
          "hum kabhi ek-dusre ke liye strangers na banein.

" +
          "Hamesha apne chotu Ram ke liye
" +
          "thodi si jagah rakhna 🤍"
      }
    };

    const letterBody = document.getElementById("letterBody");
    const noteTitlePill = document.getElementById("noteTitlePill");
    const noteTitleText = document.getElementById("noteTitleText");
    const replayBtn = document.getElementById("replayBtn");
    const statusText = document.getElementById("statusText");
    const noteButtons = document.querySelectorAll(".note-button");

    let currentNote = 1;
    let typingInterval = null;
    let charIndex = 0;

    function setNoteTitleIndex(index) {
      noteTitlePill.querySelector(".index").textContent = index;
    }

    function typeNote(noteId) {
      clearInterval(typingInterval);
      letterBody.classList.remove("done");
      letterBody.textContent = "";

      const content = notes[noteId].text;
      charIndex = 0;

      typingInterval = setInterval(() => {
        if (charIndex < content.length) {
          letterBody.textContent += content.charAt(charIndex);
          charIndex++;
        } else {
          clearInterval(typingInterval);
          letterBody.classList.add("done");
          statusText.textContent = `Note ${noteId} finished — bas itna hi kehna tha.`;
        }
      }, 26); // typing speed
    }

    function setActiveNote(noteId) {
      currentNote = noteId;
      // Update title pill
      noteTitleText.textContent = notes[noteId].title;
      setNoteTitleIndex(noteId);
      statusText.textContent = `Note ${noteId} playing softly...`;

      // Visual active state on buttons
      noteButtons.forEach((btn) => {
        if (btn.getAttribute("data-note") === String(noteId)) {
          btn.style.filter = "brightness(1.05)";
        } else {
          btn.style.filter = "brightness(0.92)";
        }
      });

      typeNote(noteId);
    }

    // Attach click handlers to note buttons
    noteButtons.forEach((btn) => {
      btn.addEventListener("click", () => {
        const noteId = parseInt(btn.getAttribute("data-note"), 10);
        setActiveNote(noteId);
      });
    });

    // Replay current note
    replayBtn.addEventListener("click", () => {
      statusText.textContent = `Note ${currentNote} phir se start ho gaya.`;
      typeNote(currentNote);
    });

    // Start with first note
    setActiveNote(1);
  </script>
</body>
</html>
