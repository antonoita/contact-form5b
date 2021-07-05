# contact-form5b
<div class= "contact-title">
<h1><em>any heater,all solutions<em></h1>
<h2><em>get faster and simple solutions<em></h2>

<div class="contact-form">
<form id="contact-form" method= " post" action= "youtube-contact-formphp.php">
<input name="name" type="text" class="form-control" placeholder="your name" required><br>
<input name="email" type="email" class="form-control" placeholder="your email" required><br>
<textarea name="message" class="form-control" placeholder= "message" row="7" required></textarea><br>

<input type="submit" class="form-control submit" value="send message">
</form>

</div>
<?php
      $name = $_POST['name'];
      $visitor_email = $_post['email'];
      $message = $_POST['message']

      $email_from = ' kuileyshi3000k@gmail.com';
      
      $email_subject = "new form submission";
      
      $email_body = "User name: $name.\n."
                      "User Email: $visitor_email.\n."
                        "User message: $message.\n";

     $to = "kuileyshi3000k@gmail.com";
     $header ="from: $email_from \r\n";
$headers .= "reply-to: $visitor_email \r\n";
 mail($to,$email_subject,$email_body,$headers);
    header( " location: index.html");
?>
