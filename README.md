<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Countdown Timers</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f0f0f0;
      color: #333;
    }
    .container {
      margin: 20px auto;
      padding: 20px;
      background: #fff;
      border-radius: 8px;
      width: 80%;
      max-width: 400px;
    }
    .header {
      font-size: 1.5em;
      color: #FF0000;
      margin-bottom: 10px;
    }
    .countdown {
      font-size: 1.2em;
      font-weight: bold;
    }
  </style>
</head>
<body>

<div class="container">
  <div class="header">Christmas Countdown</div>
  <div class="countdown" id="christmasCountdown">Loading...</div>
</div>

<div class="container">
  <div class="header">Countdown to The Bers</div>
  <div class="countdown" id="bersCountdown">Loading...</div>
</div>

<script>
  function updateChristmasCountdown() {
    const now = new Date();
    const nextChristmas = new Date(now.getFullYear(), 11, 25); // December 25th
    if (now > nextChristmas) {
      nextChristmas.setFullYear(nextChristmas.getFullYear() + 1);
    }
    const timeRemaining = nextChristmas - now;
    const days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));
    document.getElementById('christmasCountdown').innerText = `${days} days until Christmas`;
  }

  function updateBersCountdown() {
    const now = new Date();
    const nextBers = new Date(now.getFullYear(), 8, 1); // September 1st
    if (now > nextBers) {
      nextBers.setFullYear(nextBers.getFullYear() + 1);
    }
    const timeRem
