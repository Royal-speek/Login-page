<!DOCTYPE html>  <html lang="ar">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>تسجيل الدخول</title>  
    <style>  
        body {  
            font-family: Arial, sans-serif;  
            display: flex;  
            justify-content: center;  
            align-items: center;  
            height: 100vh;  
            background-color: #f5f5f5;  
        }  
        .login-container {  
            background: white;  
            padding: 20px;  
            border-radius: 8px;  
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);  
            text-align: center;  
        }  
        input {  
            width: 100%;  
            padding: 10px;  
            margin: 10px 0;  
            border: 1px solid #ccc;  
            border-radius: 5px;  
        }  
        button {  
            background-color: #4285F4;  
            color: white;  
            border: none;  
            padding: 10px;  
            border-radius: 5px;  
            cursor: pointer;  
            width: 100%;  
        }  
        img {  
            width: 100px;  
            display: block;  
            margin: 0 auto 10px;  
        }  
    </style>  
</head>  
<body>  
    <div class="login-container">  
        <img src="https://upload.wikimedia.org/wikipedia/commons/2/2f/Google_2015_logo.svg" alt="Google Logo">  
        <h3>تسجيل الدخول</h3>  
        <h2>Googleباستخدام حسابك على </h2>  
        <input type="email" id="email" placeholder="البريد الإلكتروني" oninput="validateEmail()">  
        <input type="password" id="password" placeholder="كلمة المرور">  
        <button onclick="login()">تسجيل الدخول</button>  
        <p id="message" style="color: green; display: none;">تم تسجيل دخولك بنجاح!</p>  
        <p id="email-error" style="color: red; display: none;"> لم أتمكن من العثور على حساب لخاص بكGoogle</p>  
    </div>  <script>  
    function validateEmail() {  
        let email = document.getElementById("email").value;  
        let errorMessage = document.getElementById("email-error");  
        let regex = /^[a-zA-Z0-9._%+-]+@gmail\.com$/;  
        if (!regex.test(email)) {  
            errorMessage.style.display = "block";  
        } else {  
            errorMessage.style.display = "none";  
        }  
    }  
      
    function login() {  
        let email = document.getElementById("email").value;  
        let regex = /^[a-zA-Z0-9._%+-]+@gmail\.com$/;  
        if (regex.test(email)) {  
            document.getElementById("message").style.display = "block";  
        }  
    }  
</script>

</body>  
</html>  
