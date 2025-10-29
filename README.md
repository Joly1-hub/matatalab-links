links = {
    "Matatalab Curriculum": [
        ("Matatalab Curriculum", "https://matatalab.com/en/curriculum"),
        ("Matatalab Activity", "https://matatalab.com/en/activity"),
        ("Matatalab Play (Scratch)", "http://play.matatalab.com/"),
        ("Matatalab Drawing Mode (Scratch)",
         "http://play.matatalab.com/drawing-mode.html"),
        ("Matatalab Scratch Games",
         "https://scratch.mit.edu/search/projects?q=matatalab"),
        ("Matatalab Challenge Mode (Scratch Game)",
         "https://scratch.mit.edu/projects/381555862/"),
        ("Scratch Matatalab Bluetooth", "https://create.matatalab.com/")
    ],
    "Matatalab Letters": [
        ("Matatalab Letters (PDF)",
         "https://meelespealasteaiameeskond.wordpress.com/wp-content/uploads/2023/02/joonista-tahti.pdf"),
        ("Matatalab Arabic Numbers", "https://matatalab.com/en/node/87"),
        ("Matatalab Arabic Numbers (PDF)",
         "https://matatalab.com/cdn/ff/WkDD806gF3cab_tQRg4XiV92L0HN-_JJyzsm2uQu98o/1595477728/public/2020-07/Draw%20numbers%20Samples.pdf")
    ],
    "Matatalab Cozy Home": [
        ("Matatalab Cozy Home", "https://matatalab.com/en/node/85"),
        ("Matatalab Cozy Home (PDF)",
         "https://matatalab.com/cdn/ff/gJUTM9Zpsh3aJV036ZTuizoutYeUFwU0zUMjk1YxV9s/1595476784/public/2020-07/House%20Samples.pdf")
    ]
}

html = """
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <title>Matatalab Links</title>
  <style>
    body {
      font-family: 'Segoe UI', Roboto, sans-serif;
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #a5f3fc, #93c5fd, #c4b5fd, #f9a8d4);
      background-size: 300% 300%;
      animation: gradient 10s ease infinite;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      text-align: center;
      padding-top: 50px;
    }
    @keyframes gradient {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }
    h1 {
      color: #1e3a8a;
      font-size: 64px;
      margin-bottom: 40px;
      text-shadow: 2px 2px 10px rgba(0,0,0,0.2);
    }
    h2 {
      color: #1e40af;
      font-size: 38px;
      margin-top: 40px;
      margin-bottom: 10px;
      text-shadow: 1px 1px 6px rgba(0,0,0,0.1);
    }
    a {
      display: block;
      margin: 10px 0;
      text-decoration: none;
      color: #1d4ed8;
      font-size: 26px;
      transition: all 0.3s ease;
      font-weight: 500;
    }
    a:hover {
      color: #f97316;
      transform: scale(1.1);
      text-shadow: 1px 1px 6px rgba(0,0,0,0.2);
    }
    .section {
      background: rgba(255, 255, 255, 0.6);
      border-radius: 20px;
      padding: 25px 40px;
      margin: 20px 0;
      box-shadow: 0 10px 20px rgba(0,0,0,0.15);
      width: 80%;
      max-width: 800px;
    }
  </style>
</head>
<body>
  <h1>Matatalab Links</h1>
"""

for section, items in links.items():
    html += f'<div class="section">\n<h2>{section}</h2>\n'
    for title, url in items:
        html += f'  <a href="{url}" target="_blank" rel="noopener">{title}</a>\n'
    html += '</div>\n'

html += """
</body>
</html>
"""

with open("matatalab_links.html", "w", encoding="utf-8") as f:
    f.write(html)

print("✅ matatalab_links.html created successfully — centered and colorful!")
