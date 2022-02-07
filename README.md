# Captcha 
Simple Captcha for PHP website

## How to Install?
You can Install it via composer by typing:-

composer require litto/captcha:v1.0

## How it works?

In the form just add:-
    
           <img src="captcha.php" alt="captcha" title="captcha" class="captcha" width="100px" height="50px">
              <label for="email2">Enter Code</label>
              <input  class="form-control"  name="txtCode"  type="text"  value="Captcha">
    
In the form submission function, just do like this:-

session_start();
$text=$_SESSION["vercode"] ;
unset($_SESSION["vercode"]);
 $captcha        =  $_POST['txtCode'];
  if($captcha==$text)
{
// Save Function
}else{
//captcha Validation Error
}
