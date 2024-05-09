<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Moving Directions Website</title>
    <style>
        /* Стилі для навігаційного меню */
        nav {
            background-color: #1E1E1E;
            overflow: hidden;
        }
        nav ul {
            list-style-type: none;
            margin: 0;
            padding: 0;
            overflow: hidden;
        }
        nav ul li {
            float: left;
            margin-right: 20px;
        }
        nav ul li a {
            display: block;
            color: #FFFFFF;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
            font-size: 16px;
            font-weight: bold;
        }
        nav ul li a:hover {
            background-color: #FFFFFF;
            color: #1E1E1E;
            border-radius: 5px;
        }
        /* Стилі для основного контенту */
        .content {
            padding: 20px;
            text-align: center;
            color: #1E1E1E;
            font-family: Arial, sans-serif;
        }
        /* Стилі для підвалу */
        footer {
            background-color: #1E1E1E;
            color: #FFFFFF;
            padding: 10px;
            text-align: center;
            position: fixed;
            bottom: 0;
            width: 100%;
            font-size: 14px;
        }
        h1 {
            color: #1E1E1E;
        }
    </style>
</head>
<body>
    <nav>
        <ul>
            <li><a href="index(1).html">Головна</a></li>
            <!-- Показувати посилання на реєстрацію та вхід тільки якщо користувач не авторизований -->
            {% if not session.logged_in %}
            <li><a href="index(3).html">Регестрація</a></li>
            <li><a href="index(2).html">Вхід</a></li>
            {% endif %}
            <!-- Показувати посилання на вихід тільки якщо користувач авторизований -->
            {% if session.logged_in %}
            <li><a href="index(4).html">Стоврити напрямок</a></li>
            {% endif %}
            <!-- Додайте інші посилання на ваш вміст тут -->
        </ul>
    </nav>

    <div class="content">
        <!-- Показувати інформацію про користувача, якщо він авторизований -->
        
        <h2>Welcome</h2>
        <p>You are logged in as</p>
        <h1>Welcome to Your Moving Directions Website</h1>
        <p>This is a place where you can generate directions for your move.</p>
        <!-- Додайте інший контент вашого сайту тут -->
    </div>

    <footer>
        <p>&copy; 2024 Your Moving Directions Website</p>
    </footer>
</body>
</html>
