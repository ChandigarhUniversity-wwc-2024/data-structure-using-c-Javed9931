<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cultural Experience Finder</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f9f9f9;
    }

    header {
      background-color: #673AB7;
      color: white;
      padding: 15px 0;
      text-align: center;
    }

    .container {
      padding: 20px;
      max-width: 800px;
      margin: auto;
      background: white;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    h2 {
      color: #333;
    }

    input[type="text"] {
      width: calc(100% - 22px);
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      background-color: #673AB7;
      color: white;
      border: none;
      padding: 10px 20px;
      margin: 5px 0;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background-color: #5E35B1;
    }

    .results {
      margin-top: 20px;
    }

    .result-card {
      background: #f4f4f9;
      padding: 15px;
      margin-bottom: 10px;
      border-left: 4px solid #673AB7;
    }

    .result-card h3 {
      margin: 0;
    }

    .result-card p {
      margin: 5px 0 0;
    }
  </style>
</head>
<body>

<header>
  <h1>Cultural Experience Finder</h1>
</header>

<div class="container">
  <h2>Find Cultural Experiences</h2>
  <p>Enter a location to explore cultural experiences:</p>
  <input type="text" id="locationInput" placeholder="Enter a location">
  <button onclick="findExperiences()">Search</button>

  <div id="results" class="results"></div>
</div>

<script>
  const culturalExperiences = {
    "New York": [
      { name: "Metropolitan Museum of Art", description: "Explore one of the world's largest art museums." },
      { name: "Broadway Shows", description: "Experience the magic of live theater in Times Square." },
      { name: "Chinatown", description: "Immerse yourself in Chinese culture and cuisine." }
    ],
    "Tokyo": [
      { name: "Sensoji Temple", description: "Visit Tokyo's oldest Buddhist temple in Asakusa." },
      { name: "Tsukiji Outer Market", description: "Indulge in fresh sushi and local delicacies." },
      { name: "Harajuku", description: "Discover unique fashion and Japanese pop culture." }
    ],
    "Paris": [
      { name: "Eiffel Tower", description: "Admire the iconic symbol of France." },
      { name: "Louvre Museum", description: "Explore the world's largest art museum and a historic monument." },
      { name: "Montmartre", description: "Walk through the historic district known for its artistic heritage." }
    ],
    "Mumbai": [
      { name: "Gateway of India", description: "Visit the iconic arch-monument overlooking the Arabian Sea." },
      { name: "Elephanta Caves", description: "Explore ancient rock-cut caves with stunning sculptures." },
      { name: "Chowpatty Beach", description: "Experience local street food and the vibrant coastal life." }
    ]
  };

  function findExperiences() {
    const location = document.getElementById("locationInput").value.trim();
    const resultsContainer = document.getElementById("results");
    resultsContainer.innerHTML = ""; // Clear previous results

    if (!location) {
      resultsContainer.innerHTML = "<p>Please enter a location to search.</p>";
      return;
    }

    const experiences = culturalExperiences[location];

    if (experiences) {
      experiences.forEach(exp => {
        const card = document.createElement("div");
        card.className = "result-card";

        const title = document.createElement("h3");
        title.textContent = exp.name;

        const description = document.createElement("p");
        description.textContent = exp.description;

        card.appendChild(title);
        card.appendChild(description);
        resultsContainer.appendChild(card);
      });
    } else {
      resultsContainer.innerHTML = <p>No cultural experiences found for "${location}". Try another location!</p>;
    }
  }
</script>

</body>
</html>
