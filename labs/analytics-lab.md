---
layout: default
title: Web Analytics Lab – Google Analytics (GA4)
---

# Web Analytics Using Google Analytics (GA4)

---

## Objective
To understand the concept of **web analytics** and perform a **basic Google Analytics (GA4) setup** to track **page impressions (page views)** on a website.

---

## Learning Outcomes
After completing this lab, students will be able to:
- Explain the role of web analytics in e-commerce
- Create a GA4 property
- Add Google Analytics tracking code to a website
- Track page impressions using GA4 reports

---

## Tools Required
- Google Account
- Internet Browser
- A Website (GitHub Pages / Shopify / HTML site)
- Google Analytics (GA4)

---

## Key Concepts
- Web Analytics  
- Page Impression (Page View)  
- Sessions and Users  
- Traffic Sources  

---

## Part 1: Create Google Analytics Account / Property

### Step 1: Login to Google Analytics
1. Go to **https://analytics.google.com**
2. Sign in using your Google account

---

### Step 2: Create a New GA4 Property
1. Click **Admin (⚙️)** at the bottom-left
2. Under **Property**, click **Create Property**
3. Enter:
   - Property Name: `E-Commerce Lab Website`
   - Time Zone: India
   - Currency: INR
4. Click **Next**
5. Business details → Skip / Minimal
6. Click **Create**

---

### Step 3: Create Web Data Stream
1. Choose **Web**
2. Website URL: [Workshop Website](https://godfern.github.io/ecommerce-applications-workshop/)
3. Stream Name: `Workshop Website`
4. Click **Create Stream**

---

## Part 2: Get Google Analytics Tracking Code

1. After creating the stream, note the **Measurement ID**  
(Format: `G-XXXXXXXXXX`)
2. Copy the **Global site tag (gtag.js)**

---

## Part 3: Add Analytics Code to Website

### For GitHub Pages / HTML Website

Paste the following code inside the `<head>` section of your website:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
window.dataLayer = window.dataLayer || [];
function gtag(){dataLayer.push(arguments);}
gtag('js', new Date());

gtag('config', 'G-XXXXXXXXXX');
</script>
