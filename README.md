<!DOCTYPE html>
<html>
<head>
  <title>Ruletka</title>
  <style>
    body {
      background-color: black;
    }

    #roulette-wheel {
      width: 500px;
      height: 500px;
      margin: 0 auto;
      position: relative;
    }

    #roulette-ball {
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background-color: white;
      position: absolute;
      top: 250px;
      left: 250px;
    }

    #roulette-table {
      width: 500px;
      height: 100px;
      margin: 0 auto;
      position: relative;
    }

    #roulette-table td {
      width: 25px;
      height: 25px;
      border: 1px solid black;
      text-align: center;
    }

    #roulette-table tr:nth-child(1) td {
      background-color: red;
    }

    #roulette-table tr:nth-child(2) td {
      background-color: black;
    }

    #roulette-table tr:nth-child(3) td {
      background-color: green;
    }
  </style>
</head>
<body>
  <div id="roulette-wheel">
    <div id="roulette-ball"></div>
  </div>

  <div id="roulette-table">
    <table>
      <tr>
        <td>1</td>
        <td>3</td>
        <td>5</td>
        <td>7</td>
        <td>9</td>
        <td>12</td>
        <td>14</td>
        <td>16</td>
        <td>18</td>
        <td>19</td>
        <td>21</td>
        <td>23</td>
        <td>25</td>
        <td>27</td>
        <td>30</td>
        <td>32</td>
        <td>34</td>
        <td>36</td>
      </tr>
      <tr>
        <td>2</td>
        <td>4</td>
        <td>6</td>
        <td>8</td>
        <td>10</td>
        <td>11</td>
        <td>13</td>
        <td>15</td>
        <td>17</td>
        <td>20</td>
        <td>22</td>
        <td>24</td>
        <td>26</td>
        <td>28</td>
        <td>29</td>
        <td>31</td>
        <td>33</td>
        <td>35</td>
      </tr>
      <tr>
        <td colspan="18">0</td>
      </tr>
    </table>
  </div>

  <script>
    // Pobierz element koła ruletki
    const rouletteWheel = document.getElementById('roulette-wheel');

    // Pobierz element piłki ruletki
    const rouletteBall = document.getElementById('roulette-ball');

    // Pobierz element stołu ruletki
    const rouletteTable = document.getElementById('roulette-table');

    // Utwórz nową instancję obiektu Wheel
    const wheel = new Wheel(rouletteWheel, rouletteBall, rouletteTable);

    // Dodaj zdarzenie nasłuchujące zdarzenia click do koła ruletki
    rouletteWheel.addEventListener('click', () => {

      // Rozpocznij obracanie koła ruletki
      wheel.spin();

    });
  </script>
</body>
</html>
