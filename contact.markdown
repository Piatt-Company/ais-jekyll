---
layout: single
title: "Contact Us"
permalink: /contact/
author_profile: true
sidebar:
  nav: "main"
---

We engage with hyperscalers, colocation providers, and enterprise AI labs. 

### Headquarters
**AI Infrastructure Services** San Antonio, Texas  
USA

---

### Business Inquiries

For RFP invitations or site assessment requests, please contact us directly.

**Email:** [bret@ai-infraservices.com](mailto:bret@ai-infraservices.com)

---

### Secure Inquiry Form

<form id="contact-form">
  <div class="form-group">
    <label for="email">Your Email Address</label>
    <input type="email" name="email" id="email" class="form-control" placeholder="name@company.com" required>
  </div>
  
  <div class="form-group">
    <label for="message">Message</label>
    <textarea name="message" id="message" class="form-control" rows="6" placeholder="How can we support your infrastructure?" required></textarea>
  </div>

  <button type="submit" id="submit-btn" class="btn btn--primary btn--large">Send Message</button>
  <p id="form-status" style="margin-top: 1em; font-weight: bold;"></p>
</form>

<script>
  document.getElementById("contact-form").addEventListener("submit", async function(event) {
    event.preventDefault();

    const form = event.target;
    const status = document.getElementById("form-status");
    const btn = document.getElementById("submit-btn");

    // Google Apps Script Web App URL
    const scriptUrl = "https://script.google.com/macros/s/AKfycbwI4wKHaHUeKqymmk8vsqCIgurG0kbKTi4r2BtwxwgkZWEz9rnimkRliWesrUbTQSGkUg/exec";

    // Prepare Data
    const formData = new FormData(form);
    const data = Object.fromEntries(formData.entries());

    try {
      btn.disabled = true;
      btn.innerText = "Sending...";

      // Send to Google (Using text/plain to avoid CORS preflight)
      const response = await fetch(scriptUrl, {
        method: "POST",
        body: JSON.stringify(data) 
      });

      if (response.ok) {
        status.innerText = "Message sent successfully. We will be in touch shortly.";
        status.style.color = "green";
        form.reset();
      } else {
        throw new Error("Network response was not ok.");
      }
    } catch (error) {
      status.innerText = "There was an error sending your message. Please email us directly.";
      status.style.color = "red";
      console.error(error);
    } finally {
      btn.disabled = false;
      btn.innerText = "Send Message";
    }
  });
</script>