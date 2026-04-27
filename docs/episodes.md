---
layout: default
title: Episodes
permalink: /episodes/
---

<style>
input.custom-input,
textarea.custom-input {
  background-color: #000;
  color: #fff;
  border: 1px solid #fff;
  font-family: 'Share Tech Mono', monospace;
}

input.custom-input::placeholder,
textarea.custom-input::placeholder {
  color: #ccc;
}

button.custom-button {
  background-color: #000;
  color: #fff;
  border: 1px solid #fff;
  font-family: 'Share Tech Mono', monospace;
  padding: 0.5rem 1.5rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}
</style>

# EPISODES

<div style="margin-bottom: 2rem;">
  <h3>Table of Contents</h3>
  <ul>
    <li><a href="#episode-1">Episode 1 — PSYOPtics</a></li>
    <!-- Later: more episodes here -->
  </ul>
</div>

<hr>

<div id="episode-1" style="margin-top: 3rem;">

  <h2>Episode 1 — PSYOPtics: Psychological Operations and the Formation of American Reality</h2>

  <!-- Video embed -->
  <div style="margin: 1.5rem 0;">
    <!-- Replace the src with your actual video URL/embed -->
    <iframe 
      width="100%" 
      height="400" 
      src="https://www.youtube.com/embed/VIDEO_ID" 
      title="Episode 1"
      frameborder="0" 
      allowfullscreen>
    </iframe>
  </div>

  <!-- Bio / description -->
  <div style="margin-bottom: 2rem;">
    <h3>Episode Bio</h3>
    <p>
      episode bio!!
    </p>
  </div>

 <form action="https://api.staticforms.xyz/submit" method="post" style="max-width: 600px; margin: 0 auto; text-align:left;">

  <!-- StaticForms required hidden fields -->
  <input type="hidden" name="accessKey" value="sf_ecb49cba207c94bdaa4cdc53">
  <input type="hidden" name="redirectTo" value="https://theunravelproject.github.io/episodes/#episode-1">
  <input type="hidden" name="episode" value="Episode 1">
  <input type="hidden" name="github" value="theunravelproject/theunravelproject.github.io">

  <!-- Name -->
  <div style="margin-bottom: 1.5rem;">
    <label for="name" style="color:white; font-family:'Share Tech Mono', monospace;">Name</label><br>
    <input 
      type="text" 
      id="name" 
      name="name" 
      class="custom-input"
      style="width: 100%; padding: 0.5rem;">
  </div>

  <!-- Email -->
  <div style="margin-bottom: 1.5rem;">
    <label for="email" style="color:white; font-family:'Share Tech Mono', monospace;">Email (optional, not shown publicly)</label><br>
    <input 
      type="email" 
      id="email" 
      name="email" 
      class="custom-input"
      style="width: 100%; padding: 0.5rem;">
  </div>

  <!-- Message -->
  <div style="margin-bottom: 1.5rem;">
    <label for="message" style="color:white; font-family:'Share Tech Mono', monospace;">Your thoughts</label><br>
    <textarea 
      id="message" 
      name="message" 
      rows="5" 
      required
      class="custom-input"
      style="width: 100%; padding: 0.5rem;"></textarea>
  </div>

  <!-- Submit -->
  <div style="text-align:right;">
    <button 
      type="submit" 
      class="custom-button">
      POST COMMENT
    </button>
  </div>

</form>

<!-- ========================= -->
<!-- EPISODE 1 PUBLIC COMMENTS -->
<!-- ========================= -->

<h3 style="margin-top:3rem; color:white; font-family:'Share Tech Mono', monospace;">
  Public Discussion
</h3>

{% comment %}
STEP 1 — Pull all GitHub Issues for this repo
GitHub Pages automatically exposes them via site.github.issues
{% endcomment %}

{% assign all_comments = site.github.issues %}

{% comment %}
STEP 2 — Filter to Episode 1 only
StaticForms sends "episode: Episode 1" in the Issue body.
We match that.
{% endcomment %}

{% assign ep1_comments = all_comments | where_exp: "item", "item.body contains 'Episode 1'" %}

{% comment %}
STEP 3 — Separate top-level comments from replies
Replies will contain "reply-to:ISSUE_NUMBER"
Top-level comments will NOT contain "reply-to:"
{% endcomment %}

{% assign top_level = ep1_comments | reject: "body", "reply-to:" %}

{% comment %}
STEP 4 — Sort oldest first
{% endcomment %}

{% assign sorted_top = top_level | sort: "created_at" %}

<div style="margin-top:2rem;">

  {% for comment in sorted_top %}
    <div style="border:1px solid white; padding:1rem; margin-bottom:1.5rem;">

      <!-- Comment header -->
      <div style="color:white; font-family:'Share Tech Mono', monospace; margin-bottom:0.5rem;">
        <strong>{{ comment.user.login }}</strong>
        <span style="opacity:0.6; font-size:0.9rem;">
          — {{ comment.created_at | date: "%B %d, %Y" }}
        </span>
      </div>

      <!-- Comment body -->
      <div style="color:white; font-family:'Share Tech Mono', monospace; margin-bottom:1rem;">
        {{ comment.body | newline_to_br }}
      </div>

      <!-- Reply button (scrolls to reply form) -->
      <a href="#reply-to-{{ comment.number }}" 
         style="color:white; font-family:'Share Tech Mono', monospace; text-decoration:underline;">
        Reply
      </a>

      <!-- ========================= -->
      <!-- NESTED REPLIES FOR THIS COMMENT -->
      <!-- ========================= -->

      {% assign replies = ep1_comments | where_exp: "item", "item.body contains 'reply-to:{{ comment.number }}'" %}
      {% assign sorted_replies = replies | sort: "created_at" %}

      {% if sorted_replies.size > 0 %}
        <div style="margin-left:2rem; margin-top:1rem;">

          {% for reply in sorted_replies %}
            <div style="border-left:1px solid white; padding-left:1rem; margin-bottom:1rem;">

              <div style="color:white; font-family:'Share Tech Mono', monospace; margin-bottom:0.3rem;">
                <strong>{{ reply.user.login }}</strong>
                <span style="opacity:0.6; font-size:0.9rem;">
                  — {{ reply.created_at | date: "%B %d, %Y" }}
                </span>
              </div>

              <div style="color:white; font-family:'Share Tech Mono', monospace;">
                {{ reply.body | newline_to_br }}
              </div>

            </div>
          {% endfor %}

        </div>
      {% endif %}

    </div>
  {% endfor %}

</div>

