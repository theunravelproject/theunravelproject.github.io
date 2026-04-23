---
layout: default
title: Home
permalink: /
---

<div style="text-align:center;">

 <h1>WELCOME TO UNRAVEL</h1>

A STATIC PUBLIC BROADCASTING NETWORK
SEND US A MESSAGE WITH YOUR THOUGHTS, QUESTIONS, OR ANYTHING INTERESTING

<div class="d-flex justify-content-center mt-5">
  <div class="col-12 col-md-8 col-lg-6">

    <h2 class="mb-4">Contact Us</h2>

    <form action="https://api.staticforms.xyz/submit" method="POST">

      <!-- StaticForms Access Key -->
      <input type="hidden" name="accessKey" value="sf_ecb49cba207c94bdaa4cdc53">

      <!-- Optional redirect -->
      <input type="hidden" name="redirectTo" value="https://theunravelproject.github.io/PSYOPtics-Collection/contact-success.html">

      <div class="mb-3 text-start">
        <label class="form-label">Your Name</label>
        <input type="text" name="name" class="form-control custom-input" required>
      </div>

      <div class="mb-3 text-start">
        <label class="form-label">Your Email (optional)</label>
        <input type="email" name="email" class="form-control custom-input">
      </div>

      <div class="mb-3 text-start">
        <label class="form-label">Your Message</label>
        <textarea name="message" class="form-control custom-input" rows="5" required></textarea>
      </div>

      <button type="submit" class="btn custom-send-btn px-4 py-2">Send Message</button>

    </form>

  </div>
</div>

</div>

<style>
  /* Black input boxes with white border + white text */
  .custom-input {
    background-color: #000000 !important;
    color: #ffffff !important;
    border: 2px solid #ffffff !important;
    font-family: 'Share Tech Mono', monospace !important;
  }

  .custom-input::placeholder {
    color: #cccccc !important;
  }

  .custom-input:focus {
    background-color: #000000 !important;
    color: #ffffff !important;
    border-color: #ffffff !important;
    box-shadow: none !important;
  }

  /* Custom Send Message button */
  .custom-send-btn {
    background-color: #000000 !important;
    color: #ffffff !important;
    border: 2px solid #ffffff !important;
    font-family: 'Share Tech Mono', monospace !important;
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  .custom-send-btn:hover {
    background-color: #1a1a1a !important;
    border-color: #ffffff !important;
    color: #ffffff !important;
  }
</style>
