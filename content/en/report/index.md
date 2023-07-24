---
title: "Report Incorrect Data"
description: "Report incorrect data to us"
date: 2020-08-27T19:23:18+02:00
lastmod: 2020-08-27T19:23:18+02:00
draft: false
images: []
---

<body>
  <p>Due to the automated nature of our data collection process, we cannot guarantee the accuracy of our data. If you find incorrect data, please report it to us using the form below.</p>

  <p>Note from developer: This is a project I operate for free in my spare time, so please be patient with me. I will do my best to fix any issues as soon as possible.</p>
  <!-- modify this form HTML and place wherever you want your form -->
  <form action="https://formspree.io/f/xwkdpapq" method="POST">
    <div class="form-group">
      <label for="textarea">Brief Description of Issue</label>
      <textarea class="form-control" id="exampleFormControlTextarea1" rows="5" style="color: black" name="issue_description" required></textarea>
      <small id="emailHelp" class="form-text text-muted">Any info provided will help us diagnose the issue.</small>
    </div>
    <div class="form-group">
      <label for="exampleInputPassword1">API Endpoint (if applicable)</label>
      <input type="text" class="form-control" id="exampleInputPassword1" style="color: black" name="api_endpoint">
      <small id="emailHelp" class="form-text text-muted">If you are reporting an issue with a specific API endpoint, please provide the endpoint here.</small>
    </div>
    <div class="form-group">
      <label for="exampleInputEmail1">Email address (optional)</label>
      <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" style="color: black" name='email_address'>
      <small id="emailHelp" class="form-text text-muted">Provide an email if you are able to be contacted for more info if needed.</small>
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
</body>