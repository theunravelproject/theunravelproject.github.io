---
layout: default
title: Home
permalink: /
---

# Hello

This is our homepage

<div class="d-flex justify-content-center mt-5">
  <div class="col-12 col-md-8 col-lg-6">

    <h2 class="text-center mb-4">Contact Us</h2>

    <form action="https://api.staticforms.xyz/submit" method="POST">

      <!-- StaticForms Access Key -->
      <input type="hidden" name="accessKey" value="sf_ecb49cba207c94bdaa4cdc53">

      <!-- Optional redirect -->
      <input type="hidden" name="redirectTo" value="https://theunravelproject.github.io/PSYOPtics-Collection/contact-success.html">

      <div class="mb-3">
        <label class="form-label">Your Name</label>
        <input type="text" name="name" class="form-control custom-input" required>
      </div>

      <div class="mb-3">
        <label class="form-label">Your Email (optional)</label>
        <input type="email" name="email" class="form-control custom-input">
      </div>

      <div class="mb-3">
        <label class="form-label">Your Message</label>
        <textarea name="message" class="form-control custom-input" rows="5" required></textarea>
      </div>

      <div class="text-center">
        <button type="submit" class="btn btn-primary px-4">Send Message</button>
      </div>

    </form>

  </div>
</div>

<style>
  /* Dark gray input boxes with white text */
  .custom-input {
    background-color: #3a3a3a !important;
    color: #ffffff !important;
    border: 1px solid #555 !important;
  }

  .custom-input::placeholder {
    color: #cccccc !important;
  }

  .custom-input:focus {
    background-color: #2f2f2f !important;
    color: #ffffff !important;
    border-color: #888 !important;
    box-shadow: none !important;
  }
</style>
