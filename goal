<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Story Polisher & Voice Challenge App</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #f9f9ff, #eef1ff);
      text-align: center;
      padding: 20px;
    }
    h1 {
      color: #5b3eff;
      text-shadow: 1px 1px #ccc;
    }
    textarea {
      width: 90%;
      height: 200px;
      margin-top: 10px;
      border: 2px solid #d0d0ff;
      border-radius: 12px;
      padding: 10px;
      font-size: 16px;
      resize: none;
      background: #fff;
    }
    button {
      margin: 10px 5px;
      padding: 10px 20px;
      border: none;
      border-radius: 10px;
      background: #5b3eff;
      color: white;
      font-size: 16px;
      cursor: pointer;
      transition: 0.2s;
    }
    button:hover {
      background: #3e28cc;
      transform: scale(1.05);
    }
    #output {
      width: 90%;
      margin: 20px auto;
      background: #fff;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 0 10px #ccc;
      text-align: left;
    }
  </style>
</head>
<body>
  <h1>🎙 Story Polisher + Writing Challenge 🌈</h1>

  <textarea id="storyInput" placeholder="Type or speak your story here..."></textarea><br>

  <button onclick="startVoiceInput()">🎤 Speak Story</button>
  <button onclick="polishStory()">🪄 Polish</button>
  <button onclick="gradeStory()">📊 Grade</button>
  <button onclick="challengeOfTheDay()">🌈 Daily Challenge</button>
  <button onclick="explainGrade()">💬 Explain Grade</button>
  <button onclick="compareMode()">🪞 Before/After</button>

  <div id="output"></div>

  <script>
    let originalStory = "";
    let polishedStory = "";
    let lastGrade = "";

    // 🎙 Voice-to-Story Feature
    function startVoiceInput() {
      if (!('webkitSpeechRecognition' in window)) {
        alert("Voice input not supported on this browser.");
        return;
      }
      const recognition = new webkitSpeechRecognition();
      recognition.continuous = false;
      recognition.interimResults = false;
      recognition.lang = "en-US";

      document.getElementById('output').innerHTML = "<p>🎤 Listening... tell me your story!</p>";
      recognition.start();

      recognition.onresult = function(event) {
        const transcript = event.results[0][0].transcript;
        document.getElementById('storyInput').value = transcript;
        document.getElementById('output').innerHTML = `<p>📝 Transcribed story:</p><p>${transcript}</p>`;
      };

      recognition.onerror = function(e) {
        document.getElementById('output').innerHTML = `<p>⚠️ Error: ${e.error}</p>`;
      };
    }

    // 🪄 Simple polish feature
    function polishStory() {
      const story = document.getElementById('storyInput').value;
      if (!story.trim()) return alert("Write something first!");
      originalStory = story;
      polishedStory = story
        .replace(/\bvery\b/g, "extremely")
        .replace(/\bsaid\b/g, "remarked")
        .replace(/\bmad\b/g, "furious");
      document.getElementById('output').innerHTML = `<h3>Polished Story:</h3><p>${polishedStory}</p>`;
    }

    // 📊 Fake grading system
    function gradeStory() {
      const story = document.getElementById('storyInput').value;
      if (!story.trim()) return alert("Write something first!");
      const scor

