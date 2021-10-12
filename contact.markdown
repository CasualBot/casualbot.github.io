---
title: Contact Me!
layout: page
---
<div>
</div>
### If you ask anyone I love to talk! Want to chat? Let's chat!
#### Things I love to talk about:
* 🐕 **My dog** 
* 🥴 **Burn out in the tech industry**
* 🎮 **Video Games & Streaming**


<form id="my-form" action="https://formspree.io/f/xjvjznvo" method="POST">
<div class="form-left-decoration"></div>
<div class="form-right-decoration"></div>
<div class="circle"></div>
<div class="form-inner">
    <input type="email" name="email" placeholder="fake@news.com" />
    <textarea placeholder="Message..." rows="5"></textarea>
    <button id="my-form-button"
            class="g-recaptcha" 
            data-sitekey="6LfTS8gcAAAAACSB0m3LRs28yq6LXZ1KZ4H1fUHO" 
            data-callback='onSubmit' 
            data-action='submit'>Submit
    </button>
    <p id="my-form-status"></p>
</div>
</form>
<!-- Place this script at the end of the body tag -->
<script>
    var form = document.getElementById("my-form");
    
    async function handleSubmit(event) {
      event.preventDefault();
      var status = document.getElementById("my-form-status");
      var data = new FormData(event.target);
      fetch(event.target.action, {
        method: form.method,
        body: data,
        headers: {
            'Accept': 'application/json'
        }
      }).then(response => {
        status.innerHTML = "Thanks for your submission!";
        form.reset()
      }).catch(error => {
        status.innerHTML = "Oops! There was a problem submitting your form"
      });
    }
    form.addEventListener("submit", handleSubmit)
</script>
<style>
form {
    position: relative;
    width: 80%;
    border-radius: 30px;
    background: #fff;
}
.form-left-decoration,
.form-right-decoration {
    content: "";
    position: absolute;
    width: 50px;
    height: 20px;
    border-radius: 20px;
    background: #800000;
}
.form-left-decoration {
    bottom: 60px;
    left: -30px;
}
.form-right-decoration {
    top: 60px;
    right: -30px;
}
.form-left-decoration:before,
.form-left-decoration:after,
.form-right-decoration:before,
.form-right-decoration:after {
    content: "";
    position: absolute;
    width: 50px;
    height: 20px;
    border-radius: 30px;
    background: #fff;
}
.form-left-decoration:before {
    top: -20px;
}
.form-left-decoration:after {
    top: 20px;
    left: 10px;
}
.form-right-decoration:before {
    top: -20px;
    right: 0;
}
.form-right-decoration:after {
    top: 20px;
    right: 10px;
}
.circle {
    position: absolute;
    bottom: 80px;
    left: -55px;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background: #fff;
}
.form-inner {
padding: 40px;
}
.form-inner input,
.form-inner textarea {
    display: block;
    width: 100%;
    padding: 15px;
    margin-bottom: 10px;
    border: none;
    border-radius: 20px;
    background: #d0dfe8;
}
.form-inner textarea {
resize: none;
}
button {
    width: 100%;
    padding: 10px;
    margin-top: 20px;
    border-radius: 20px;
    border: none;
    border-bottom: 4px solid #b00000;
    background: #800000; 
    font-size: 16px;
    font-weight: 400;
    color: #fff;
}
button:hover {
background: #030303   ;
} 
@media (min-width: 568px) {
form {
width: 60%;
}
}
</style>
 <script src="https://www.google.com/recaptcha/api.js"></script>
  <script>
   function onSubmit(token) {
     document.getElementById("my-form").submit();
   }
 </script>