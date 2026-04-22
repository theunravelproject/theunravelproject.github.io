---
layout: default
title: Home
permalink: /
---

# Hello

This is our homepage

<h2 class="mt-5 mb-3">Contact Us</h2>

<form action="https://api.staticforms.xyz/submit" method="POST" class="mb-5">

  <!-- StaticForms Access Key -->
  <input type="hidden" name="accessKey" value="sf_ecb49cba207c94bdaa4cdc53">

  <!-- Optional: redirect after submit -->
  <input type="hidden" name="redirectTo" value="https://theunravelproject.github.io/PSYOPtics-Collection/contact-success.html">

  <div class="mb-3">
    <label class="form-label">Your Name</label>
    <input type="text" name="name" class="form-control" required>
  </div>

  <div class="mb-3">
    <label class="form-label">Your Email (optional)</label>
    <input type="email" name="email" class="form-control">
  </div>

  <div class="mb-3">
    <label class="form-label">Your Message</label>
    <textarea name="message" class="form-control" rows="5" required></textarea>
  </div>

  <button type="submit" class="btn btn-primary">Send Message</button>
</form>
