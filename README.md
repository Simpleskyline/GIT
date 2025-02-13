<html>
<head>
  <title>Gestalt Principles</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background-color: #f0f0f5;
    }
    h1 {
      text-align: center;
    }
    .principle-card {
      border: 2px solid #ccc;
      border-radius: 10px;
      box-shadow: 2px 2px 10px rgba(0,0,0,0.1);
      margin: 20px;
      padding: 20px;
      background-color: #fff;
      transition: transform 0.3s;
    }
    .example {
      height: 100px;
      background-color: #d9e6f2;
      margin-top: 10px;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 20px;
    }
  </style>
</head>
<body>
  <h1>Gestalt Principles of Design</h1>
  <div class="grid" id="principles-container"></div>

  <script>
    const principles = [
      { name: 'Proximity', description: 'Objects that are close together are perceived as a group.' },
      { name: 'Similarity', description: 'Objects that are similar are perceived as related.' },
      { name: 'Closure', description: 'The mind completes incomplete shapes.' },
      { name: 'Continuity', description: 'The eye follows lines and curves naturally.' },
      { name: 'Figure-Ground', description: 'Objects stand out from their background.' },
      { name: 'Common Fate', description: 'Objects moving in the same direction are seen as a group.' }
    ];

    const container = document.getElementById('principles-container');

    principles.forEach(principle => {
      const card = document.createElement('div');
      card.className = 'principle-card';
      card.innerHTML = `
        <h2>${principle.name}</h2>
        <p>${principle.description}</p>
        <div class="example">Example visualization here</div>
      `;
      container.appendChild(card);
    });
  </script>
</body>
</html>
