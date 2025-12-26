<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Para Ti ❤️</title>

<style>
    body {
        margin: 0;
        height: 100vh;
        background: radial-gradient(circle at bottom, #050510, #000);
        overflow: hidden;
        font-family: Arial, sans-serif;
        color: white;
    }

    /* Estrellas */
    body::before {
        content: "";
        position: absolute;
        width: 100%;
        height: 100%;
        background-image: 
            radial-gradient(1px 1px at 20% 30%, white, transparent),
            radial-gradient(1px 1px at 70% 80%, white, transparent),
            radial-gradient(2px 2px at 40% 60%, white, transparent),
            radial-gradient(1px 1px at 90% 20%, white, transparent);
        animation: stars 20s linear infinite;
    }

    @keyframes stars {
        from { transform: translateY(0); }
        to { transform: translateY(-200px); }
    }

    .container {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
    }

    h1 {
        font-size: 2em;
        margin-bottom: 40px;
        animation: glow 2s infinite alternate;
    }

    @keyframes glow {
        from { text-shadow: 0 0 10px pink; }
        to { text-shadow: 0 0 25px red; }
    }

    /* Corazón */
    .heart {
        width: 80px;
        height: 80px;
        background: red;
        position: relative;
        transform: rotate(-45deg);
        margin: auto;
        animation: pulse 1.5s infinite;
    }

    .heart::before,
    .heart::after {
        content: "";
        width: 80px;
        height: 80px;
        background: red;
        border-radius: 50%;
        position: absolute;
    }

    .heart::before {
        top: -40px;
        left: 0;
    }

    .heart::after {
        left: 40px;
        top: 0;
    }

    @keyframes pulse {
        0% { transform: scale(1) rotate(-45deg); }
        50% { transform: scale(1.2) rotate(-45deg); }
        100% { transform: scale(1) rotate(-45deg); }
    }

    /* Órbitas */
    .orbit {
        position: absolute;
        width: 220px;
        height: 220px;
        border: 1px solid rgba(255, 100, 100, 0.5);
        border-radius: 50%;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        animation: spin 8s linear infinite;
    }

    .orbit::after {
        content: "";
        width: 10px;
        height: 10px;
        background: pink;
        border-radius: 50%;
        position: absolute;
        top: 0;
        left: 50%;
    }

    @keyframes spin {
        from { transform: translate(-50%, -50%) rotate(0deg); }
        to { transform: translate(-50%, -50%) rotate(360deg); }
    }
</style>
</head>

<body>
    <div class="container">
        <h1>Te quiero con todo mi corazón ✨</h1>
        <div class="heart"></div>
    </div>

    <div class="orbit"></div>
</body>
</html>
