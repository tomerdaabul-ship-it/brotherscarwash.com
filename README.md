<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <title>האחים מכונית בע"מ 🚗💦🧽</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: url('background.jpg') center/cover fixed no-repeat;
      background-color: #e8f2ff;
      color: #222;
    }

    header {
      position: relative;
      padding: 60px 20px;
      text-align: center;
      color: white;
    }

    header::before {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(10, 80, 160, 0.7);
    }

    header * {
      position: relative;
      z-index: 1;
    }

    .team-note {
      position: absolute;
      left: 20px;
      top: 20px;
      font-weight: bold;
    }

    section {
      background: white;
      max-width: 900px;
      margin: 20px auto;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    h2 {
      color: #0a74da;
    }

    ul {
      line-height: 1.8;
    }

    button {
      background: #0a74da;
      color: white;
      border: none;
      padding: 12px;
      width: 100%;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background: #085bb0;
    }

    input, select, textarea {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      border-radius: 6px;
      border: 1px solid #ccc;
      box-sizing: border-box;
    }

    footer {
      text-align: center;
      padding: 15px;
      color: #666;
    }

    .rating-box {
      position: fixed;
      right: 20px;
      top: 140px;
      width: 230px;
      background: #ffffffee;
      border-radius: 12px;
      padding: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      z-index: 999;
    }

    .rating-box h3 {
      text-align: center;
      color: #0a74da;
      margin-top: 0;
    }

    .stars {
      text-align: center;
      font-size: 22px;
      cursor: pointer;
      user-select: none;
    }

    .stars span {
      filter: grayscale(100%);
      margin: 0 1px;
    }

    .stars span.active {
      filter: grayscale(0%);
    }

    .review {
      border-bottom: 1px solid #eee;
      padding: 10px 0;
    }

    .stars-view {
      color: gold;
      margin: 4px 0;
    }

    .rating-box + .rating-box {
      margin-top: 10px;
    }

    @media (max-width: 980px) {
      .rating-box {
        position: static;
        width: auto;
        max-width: 900px;
        margin: 10px auto;
      }
    }
  </style>
</
