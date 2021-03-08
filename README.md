# QR-Code-Maker
This little website allows you to create a QR code for any URL you enjoy visiting!

----------------------------------------------------------------------------------


QR code example: ![image](https://user-images.githubusercontent.com/74619699/110327758-6515cd80-7fe8-11eb-84be-8376e58725a1.png)

Support all your URL needs with this little app! QR codes are the future!



================================
Viewer code is available here:

!DOCTYPE html> html> head> link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.3.7/css/bootstrap.min.css" /> style> .qr-code { max-width: 300px; margin: 40px; } button { background-color: rgb(0, 119, 255); color: white } /style> title>QR Code Generator/title> /head> body> div class="container-fluid"> div class="text-center"> img src="https://chart.googleapis.com/chart?cht=qr&chl=Hello+World&chs=160x160&chld=L|0" class="qr-code img-thumbnail img-responsive" /> /div> div class="form-horizontal"> div class="form-group"> label class="control-label col-sm-20" for="content"> URL: /label> div class="col-sm-20"> input type="text" placeholder="URL Goes Here:" size="30" maxlength="50" class="form-control" id="content" /> /div> /div> div class="form-group"> div class="col-sm-offset-100 col-sm-100"> button type="button" class="btn-default" id="generate"> Build QR Code /button> button type="button" onclick="if (confirm('Are you sure you want to delete this QR code? Proceeding will result in a loss of work!')) { // Save it! window.location.href = '/index.html' } else { // Do nothing! console.log('Thing was not saved to the database.'); }" > Back /button> button type="button" onclick="if (confirm('Are you sure you want to delete this QR code? Proceeding will result in a loss of work!')) { // Save it! window.location.reload() } else { // Do nothing! console.log('Thing was not saved to the database.'); }"" a href = "mailto:?subject = Look, I made a QR code! = This code was made here: https://4jxf2.csb.app/index.html Upload QR code here:"> Share Code /a> /button> /div> /div> /div> /div> script src="https://code.jquery.com/jquery-3.5.1.js"> script> // Function to HTML encode the text // This creates a new hidden element, // inserts the given text into it // and outputs it out as HTML function htmlEncode(value) { return $("div/>").text(value).html(); } $(function () { // Specify an onclick function // for the generate button $("#generate").click(function () { // Generate the link that would be // used to generate the QR Code // with the given data let finalURL = "https://chart.googleapis.com/chart?cht=qr&chl=" + htmlEncode($("#content").val()) + "&chs=160x160&chld=L|0"; // Replace the src of the image with // the QR code image $(".qr-code").attr("src", finalURL); }); }); /script> /body> /html>




