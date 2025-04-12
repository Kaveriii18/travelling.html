<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Travel Planner</title>
    <style>
        .form-control {
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <h1>TRAVEL PLANNER</h1>

    <div class="form-control">
        <label for="name">Enter your name:</label>
        <input type="text" id="name">
    </div>

    <div class="form-control">
        <label for="phone">Enter your phone number:</label>
        <input type="text" id="phone">
    </div>

    <div class="form-control">
        <label for="date">Enter your date:</label>
        <input type="date" id="date">
    </div>

    <div class="form-control">
        <label for="time">Enter your time:</label>
        <input type="time" id="time">
    </div>

    <div class="form-control">
        <label for="food">Food preference:</label>
        <input type="checkbox" id="food"> Veg Only
    </div>

    <div class="form-control">
        <label for="city">Enter your city:</label>
        <input type="text" id="city">
    </div>

    <div class="form-control">
        <button onclick="openTourism()">Show Tourism Places</button>
    </div>

    <script>
        function openTourism() {
            const city = document.getElementById("city").value;
            if(city) {
                // open Google search for tourism places in that city
                window.open(`https://www.google.com/search?q=best+tourist+places+in+${encodeURIComponent(city)}`, '_blank');
            } else {
                alert("Please enter a city first.");
            }
        }
    </script>
</body>
</html>
