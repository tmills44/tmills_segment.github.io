<!DOCTYPE html>
<html lang="en">
<head>
  <script>
    !function(){var i="analytics",analytics=window[i]=window[i]||[];if(!analytics.initialize)if(analytics.invoked)window.console&&console.error&&console.error("Segment snippet included twice.");else{analytics.invoked=!0;analytics.methods=["trackSubmit","trackClick","trackLink","trackForm","pageview","identify","reset","group","track","ready","alias","debug","page","screen","once","off","on","addSourceMiddleware","addIntegrationMiddleware","setAnonymousId","addDestinationMiddleware","register"];analytics.factory=function(e){return function(){if(window[i].initialized)return window[i][e].apply(window[i],arguments);var n=Array.prototype.slice.call(arguments);if(["track","screen","alias","group","page","identify"].indexOf(e)>-1){var c=document.querySelector("link[rel='canonical']");n.push({__t:"bpc",c:c&&c.getAttribute("href")||void 0,p:location.pathname,u:location.href,s:location.search,t:document.title,r:document.referrer})}n.unshift(e);analytics.push(n);return analytics}};for(var n=0;n<analytics.methods.length;n++){var key=analytics.methods[n];analytics[key]=analytics.factory(key)}analytics.load=function(key,n){var t=document.createElement("script");t.type="text/javascript";t.async=!0;t.setAttribute("data-global-segment-analytics-key",i);t.src="https://cdn.segment.com/analytics.js/v1/" + key + "/analytics.min.js";var r=document.getElementsByTagName("script")[0];r.parentNode.insertBefore(t,r);analytics._loadOptions=n};analytics._writeKey="wbheZm9IKQ0nqu451vrbOYCDhM6OWVOv";;analytics.SNIPPET_VERSION="5.2.0";
      analytics.load("wbheZm9IKQ0nqu451vrbOYCDhM6OWVOv");
      analytics.page();
    }}();
  </script>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pet Registration</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Work+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --sage: #E7EEE2;
    --pine: #1F3B2C;
    --pine-light: #2E5240;
    --brass: #B8863C;
    --brass-dark: #96692A;
    --ink: #1C241D;
    --paper: #FBFAF6;
    --line: #CBD6C3;
  }

  *{ box-sizing: border-box; }

  body{
    margin:0;
    background: var(--sage);
    color: var(--ink);
    font-family: 'Work Sans', sans-serif;
    -webkit-font-smoothing: antialiased;
  }

  .wrap{
    max-width: 620px;
    margin: 0 auto;
    padding: 64px 24px 80px;
  }

  .tag{
    display:inline-flex;
    align-items:center;
    gap:8px;
    background: var(--pine);
    color: var(--sage);
    padding: 6px 14px 6px 10px;
    border-radius: 999px;
    font-size: 13px;
    letter-spacing: 0.02em;
    margin-bottom: 28px;
  }
  .tag svg{ width:16px; height:16px; }

  h1{
    font-family: 'Fraunces', serif;
    font-weight: 600;
    font-size: clamp(32px, 5vw, 44px);
    line-height: 1.08;
    margin: 0 0 14px;
    max-width: 15ch;
  }

  .lede{
    font-size: 16px;
    line-height: 1.55;
    color: #445042;
    max-width: 46ch;
    margin: 0 0 44px;
  }

  form{
    background: var(--paper);
    border: 1px solid var(--line);
    border-radius: 18px;
    padding: 8px;
  }

  fieldset{
    border: none;
    margin: 0;
    padding: 28px 28px 8px;
  }

  fieldset + fieldset{
    border-top: 1px solid var(--line);
    padding-top: 28px;
  }

  legend{
    font-family: 'Fraunces', serif;
    font-size: 19px;
    font-weight: 500;
    color: var(--pine);
    padding: 0;
    margin-bottom: 4px;
  }

  .legend-sub{
    font-size: 13.5px;
    color: #6B776A;
    margin: 0 0 20px;
  }

  .field{
    margin-bottom: 18px;
  }

  .field:last-child{ margin-bottom: 0; }

  label{
    display:block;
    font-size: 13.5px;
    font-weight: 600;
    color: var(--ink);
    margin-bottom: 6px;
  }

  input{
    width: 100%;
    padding: 12px 14px;
    border: 1px solid var(--line);
    border-radius: 9px;
    font-family: 'Work Sans', sans-serif;
    font-size: 15px;
    background: #fff;
    color: var(--ink);
    transition: border-color 0.15s ease, box-shadow 0.15s ease;
  }

  input:focus{
    outline: none;
    border-color: var(--brass);
    box-shadow: 0 0 0 3px rgba(184,134,60,0.18);
  }

  input:invalid:not(:placeholder-shown){
    border-color: #B4483B;
  }

  .hint{
    font-size: 12.5px;
    color: #7A867A;
    margin-top: 5px;
  }

  .actions{
    padding: 24px 28px 28px;
  }

  button{
    width: 100%;
    background: var(--brass);
    color: #fff;
    border: none;
    border-radius: 9px;
    padding: 14px 18px;
    font-family: 'Work Sans', sans-serif;
    font-size: 15.5px;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.15s ease;
  }

  button:hover{ background: var(--brass-dark); }
  button:disabled{ background: #C9BCA3; cursor: default; }

  .status{
    margin-top: 14px;
    font-size: 14px;
    text-align: center;
    min-height: 20px;
  }

  .status.ok{ color: var(--pine-light); font-weight: 600; }
  .status.err{ color: #B4483B; font-weight: 600; }

  .setup-note{
    max-width: 620px;
    margin: 32px auto 0;
    padding: 16px 20px;
    background: #FFF7E8;
    border: 1px solid #E9D3A0;
    border-radius: 12px;
    font-size: 13.5px;
    line-height: 1.5;
    color: #5C4A21;
  }
  .setup-note code{
    background: #F3E4C0;
    padding: 1px 5px;
    border-radius: 4px;
    font-size: 12.5px;
  }
</style>
</head>
<body>

<div class="wrap">

  <span class="tag">
    <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
      <circle cx="12" cy="14" r="4.2" fill="currentColor"/>
      <circle cx="5.5" cy="8.5" r="2.1" fill="currentColor"/>
      <circle cx="18.5" cy="8.5" r="2.1" fill="currentColor"/>
      <circle cx="8" cy="4" r="1.7" fill="currentColor"/>
      <circle cx="16" cy="4" r="1.7" fill="currentColor"/>
    </svg>
    Pet registration
  </span>

  <h1>Tell us about you and your pet</h1>
  <p class="lede">A couple of minutes to get your details and your pet's details on file. Everything here gets sent straight to Segment as you submit.</p>

  <form id="pet-form" novalidate>

    <fieldset>
      <legend>Your details</legend>
      <p class="legend-sub">How we'll reach you.</p>

      <div class="field">
        <label for="owner-name">Full name</label>
        <input type="text" id="owner-name" name="ownerName" placeholder="Jamie Rivera" autocomplete="name" required>
      </div>

      <div class="field">
        <label for="owner-email">Email address</label>
        <input type="email" id="owner-email" name="ownerEmail" placeholder="jamie@example.com" autocomplete="email" required>
      </div>

      <div class="field">
        <label for="owner-phone">Phone number</label>
        <input type="tel" id="owner-phone" name="ownerPhone" placeholder="(555) 012-3456" autocomplete="tel" required>
      </div>
    </fieldset>

    <fieldset>
      <legend>Pet details</legend>
      <p class="legend-sub">Who we're actually excited to meet.</p>

      <div class="field">
        <label for="pet-name">Pet name</label>
        <input type="text" id="pet-name" name="petName" placeholder="Biscuit" required>
      </div>

      <div class="field">
        <label for="pet-breed">Breed</label>
        <input type="text" id="pet-breed" name="petBreed" placeholder="Labrador Retriever" required>
      </div>

      <div class="field">
        <label for="pet-weight">Weight (lbs)</label>
        <input type="number" id="pet-weight" name="petWeight" placeholder="42" min="0" step="0.1" required>
        <p class="hint">Estimates are fine.</p>
      </div>
    </fieldset>

    <div class="actions">
      <button type="submit" id="submit-btn">Save pet record</button>
      <p class="status" id="status"></p>
    </div>

  </form>

  <p class="setup-note">
    <strong>Setup:</strong> replace <code>YOUR_SEGMENT_WRITE_KEY</code> near the bottom of this file with your Segment source's write key before this can send data. On submit, the form calls <code>analytics.identify()</code> with the owner's details and <code>analytics.track('Pet Registered', …)</code> with the pet's details.
  </p>

</div>

<!-- Segment analytics.js snippet -->
<script>
  !function(){var analytics=window.analytics=window.analytics||[];if(!analytics.initialize)if(analytics.invoked)window.console&&console.error&&console.error("Segment snippet included twice.");else{analytics.invoked=!0;analytics.methods=["trackSubmit","trackClick","trackLink","trackForm","pageview","identify","reset","group","track","ready","alias","debug","page","once","off","on","addSourceMiddleware","addIntegrationMiddleware","setAnonymousId","addDestinationMiddleware"];analytics.factory=function(e){return function(){var t=Array.prototype.slice.call(arguments);t.unshift(e);analytics.push(t);return analytics}};for(var e=0;e<analytics.methods.length;e++){var key=analytics.methods[e];analytics[key]=analytics.factory(key)}analytics.load=function(key,e){var t=document.createElement("script");t.type="text/javascript";t.async=!0;t.src="https://cdn.segment.com/analytics.js/v1/" + key + "/analytics.min.js";var n=document.getElementsByTagName("script")[0];n.parentNode.insertBefore(t,n);analytics._loadOptions=e};analytics._writeKey="YOUR_SEGMENT_WRITE_KEY";analytics.SNIPPET_VERSION="4.16.1";
  analytics.load("YOUR_SEGMENT_WRITE_KEY");
  analytics.page();
  }}();
</script>

<script>
  const form = document.getElementById('pet-form');
  const statusEl = document.getElementById('status');
  const submitBtn = document.getElementById('submit-btn');

  form.addEventListener('submit', function (e) {
    e.preventDefault();

    if (!form.checkValidity()) {
      form.reportValidity();
      return;
    }

    const ownerName = document.getElementById('owner-name').value.trim();
    const ownerEmail = document.getElementById('owner-email').value.trim();
    const ownerPhone = document.getElementById('owner-phone').value.trim();
    const petName = document.getElementById('pet-name').value.trim();
    const petBreed = document.getElementById('pet-breed').value.trim();
    const petWeight = parseFloat(document.getElementById('pet-weight').value);

    submitBtn.disabled = true;
    submitBtn.textContent = 'Saving…';
    statusEl.textContent = '';
    statusEl.className = 'status';

    try {
      // Identify the pet owner as the user
      window.analytics.identify(ownerEmail, {
        name: ownerName,
        email: ownerEmail,
        phone: ownerPhone
      });

      // Track the pet details as an event tied to that user
      window.analytics.track('Pet Registered', {
        petName: petName,
        petBreed: petBreed,
        petWeight: petWeight
      });

      statusEl.textContent = 'Saved — sent to Segment.';
      statusEl.className = 'status ok';
      submitBtn.textContent = 'Save pet record';
      submitBtn.disabled = false;
      form.reset();
    } catch (err) {
      console.error(err);
      statusEl.textContent = 'Something went wrong sending this. Check the console.';
      statusEl.className = 'status err';
      submitBtn.textContent = 'Save pet record';
      submitBtn.disabled = false;
    }
  });
</script>

</body>
</html>
# tmills_segment.github.io
Segment training
