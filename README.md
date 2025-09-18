<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>example of div</title>
</head>
<body>
     <h2> Details form</h2>
    <div>   
        <lable for ="name">Name:</lable>
        <input type="text" id="name" name="name"  placeholder="Enter your name.">
    </div>
    <br>
    <div>   
        <lable for ="email">Email:</lable>
        <input type="email" id="email" name="email"  placeholder="Enter your email.">
    </div>
    <br>
    <div>   
        <lable for ="phone">Phone:</lable>
        <input type="phone" id="phone" name="phone" placeholder="Enter your 10 digit no." pattern="[0-9]{10}" inputmode="numeric" required aria-required="true" aria-describedby="phone-error" onkeypress="restrictAlphabets(event)">
        <span id ="phone-error" role="alert" style="display: none;">numbers only.</span>"></span> 
    </div>
    <script>
        function restrictAlphabets(event) {
            const key = event.key;
            if (!/[0-9]/.test(key) && key !=="Backspace"
            && key !=="ArrowLeft" && key !== "ArrowRight"){
                event.preventDefault();
            }
        }
    </script>
</body>
</html>
