<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lydia's Birthday Lunch Menu</title>
    <style>
        /* Reset styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f0f4f8;
            color: #333;
            overflow: hidden; /* Prevent scrolling during intro */
        }

        /* Intro Section */
        #intro {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRF8eT7-fk6BpnYr8plJzCFRGW0AuMcZOGzbA&s') center/cover no-repeat; /* Edit image link */
            color: #fff;
            text-align: center;
            animation: fadeOut 1.5s ease-in-out 3s forwards;
        }

        #intro h1 {
            font-size: 3.5rem;
            animation: fadeInZoom 2s ease-in-out;
            background: rgba(0, 0, 0, 0.5);
            padding: 10px 20px;
            border-radius: 10px;
        }

        /* Main Content */
        #content {
            display: none;
            animation: fadeInContent 1.5s ease-in-out 3s forwards;
        }

        header {
            background-color: #ffcc80;
            text-align: center;
            padding: 40px 20px;
        }

        header h1 {
            font-size: 3rem;
            margin-bottom: 10px;
        }

        header p {
            font-size: 1.2rem;
            color: #555;
        }

        .menu-section {
            max-width: 800px;
            margin: 20px auto;
            background-color: #fff;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        .menu-section h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
        }

        .menu-section h2::after {
            content: '';
            width: 50px;
            height: 3px;
            background-color: #ffab40;
            position: absolute;
            left: 0;
            bottom: -5px;
            border-radius: 2px;
        }

        ul {
            list-style-type: none;
        }

        li {
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            transition: transform 0.3s ease;
        }

        li img {
            width: 80px;
            height: 80px;
            object-fit: cover;
            border-radius: 10px;
            margin-right: 15px;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
        }

        li img:hover {
            transform: scale(1.1);
        }

        li span {
            font-size: 1.2rem;
        }

        /* Fullscreen Popup for Images */
        .popup {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .popup img {
            max-width: 80%;
            max-height: 80%;
            border-radius: 10px;
        }

        .popup:target {
            display: flex;
        }

        .popup .close {
            position: absolute;
            top: 10px;
            right: 10px;
            font-size: 2rem;
            color: #fff;
            cursor: pointer;
        }

        /* Animations */
        @keyframes fadeInZoom {
            from {
                opacity: 0;
                transform: scale(0.5);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        @keyframes fadeOut {
            to {
                opacity: 0;
                visibility: hidden;
            }
        }

        @keyframes fadeInContent {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        /* Responsive Design */
        @media (max-width: 600px) {
            header h1 {
                font-size: 2.5rem;
            }

            li {
                flex-direction: column;
                align-items: flex-start;
            }

            li img {
                margin-bottom: 10px;
            }
        }
    </style>
</head>
<body>

    <!-- Intro Section -->
    <div id="intro">
        <h1>Lydia's Birthday Lunch Menu</h1>
    </div>

    <!-- Main Content -->
    <div id="content">
        <header>
            <h1>Welcome to Our Lunch Party</h1>
            <p>Delicious dishes prepared with love</p>
        </header>

        <div class="menu-section">
            <h2>Main Courses</h2>
            <ul>
                <!-- Editable Dish 1 -->
                <li>
                    <a href="#popup1"><img src="https://upload.wikimedia.org/wikipedia/commons/d/d5/Souvla.jpg" alt="Regas' Souvla"></a>
                    <span>Regas' Souvla</span>
                </li>
                <!-- Editable Dish 2 -->
                <li>
                    <a href="#popup2"><img src="https://30minutesmeals.com/wp-content/uploads/2019/11/Ham-and-Cheese-Pasta-1.jpg" alt="Pasta with Cheese and Ham"></a>
                    <span>Pasta with Cheese and Ham</span>
                </li>
                <!-- Editable Dish 3 -->
                <li>
                    <a href="#popup3"><img src="file:///C:/Users/oneop/Downloads/download.jpg" alt="Oven Potatoes"></a>
                    <span>Oven Potatoes</span>
                </li>
                <!-- Editable Dish 4 (Salad) -->
                <li>
                    <a href="#popup4"><img src="file:///C:/Users/oneop/Downloads/download%20(1).jpg" alt="Salad"></a>
                    <span>Salad</span>
                </li>
            </ul>
        </div>
    </div>

    <!-- Popup Sections -->
    <div id="popup1" class="popup">
        <span class="close" onclick="window.location='#'">&times;</span>
        <img src="https://upload.wikimedia.org/wikipedia/commons/d/d5/Souvla.jpg" alt="Regas' Souvla">
    </div>
    <div id="popup2" class="popup">
        <span class="close" onclick="window.location='#'">&times;</span>
        <img src="https://30minutesmeals.com/wp-content/uploads/2019/11/Ham-and-Cheese-Pasta-1.jpg" alt="Pasta with Cheese and Ham">
    </div>
    <div id="popup3" class="popup">
        <span class="close" onclick="window.location='#'">&times;</span>
        <img src="file:///C:/Users/oneop/Downloads/download.jpg" alt="Oven Potatoes">
    </div>
    <div id="popup4" class="popup">
        <span class="close" onclick="window.location='#'">&times;</span>
        <img src="file:///C:/Users/oneop/Downloads/download%20(1).jpg" alt="Salad">
    </div>

    <script>
        // Ensure the page starts at the top
        setTimeout(() => {
            document.getElementById('content').style.display = 'block';
            document.body.style.overflow = 'auto';
        }, 3000);
    </script>

</body>
</html>

