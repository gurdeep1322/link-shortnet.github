<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="NeonShorty is the ultimate URL shortener. Instantly shorten long links with style, improve SEO, and increase traffic. Free and simple to use." />
  <meta name="keywords" content="URL shortener, free link shortener, SEO tools, neon style link shortener, shorten URL online, free link tool, fast URL shortener, simple link shortener, ad-supported link shortener, traffic booster" />
  <meta name="author" content="NeonShorty Team" />
  <title>NeonShorty - Ultimate SEO Link Shortener</title>
  <style>
    body {
      background-color: #000;
      color: #fff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      text-align: center;
      padding: 40px;
      margin: 0;
    }
    .container {
      max-width: 700px;
      margin: auto;
      border: 4px solid #0ff;
      padding: 40px;
      border-radius: 25px;
      box-shadow: 0 0 25px #0ff;
      background-color: #111;
    }
    h1 {
      font-size: 2.8em;
      color: #0ff;
      text-shadow: 0 0 15px #0ff;
    }
    p, label {
      font-size: 1.1em;
    }
    input[type="url"] {
      width: 85%;
      padding: 12px;
      margin: 20px 0;
      border: none;
      border-radius: 10px;
      font-size: 1em;
      outline: none;
    }
    button {
      background-color: #0ff;
      border: none;
      padding: 12px 30px;
      font-size: 1em;
      color: #000;
      border-radius: 10px;
      cursor: pointer;
      box-shadow: 0 0 12px #0ff;
      transition: transform 0.2s;
    }
    button:hover {
      transform: scale(1.05);
    }
    .short-url {
      margin-top: 20px;
      font-weight: bold;
      color: #0f0;
      text-shadow: 0 0 5px #0f0;
    }
    .ad-section {
      margin-top: 30px;
      padding: 20px;
      background-color: #222;
      border: 2px dashed #f0f;
      border-radius: 12px;
      color: #f0f;
    }
    .reviews {
      margin-top: 40px;
      padding: 20px;
      background-color: #101010;
      border-radius: 15px;
      border: 1px solid #0ff;
      box-shadow: 0 0 10px #0ff;
    }
    .review {
      margin: 10px 0;
      font-style: italic;
      color: #ccc;
    }
    .review span {
      color: #0ff;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>NeonShorty</h1>
    <p>Paste your long URL below to shorten it and boost your SEO presence:</p>
    <input type="url" id="longUrl" placeholder="Enter your long URL here...">
    <br>
    <button onclick="shortenUrl()">Shorten</button>
    <div id="result" class="short-url"></div>

    <div class="ad-section">
      <p><strong>Ad:</strong> Drive traffic like a pro! Use our advanced SEO dashboard. <a href="#" style="color:#0ff">Try it free</a></p>
    </div>

    <div class="reviews">
      <h3>User Reviews:</h3>
      <div class="review"><span>@ritik_dev:</span> "Simple and elegant. Love the neon UI! 🔥"</div>
      <div class="review"><span>@eco_trends:</span> "Boosted my blog's SEO in just days! Highly recommended."</div>
      <div class="review"><span>@techgalaxy:</span> "Finally, a stylish shortener that actually works!"</div>
    </div>
  </div>

  <script>
    function shortenUrl() {
      const input = document.getElementById('longUrl');
      const result = document.getElementById('result');
      const longUrl = input.value.trim();

      if (!longUrl) {
        result.textContent = 'Please enter a valid URL.';
        return;
      }

      const shortUrl = 'https://neon.ly/' + btoa(longUrl).slice(0, 6);
      result.innerHTML = `Shortened URL: <a href="${longUrl}" target="_blank" style="color:#0ff">${shortUrl}</a>`;
    }
  </script>
</body>
</html>
