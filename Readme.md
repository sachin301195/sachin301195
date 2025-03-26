<!DOCTYPE html>
<html>
<head>
  <style>
    body { background: #1a1a1a; color: #00ff00; font-family: monospace; }
    .dashboard { display: flex; flex-wrap: wrap; gap: 20px; }
    .component { border: 1px solid #00ff00; padding: 10px; width: 200px; }
    .component:hover { background: #003300; }
    .pulse { animation: pulse 1s infinite; }
    @keyframes pulse { 0% { opacity: 1; } 50% { opacity: 0.5; } 100% { opacity: 1; } }
    .footer { position: fixed; bottom: 10px; }
  </style>
</head>
<body>
  <h1>Sachin Bulchandani’s E-Commerce Control Room</h1>
  <div class="dashboard">
    <div class="component">
      <h3>Current Mission</h3>
      <p class="pulse">Energy Consumption Predictor</p>
      <a href="https://github.com/sachin301195/Energy_Consumption_Predictor" target="_blank">View on GitHub</a>
    </div>
    <div class="component" onclick="scalePods()">
      <h3>EKS</h3>
      <p id="pods">Pods: 3</p>
    </div>
    <div class="component">
      <h3>System Specs</h3>
      <p>Powered by: Python, AWS, Docker</p>
    </div>
  </div>
  <div class="footer">
    <a href="https://github.com/sachin301195" target="_blank">GitHub</a> |
    <a href="https://www.kaggle.com/sachinbulchandani" target="_blank">Kaggle</a> |
    <a href="https://drive.google.com/file/d/1AQU8PHeIdrXch60T0uTX0SW7Z/view?usp=sharing" target="_blank">Resume</a>
  </div>

  <script>
    function scalePods() {
      let pods = document.getElementById('pods');
      pods.innerText = 'Pods: Scaling...';
      setTimeout(() => pods.innerText = 'Pods: 5', 1000);
    }
  </script>
</body>
</html>
