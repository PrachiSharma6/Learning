<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Register</title>
</head>
<body>
    <div class="wrapper">
        <h2>Registration</h2>
    <form action = "Register.php" method = "post">
        <div class="input-box"><label class="label">Email :</label> <input type = "email" name = "email" placeholder="Enter email address"></div>
        
        <div class="input-box"> <label class="label">Password : </label><input type = "password" name = "password" placeholder="Enter password"></div>
        <div class="input-box"> <label class="label">Name : </label><input type = "text" name = "name" placeholder="Enter name"></div>
        <div class="input-box"><label class="label">Address : </label><input type = "text" name = "address" placeholder="Enter address"></div>
        <div class="input-box"><label class="label">Phone : </label><input type = "number" name = "phone" placeholder="Enter phone"></div>
    <div class="input-box button"><input type = "Submit"></div>
   
    <div class="text">
        <h3>Already have an account? <a href = "Login.html">Login</a></h3>
      </div>
</div>
</form>
</body>
</html>
