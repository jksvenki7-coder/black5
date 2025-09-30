# black5<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>JKS Group of Business - All Services</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin:0; background: #22232c; color: #fff;
  }
  header {
    font-size: 2.2rem;
    font-weight: bold;
    color: #3aaaff;
    text-align: center;
    padding: 36px 10px 10px 10px;
    user-select: none;
  }
  #dashboard {
    max-width: 960px;
    margin: 20px auto;
    display: grid;
    grid-template-columns: repeat(4,1fr);
    gap: 20px;
  }
  .service-button {
    border: 2.5px solid #ffe066;
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    cursor: pointer;
    font-weight: 600;
    color: #ffe066;
    background-color: #232335;
    box-shadow: 0 0 18px #ffe066aa;
    transition: all 0.3s ease;
    user-select: none;
  }
  .service-button:hover {
    color: #fffbd0;
    background-color: #232342;
    box-shadow: 0 0 38px #ffe066ff;
    transform: scale(1.05);
  }
  .section {
    max-width: 960px;
    margin: 20px auto;
    padding: 20px;
    background: #f9f9f9;
    color: #222;
    border-radius: 12px;
    display: none;
  }
  .section.active {
    display: block;
  }
  h2 {
    color: #205081;
    border-bottom: 3px solid #85bbeb;
    padding-bottom: 6px;
  }
  button.back-button, form button.submit-btn {
    margin-top: 20px;
    padding: 10px 15px;
    font-weight: 600;
    cursor: pointer;
    border: none;
    border-radius: 6px;
    background-color: #3498db;
    color: white;
  }
  a.whatsapp-btn {
    display: inline-block;
    margin: 15px 0;
    background: #25D366;
    color: white;
    padding: 10px 20px;
    border-radius: 6px;
    font-weight: 700;
    text-decoration: none;
  }
  input, textarea, select {
    width: 100%;
    padding: 8px;
    margin-top: 4px;
    border-radius: 6px;
    border: 1px solid #ccc;
    box-sizing: border-box;
  }
  label {
    font-weight: 600;
    margin-top: 12px;
    display: block;
  }
  .error {
    color: red;
    font-size: 0.85em;
    display: none;
    margin-top: 4px;
  }
  nav.small-nav {
    display: flex;
    justify-content: center;
    gap: 12px;
    margin-bottom: 18px;
    flex-wrap: wrap;
  }
  nav.small-nav button {
    padding: 10px 14px;
    font-weight: 600;
    border-radius: 8px;
    border: none;
    cursor: pointer;
    background: #eef2ff;
    color: #3366cc;
    transition: background 0.3s, color 0.3s;
  }
  nav.small-nav button.selected {
    background: #3366cc;
    color: white;
  }
  nav.small-nav button:hover:not(.selected) {
    background: #d3d9f6;
  }
  #map {
    width: 100%;
    height: 300px;
    margin: 20px 0;
    border-radius: 12px;
  }
  video {
    display: block;
    margin: 20px auto;
    border-radius: 12px;
    max-width: 100%;
    height: auto;
  }
</style>
</head>
<body>
<header>JKS Group of Business</header>

<div id="dashboard">
  <div class="service-button" onclick="showSection('ecommerce')">My E-commerce</div>
  <div class="service-button" onclick="showSection('events')">Events & Catering</div>
  <div class="service-button" onclick="showSection('courier')">Courier & Ride Booking</div>
  <div class="service-button" onclick="showSection('job')">Job Consultancy & Services</div>
  <div class="service-button" onclick="showSection('tours')">Tours & Travels</div>
  <div class="service-button" onclick="showSection('realestate')">Real Estate & Construction</div>
  <div class="service-button" onclick="showSection('investment')">Investment & Business</div>
  <div class="service-button" onclick="showSection('loans')">Loans & Insurance</div>
  <div class="service-button" onclick="showSection('homeservices')">Home Services</div>
</div>

<!-- E-commerce Section -->
<div id="ecommerce" class="section">
  <h2>My E-commerce</h2>
  <nav class="small-nav">
    <button class="selected" onclick="switchEcommTab('groceries', this)">Groceries</button>
    <button onclick="switchEcommTab('food', this)">Food</button>
    <button onclick="switchEcommTab('pharmacy', this)">Pharmacy</button>
    <button onclick="switchEcommTab('camera', this)">Camera</button>
    <button onclick="switchEcommTab('maps', this)">Location Map</button>
  </nav>
  <div id="groceriesTab" class="ecomm-tab active">
    <h3>Groceries Categories</h3>
    <form id="ecommerceGroceriesForm">
      <label for="nameEcomGro">Name</label>
      <input type="text" id="nameEcomGro" name="nameEcomGro" required />
      <label for="mobileEcomGro">Mobile Number</label>
      <input type="tel" id="mobileEcomGro" name="mobileEcomGro" pattern="[6-9][0-9]{9}" maxlength="10" required />
      <div class="error" id="mobileEcomGroError">Please enter valid 10-digit mobile number starting with 6-9</div>
      <label for="orderEcomGro">Order Details</label>
      <textarea id="orderEcomGro" name="orderEcomGro" rows="3" required></textarea>
      <label for="addressEcomGro">Delivery Address</label>
      <textarea id="addressEcomGro" name="addressEcomGro" rows="2" required></textarea>
      <button type="submit" class="submit-btn">Place Order via WhatsApp</button>
    </form>
  </div>
  <div id="foodTab" class="ecomm-tab" style="display:none;">
    <h3>Food Categories</h3>
    <form id="ecommerceFoodForm">
      <label for="nameEcomFood">Name</label>
      <input type="text" id="nameEcomFood" name="nameEcomFood" required />
      <label for="mobileEcomFood">Mobile Number</label>
      <input type="tel" id="mobileEcomFood" name="mobileEcomFood" pattern="[6-9][0-9]{9}" maxlength="10" required />
      <div class="error" id="mobileEcomFoodError">Please enter valid 10-digit mobile number starting with 6-9</div>
      <label for="orderEcomFood">Order Details</label>
      <textarea id="orderEcomFood" name="orderEcomFood" rows="3" required></textarea>
      <label for="addressEcomFood">Delivery Address</label>
      <textarea id="addressEcomFood" name="addressEcomFood" rows="2" required></textarea>
      <button type="submit" class="submit-btn">Place Order via WhatsApp</button>
    </form>
  </div>
  <div id="pharmacyTab" class="ecomm-tab" style="display:none;">
    <h3>Pharmacy</h3>
    <form id="ecommercePharmacyForm">
      <label for="nameEcomPhar">Name</label>
      <input type="text" id="nameEcomPhar" name="nameEcomPhar" required />
      <label for="mobileEcomPhar">Mobile Number</label>
      <input type="tel" id="mobileEcomPhar" name="mobileEcomPhar" pattern="[6-9][0-9]{9}" maxlength="10" required />
      <div class="error" id="mobileEcomPharError">Please enter valid 10-digit mobile number starting with 6-9</div>
      <label for="orderEcomPhar">Order Details</label>
      <textarea id="orderEcomPhar" name="orderEcomPhar" rows="3" required></textarea>
      <label for="addressEcomPhar">Delivery Address</label>
      <textarea id="addressEcomPhar" name="addressEcomPhar" rows="2" required></textarea>
      <button type="submit" class="submit-btn">Place Order via WhatsApp</button>
    </form>
  </div>

  <div id="cameraTab" class="ecomm-tab" style="display:none;">
    <h3>Camera Access</h3>
    <button onclick="openCamera()">Start Camera</button>
    <video id="video" autoplay></video>
  </div>
  <div id="mapsTab" class="ecomm-tab" style="display:none;">
    <h3>Location Map</h3>
    <div id="map"></div>
  </div>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Events & Catering Section -->
<div id="events" class="section">
  <h2>Events & Catering</h2>
  <nav class="small-nav">
    <button class="selected" onclick="switchEventTab('package', this)">Package</button>
    <button onclick="switchEventTab('customized', this)">Customized</button>
    <button onclick="switchEventTab('premium', this)">Premium</button>
  </nav>
  <div id="packageTab" class="tab-content">
    <p>Choose your package and services.</p>
    <ul>
      <li>Silver: 50,000 - 1,00,000</li>
      <li>Gold: 1,00,000 - 3,00,000</li>
      <li>Diamond: 3,00,000 - 5,00,000</li>
      <li>Platinum: 5,00,000 - 8,00,000</li>
    </ul>
  </div>
  <div id="customizedTab" class="tab-content" style="display:none;">
    <p>Customize your event with various services.</p>
  </div>
  <div id="premiumTab" class="tab-content" style="display:none;">
    <p>Premium services will be available soon.</p>
  </div>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Courier & Ride Booking -->
<div id="courier" class="section">
  <h2>Courier & Ride Booking</h2>
  <form id="courierForm">
    <label for="nameCourier">Name</label>
    <input type="text" id="nameCourier" name="nameCourier" required />
    <label for="mobileCourier">Mobile Number</label>
    <input type="tel" id="mobileCourier" name="mobileCourier" pattern="[6-9][0-9]{9}" maxlength="10" required />
    <div class="error" id="mobileCourierError">Please enter valid 10-digit mobile number starting with 6-9</div>
    <label for="detailsCourier">Courier Details</label>
    <textarea id="detailsCourier" name="detailsCourier" rows="3" required></textarea>
    <button type="submit" class="submit-btn">Send Request via WhatsApp</button>
  </form>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Job Consultancy -->
<div id="job" class="section">
  <h2>Job Consultancy & Services</h2>
  <form id="jobForm">
    <label for="nameJob">Name</label>
    <input type="text" id="nameJob" name="nameJob" required />
    <label for="mobileJob">Mobile Number</label>
    <input type="tel" id="mobileJob" name="mobileJob" pattern="[6-9][0-9]{9}" maxlength="10" required />
    <div class="error" id="mobileJobError">Please enter valid 10-digit mobile number starting with 6-9</div>
    <label for="detailsJob">Job Inquiry Details</label>
    <textarea id="detailsJob" name="detailsJob" rows="3" required></textarea>
    <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
  </form>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Loans & Insurance -->
<div id="loans" class="section">
  <h2>Loans & Insurance</h2>
  <form id="loansForm">
    <label for="nameLoans">Name</label>
    <input type="text" id="nameLoans" name="nameLoans" required />
    <label for="mobileLoans">Mobile Number</label>
    <input type="tel" id="mobileLoans" name="mobileLoans" pattern="[6-9][0-9]{9}" maxlength="10" required />
    <div class="error" id="mobileLoansError">Please enter valid 10-digit mobile number starting with 6-9</div>
    <label for="detailsLoans">Loan or Insurance Inquiry</label>
    <textarea id="detailsLoans" name="detailsLoans" rows="3" required></textarea>
    <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
  </form>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Tours & Travels -->
<div id="tours" class="section">
  <h2>Tours & Travels</h2>
  <form id="toursForm">
    <label for="nameTours">Name</label>
    <input type="text" id="nameTours" name="nameTours" required />
    <label for="mobileTours">Mobile Number</label>
    <input type="tel" id="mobileTours" name="mobileTours" pattern="[6-9][0-9]{9}" maxlength="10" required />
    <div class="error" id="mobileToursError">Please enter valid 10-digit mobile number starting with 6-9</div>
    <label for="detailsTours">Tour Inquiry Details</label>
    <textarea id="detailsTours" name="detailsTours" rows="3" required></textarea>
    <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
  </form>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Real Estate & Construction -->
<div id="realestate" class="section">
  <h2>Real Estate & Construction</h2>
  <form id="realestateForm">
    <label for="nameRE">Name</label>
    <input type="text" id="nameRE" name="nameRE" required />
    <label for="mobileRE">Mobile Number</label>
    <input type="tel" id="mobileRE" name="mobileRE" pattern="[6-9][0-9]{9}" maxlength="10" required />
    <div class="error" id="mobileREError">Please enter valid 10-digit mobile number starting with 6-9</div>
    <label for="detailsRE">Real Estate Inquiry Details</label>
    <textarea id="detailsRE" name="detailsRE" rows="3" required></textarea>
    <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
  </form>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Investment & Business -->
<div id="investment" class="section">
  <h2>Investment & Business</h2>
  <form id="investmentForm">
    <label for="nameInv">Name</label>
    <input type="text" id="nameInv" name="nameInv" required />
    <label for="mobileInv">Mobile Number</label>
    <input type="tel" id="mobileInv" name="mobileInv" pattern="[6-9][0-9]{9}" maxlength="10" required />
    <div class="error" id="mobileInvError">Please enter valid 10-digit mobile number starting with 6-9</div>
    <label for="detailsInv">Investment Inquiry Details</label>
    <textarea id="detailsInv" name="detailsInv" rows="3" required></textarea>
    <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
  </form>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Home Services -->
<div id="homeservices" class="section">
  <h2>Home Services</h2>
  <form id="homeSvcForm">
    <label for="nameHome">Name</label>
    <input type="text" id="nameHome" name="nameHome" required />
    <label for="mobileHome">Mobile Number</label>
    <input type="tel" id="mobileHome" name="mobileHome" pattern="[6-9][0-9]{9}" maxlength="10" required />
    <div class="error" id="mobileHomeError">Please enter valid 10-digit mobile number starting with 6-9</div>
    <label for="detailsHome">Service Inquiry Details</label>
    <textarea id="detailsHome" name="detailsHome" rows="3" required></textarea>
    <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
  </form>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<script>
function showSection(id) {
  document.getElementById('dashboard').style.display = 'none';
  document.querySelectorAll('.section').forEach(sec => {
    sec.classList.remove('active');
  });
  document.getElementById(id).classList.add('active');
}

function backToDashboard() {
  document.getElementById('dashboard').style.display = 'grid';
  document.querySelectorAll('.section').forEach(sec => {
    sec.classList.remove('active');
  });
}

// Tab switching for E-commerce subcategories:
function switchEcommTab(tabId, button) {
  const parent = button.parentNode;
  Array.from(parent.children).forEach(btn => btn.classList.remove('selected'));
  button.classList.add('selected');

  const tabs = document.querySelectorAll('.ecomm-tab');
  tabs.forEach(tab => tab.style.display = 'none');
  document.getElementById(tabId + 'Tab').style.display = 'block';

  if(tabId === 'camera') openCamera();
  else stopCamera();

  if(tabId === 'maps') initMap();
}

// Tab switching for Events & Catering:
function switchEventTab(tabId, button) {
  const parent = button.parentNode;
  Array.from(parent.children).forEach(btn => btn.classList.remove('selected'));
  button.classList.add('selected');

  ['packageTab', 'customizedTab', 'premiumTab'].forEach(id => {
    document.getElementById(id).style.display = (id === tabId + 'Tab') ? 'block' : 'none';
  });
}

// Camera functions
let cameraStream = null;
function openCamera() {
  const video = document.getElementById('video');
  if(navigator.mediaDevices && navigator.mediaDevices.getUserMedia){
    navigator.mediaDevices.getUserMedia({video: true}).then(stream => {
      cameraStream = stream;
      video.srcObject = stream;
    }).catch(err => alert('Unable to access camera: ' + err));
  } else {
    alert('Camera not supported.');
  }
}
function stopCamera() {
  if(cameraStream){
    cameraStream.getTracks().forEach(track => track.stop());
    cameraStream = null;
  }
}

// Google Maps Init (Hyderabad center)
let mapInitialized = false;
function initMap() {
  if(mapInitialized) return;
  mapInitialized = true;
  const mapDiv = document.getElementById('map');
  if(!mapDiv) return;
  const hyderabad = {lat: 17.3850, lng: 78.4867};
  const map = new google.maps.Map(mapDiv, {
    zoom: 12,
    center: hyderabad
  });
  new google.maps.Marker({position: hyderabad, map: map});
}

// Mobile validation helper
function validateMobile(input, errorElem) {
  const regex = /^[6-9][0-9]{9}$/;
  if(!regex.test(input.value)) {
    errorElem.style.display = 'block';
    return false;
  } else {
    errorElem.style.display = 'none';
    return true;
  }
}

// Attach form submit handlers to open WhatsApp with prefilled messages
['ecommerceGroceriesForm', 'ecommerceFoodForm', 'ecommercePharmacyForm', 'courierForm', 'jobForm', 'loansForm', 'toursForm', 'realestateForm', 'investmentForm', 'homeSvcForm'].forEach(formId => {
  const form = document.getElementById(formId);
  form.onsubmit = function(e){
    e.preventDefault();

    const name = this.querySelector('input[type=text]').value.trim();
    const mobileInput = this.querySelector('input[type=tel]');
    const mobile = mobileInput.value.trim();
    const errorElem = this.querySelector('.error');
    const valid = validateMobile(mobileInput, errorElem);
    if(!valid) return;

    const details = this.querySelector('textarea').value.trim();

    const prefixMap = {
      ecommerceGroceriesForm: 'E-commerce Groceries Order',
      ecommerceFoodForm: 'E-commerce Food Order',
      ecommercePharmacyForm: 'E-commerce Pharmacy Order',
      courierForm: 'Courier & Ride Booking Request',
      jobForm: 'Job Consultancy Inquiry',
      loansForm: 'Loans & Insurance Inquiry',
      toursForm: 'Tours & Travels Booking',
      realestateForm: 'Real Estate & Construction Inquiry',
      investmentForm: 'Investment & Business Inquiry',
      homeSvcForm: 'Home Service Inquiry'
    };

    const prefix = prefixMap[formId] || 'Inquiry';

    const message = encodeURIComponent(`${prefix}\nName: ${name}\nMobile: ${mobile}\nDetails: ${details}`);

    window.open('https://wa.me/918977143043?text=' + message, '_blank');
  }
});
</script>

<script async defer src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap"></script>
</body>
</html>
