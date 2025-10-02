My Zodiac Sign project
<!DOCTYPE html>
<html>
<head>
  <title>Zodiac Horoscope</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: linear-gradient(to right, #ffecd2, #fcb69f);
      padding: 50px;
    }
    .container {
      background: white;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0px 4px 10px rgba(0,0,0,0.2);
      width: 400px;
      margin: auto;
    }
    input, button {
      padding: 10px;
      margin: 10px;
      border-radius: 8px;
      border: 1px solid gray;
      width: 80%;
    }
    button {
      background-color: #f76b1c;
      color: white;
      font-weight: bold;
      cursor: pointer;
    }
    button:hover {
      background-color: #d85b17;
    }
    #result {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
      color: #333;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Zodiac & Horoscope</h1>
    <p>Enter your name:</p>
    <input type="text" id="nameInput" placeholder="Type your name">
    <br>
    <button onclick="showHoroscope()">Get Horoscope</button>
    <div id="result"></div>
  </div>

  <script>
    function showHoroscope() {
      let name = document.getElementById("nameInput").value.trim();
      if(name === ""){
        document.getElementById("result").innerHTML = "⚠️ Please enter a name.";
        return;
      }

      let firstLetter = name[0].toUpperCase();
      let zodiac = "";
      let horoscope = "";

      // Assign zodiac based on first letter
      if("A L E".includes(firstLetter)) {
        zodiac = "Aries ♈";
        horoscope = "Today is a great day to start something new!";
      } 
      else if("B V U".includes(firstLetter)) {
        zodiac = "Taurus ♉";
        horoscope = "Patience will bring you success today.";
      } 
      else if("K G Chh".includes(firstLetter)) {
        zodiac = "Gemini ♊";
        horoscope = "Your communication skills will shine.";
      } 
      else if("D H".includes(firstLetter)) {
        zodiac = "Cancer ♋";
        horoscope = "Spend some time with loved ones.";
      } 
      else if("M T".includes(firstLetter)) {
        zodiac = "Leo ♌";
        horoscope = "Confidence will open new opportunities.";
      } 
      else if("P  T".includes(firstLetter)) {
        zodiac = "Virgo ♍";
        horoscope = "Stay focused, and success will follow.";
      } 
      else if("R T".includes(firstLetter)) {
        zodiac = "Libra ♎";
        horoscope = "Balance is the key to your happiness today.";
      } 
      else if("N Y".includes(firstLetter)) {
        zodiac = "Scorpio ♏";
        horoscope = "Trust your intuition in making decisions.";
      } 
      else if("Bh Dh F".includes(firstLetter)) {
        zodiac = "Sagittarius ♐";
        horoscope = "Adventure is calling, embrace it!";
      } 
      else if("Kh J".includes(firstLetter)) {
        zodiac = "Capricorn ♑";
        horoscope = "Hard work will bring great rewards soon.";
      } 
      else {
        zodiac = "Unknown";
        horoscope = "No horoscope available.";
      }

      document.getElementById("result").innerHTML = 
        "🔮 Zodiac Sign: <b>" + zodiac + "</b><br>✨ Horoscope: " + horoscope;
    }
  </script>
</body>
</html>
