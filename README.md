# HEMOMATCH
class CustomFooter extends HTMLElement {
  connectedCallback() {
    this.attachShadow({ mode: 'open' });
    this.shadowRoot.innerHTML = `
      <style>
        .footer-link:hover {
          color: #dc2626;
        }
      </style>
      <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-4">
          <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
            <div>
              <h3 class="text-xl font-bold mb-4">Hemomatch</h3>
              <p class="text-gray-400">Connecting donors with recipients to save lives through blood compatibility.</p>
            </div>
            
            <div>
              <h4 class="font-bold mb-4">Quick Links</h4>
              <ul class="space-y-2">
                <li><a href="#login" class="footer-link text-gray-400 hover:text-white">Register</a></li>
                <li><a href="#compatibility-checker" class="footer-link text-gray-400 hover:text-white">Compatibility Check</a></li>
                <li><a href="#nearby" class="footer-link text-gray-400 hover:text-white">Find Donors</a></li>
                <li><a href="#" class="footer-link text-gray-400 hover:text-white">About Us</a></li>
              </ul>
            </div>
            
            <div>
              <h4 class="font-bold mb-4">Contact</h4>
              <ul class="space-y-2 text-gray-400">
                <li class="flex items-center space-x-2">
                  <i data-feather="mail"></i>
                  <span>contact@hemomatch.org</span>
                </li>
                <li class="flex items-center space-x-2">
                  <i data-feather="phone"></i>
                  <span>(555) 123-4567</span>
                </li>
                <li class="flex items-center space-x-2">
                  <i data-feather="map-pin"></i>
                  <span>123 Lifesaver Ave, Health City</span>
                </li>
              </ul>
            </div>
            
            <div>
              <h4 class="font-bold mb-4">Follow Us</h4>
              <div class="flex space-x-4">
                <a href="#" class="text-gray-400 hover:text-white">
                  <i data-feather="facebook"></i>
                </a>
                <a href="#" class="text-gray-400 hover:text-white">
                  <i data-feather="twitter"></i>
                </a>
                <a href="#" class="text-gray-400 hover:text-white">
                  <i data-feather="instagram"></i>
                </a>
                <a href="#" class="text-gray-400 hover:text-white">
                  <i data-feather="linkedin"></i>
                </a>
              </div>
              <p class="mt-4 text-gray-400 text-sm">© 2023 Hemomatch. All rights reserved.</p>
            </div>
          </div>
        </div>
      </footer>
    `;
  }
  class CustomNavbar extends HTMLElement {
  connectedCallback() {
    this.attachShadow({ mode: 'open' });
    this.shadowRoot.innerHTML = `
      <style>
        .nav-link:hover {
          color: #dc2626;
        }
        .nav-link:hover svg {
          stroke: #dc2626;
        }
      </style>
      <nav class="bg-white shadow-md">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
          <a href="/" class="flex items-center space-x-2">
            <div class="h-10 w-10 bg-red-600 rounded-full flex items-center justify-center text-white font-bold">H</div>
            <span class="text-xl font-bold text-gray-800">Hemomatch</span>
          </a>
          
          <div class="hidden md:flex space-x-8">
            <a href="#login" class="nav-link text-gray-700 hover:text-red-600 flex items-center space-x-1">
              <i data-feather="user"></i>
              <span>Login</span>
            </a>
            <a href="#compatibility-checker" class="nav-link text-gray-700 hover:text-red-600 flex items-center space-x-1">
              <i data-feather="droplet"></i>
              <span>Compatibility</span>
            </a>
            <a href="#nearby" class="nav-link text-gray-700 hover:text-red-600 flex items-center space-x-1">
              <i data-feather="map-pin"></i>
              <span>Nearby</span>
            </a>
            <a href="#" class="nav-link text-gray-700 hover:text-red-600 flex items-center space-x-1">
              <i data-feather="info"></i>
              <span>About</span>
            </a>
          </div>
          
          <button class="md:hidden focus:outline-none">
            <i data-feather="menu"></i>
          </button>
        </div>
      </nav>
    `;
  }
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hemomatch | Blood Compatibility Checker</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/feather-icons/dist/feather.min.js"></script>
    <script src="https://unpkg.com/feather-icons"></script>
    <script src="components/navbar.js"></script>
    <script src="components/footer.js"></script>
</head>
<body class="bg-gray-50">
    <custom-navbar></custom-navbar>
    
    <main class="container mx-auto px-4 py-8">
        <!-- Hero Section -->
        <section class="bg-red-600 text-white rounded-xl p-8 mb-12 shadow-lg">
            <div class="max-w-3xl mx-auto text-center">
                <h1 class="text-4xl md:text-5xl font-bold mb-4">Find Your Perfect Blood Match</h1>
                <p class="text-xl mb-8">Connect with compatible donors and save lives in your community</p>
                <a href="#compatibility-checker" class="bg-white text-red-600 font-bold py-3 px-8 rounded-full hover:bg-gray-100 transition duration-300 inline-block">Check Compatibility</a>
            </div>
        </section>

        <!-- Login/Registration Form -->
        <section id="login" class="bg-white rounded-xl shadow-md p-8 mb-12">
            <h2 class="text-2xl font-bold mb-6 text-gray-800">Join Our Lifesaving Community</h2>
            <form class="space-y-6">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <label for="email" class="block text-gray-700 mb-2">Email</label>
                        <input type="email" id="email" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-red-500">
                    </div>
                    <div>
                        <label for="password" class="block text-gray-700 mb-2">Password</label>
                        <input type="password" id="password" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-red-500">
                    </div>
                    <div>
                        <label for="age" class="block text-gray-700 mb-2">Age</label>
                        <input type="number" id="age" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-red-500">
                    </div>
                    <div>
                        <label for="phone" class="block text-gray-700 mb-2">Phone Number</label>
                        <input type="tel" id="phone" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-red-500">
                    </div>
                </div>
                
                <div class="space-y-4">
                    <div class="flex items-center">
                        <input type="checkbox" id="addiction" class="h-4 w-4 text-red-600 focus:ring-red-500 border-gray-300 rounded">
                        <label for="addiction" class="ml-2 block text-gray-700">Do you have any addiction?</label>
                    </div>
                    <div class="flex items-center">
                        <input type="checkbox" id="disease" class="h-4 w-4 text-red-600 focus:ring-red-500 border-gray-300 rounded">
                        <label for="disease" class="ml-2 block text-gray-700">Do you have any chronic disease?</label>
                    </div>
                </div>
                
                <div>
                    <label for="location" class="block text-gray-700 mb-2">Location</label>
                    <input type="text" id="location" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-red-500" placeholder="Enter your city or zip code">
                </div>
                
                <button type="submit" class="w-full bg-red-600 text-white py-3 px-4 rounded-lg hover:bg-red-700 transition duration-300 font-bold">Register Now</button>
            </form>
        </section>

        <!-- Compatibility Checker -->
        <section id="compatibility-checker" class="bg-white rounded-xl shadow-md p-8 mb-12">
            <h2 class="text-2xl font-bold mb-6 text-gray-800">Blood Compatibility Checker</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div>
                    <div class="space-y-4">
                        <div>
                            <label for="donor-blood" class="block text-gray-700 mb-2">Donor Blood Type</label>
                            <select id="donor-blood" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-red-500">
                                <option value="">Select blood type</option>
                                <option value="A+">A+</option>
                                <option value="A-">A-</option>
                                <option value="B+">B+</option>
                                <option value="B-">B-</option>
                                <option value="AB+">AB+</option>
                                <option value="AB-">AB-</option>
                                <option value="O+">O+</option>
                                <option value="O-">O-</option>
                            </select>
                        </div>
                        <div>
                            <label for="receiver-blood" class="block text-gray-700 mb-2">Receiver Blood Type</label>
                            <select id="receiver-blood" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-red-500 focus:border-red-500">
                                <option value="">Select blood type</option>
                                <option value="A+">A+</option>
                                <option value="A-">A-</option>
                                <option value="B+">B+</option>
                                <option value="B-">B-</option>
                                <option value="AB+">AB+</option>
                                <option value="AB-">AB-</option>
                                <option value="O+">O+</option>
                                <option value="O-">O-</option>
                            </select>
                        </div>
                        <button id="check-compatibility" class="bg-red-600 text-white py-3 px-6 rounded-lg hover:bg-red-700 transition duration-300 font-bold">Check Compatibility</button>
                    </div>
                    
                    <div id="result" class="mt-6 p-4 rounded-lg hidden">
                        <h3 class="text-xl font-bold mb-2">Compatibility Result</h3>
                        <p id="result-text"></p>
                    </div>
                </div>
                
                <div class="bg-gray-50 p-6 rounded-lg">
                    <h3 class="text-xl font-bold mb-4 text-gray-800">Blood Compatibility Basics</h3>
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-5 w-5 text-red-600 mt-1">
                                <i data-feather="check-circle"></i>
                            </div>
                            <p class="ml-3 text-gray-700">O- is the universal donor (can donate to anyone)</p>
                        </div>
                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-5 w-5 text-red-600 mt-1">
                                <i data-feather="check-circle"></i>
                            </div>
                            <p class="ml-3 text-gray-700">AB+ is the universal receiver (can receive from anyone)</p>
                        </div>
                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-5 w-5 text-red-600 mt-1">
                                <i data-feather="alert-triangle"></i>
                            </div>
                            <p class="ml-3 text-gray-700">Mismatched blood can cause severe immune reactions</p>
                        </div>
                        <div class="flex items-start">
                            <div class="flex-shrink-0 h-5 w-5 text-red-600 mt-1">
                                <i data-feather="heart"></i>
                            </div>
                            <p class="ml-3 text-gray-700">One donation can save up to 3 lives</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Nearby Hospitals & Donors -->
        <section id="nearby" class="bg-white rounded-xl shadow-md p-8 mb-12">
            <h2 class="text-2xl font-bold mb-6 text-gray-800">Nearby Resources</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div>
                    <h3 class="text-xl font-bold mb-4 text-gray-800">Hospitals with Blood Banks</h3>
                    <div class="space-y-4">
                        <div class="border border-gray-200 rounded-lg p-4 hover:shadow-md transition duration-300">
                            <div class="flex justify-between items-start">
                                <div>
                                    <h4 class="font-bold text-lg">City General Hospital</h4>
                                    <p class="text-gray-600">2.5 miles away</p>
                                </div>
                                <span class="bg-green-100 text-green-800 px-2 py-1 rounded-full text-sm">Open Now</span>
                            </div>
                            <p class="mt-2 text-gray-700">123 Medical Center Drive</p>
                            <p class="text-gray-700">(555) 123-4567</p>
                        </div>
                        <div class="border border-gray-200 rounded-lg p-4 hover:shadow-md transition duration-300">
                            <div class="flex justify-between items-start">
                                <div>
                                    <h4 class="font-bold text-lg">Red Cross Blood Center</h4>
                                    <p class="text-gray-600">4.1 miles away</p>
                                </div>
                                <span class="bg-green-100 text-green-800 px-2 py-1 rounded-full text-sm">Open Now</span>
                            </div>
                            <p class="mt-2 text-gray-700">456 Lifesaver Lane</p>
                            <p class="text-gray-700">(555) 987-6543</p>
                        </div>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-xl font-bold mb-4 text-gray-800">Available Donors</h3>
                    <div class="space-y-4">
                        <div class="border border-gray-200 rounded-lg p-4 hover:shadow-md transition duration-300">
                            <div class="flex justify-between items-start">
                                <div>
                                    <h4 class="font-bold text-lg">John D. (O+)</h4>
                                    <p class="text-gray-600">1.2 miles away</p>
                                </div>
                                <span class="bg-red-100 text-red-800 px-2 py-1 rounded-full text-sm">Available Today</span>
                            </div>
                            <p class="mt-2 text-gray-700">Last donated: 3 months ago</p>
                            <button class="mt-2 text-red-600 hover:text-red-800 font-medium">Contact Donor</button>
                        </div>
                        <div class="border border-gray-200 rounded-lg p-4 hover:shadow-md transition duration-300">
                            <div class="flex justify-between items-start">
                                <div>
                                    <h4 class="font-bold text-lg">Sarah M. (A-)</h4>
                                    <p class="text-gray-600">2.8 miles away</p>
                                </div>
                                <span class="bg-red-100 text-red-800 px-2 py-1 rounded-full text-sm">Available Today</span>
                            </div>
                            <p class="mt-2 text-gray-700">Last donated: 4 months ago</p>
                            <button class="mt-2 text-red-600 hover:text-red-800 font-medium">Contact Donor</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Educational Content -->
        <section class="bg-white rounded-xl shadow-md p-8 mb-12">
            <h2 class="text-2xl font-bold mb-6 text-gray-800">Why Blood Compatibility Matters</h2>
            <div class="space-y-6">
                <div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">The Science Behind Blood Types</h3>
                    <p class="text-gray-700">Blood types are determined by the presence or absence of certain antigens on red blood cells. The ABO system has four main blood types: A, B, AB, and O. The Rh factor (positive or negative) adds another layer of complexity. When incompatible blood types mix, the immune system attacks the foreign antigens, leading to potentially fatal reactions.</p>
                </div>
                <div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Consequences of Mismatched Blood</h3>
                    <p class="text-gray-700">Receiving incompatible blood can cause:</p>
                    <ul class="list-disc pl-5 mt-2 space-y-2 text-gray-700">
                        <li>Fever and chills</li>
                        <li>Kidney failure</li>
                        <li>Shock</li>
                        <li>Hemolysis (destruction of red blood cells)</li>
                        <li>Death in severe cases</li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">The Impact of Your Donation</h3>
                    <p class="text-gray-700">Every blood donation can save up to three lives. Your compatible blood could be the difference between life and death for:</p>
                    <ul class="list-disc pl-5 mt-2 space-y-2 text-gray-700">
                        <li>Accident victims</li>
                        <li>Cancer patients</li>
                        <li>Surgery patients</li>
                        <li>Newborns with complications</li>
                        <li>People with chronic illnesses</li>
                    </ul>
                </div>
            </div>
        </section>
    </main>

    <custom-footer></custom-footer>

    <script src="script.js"></script>
    <script>
        feather.replace();
    </script>
</body>
</html>
document.addEventListener('DOMContentLoaded', function() {
    // Blood compatibility checker logic
    const checkBtn = document.getElementById('check-compatibility');
    const resultDiv = document.getElementById('result');
    const resultText = document.getElementById('result-text');
    
    checkBtn.addEventListener('click', function() {
        const donorBlood = document.getElementById('donor-blood').value;
        const receiverBlood = document.getElementById('receiver-blood').value;
        
        if (!donorBlood || !receiverBlood) {
            alert('Please select both donor and receiver blood types');
            return;
        }
        
        // Basic compatibility logic (simplified)
        let isCompatible = false;
        let explanation = '';
        
        if (donorBlood === 'O-' && receiverBlood !== 'O-') {
            isCompatible = true;
            explanation = 'O- is the universal donor and can give to any blood type.';
        } else if (donorBlood === 'O+' && (receiverBlood === 'O+' || receiverBlood === 'A+' || receiverBlood === 'B+' || receiverBlood === 'AB+')) {
            isCompatible = true;
            explanation = 'O+ can donate to any positive blood type.';
        } else if (donorBlood === 'A-' && (receiverBlood === 'A-' || receiverBlood === 'A+' || receiverBlood === 'AB-' || receiverBlood === 'AB+')) {
            isCompatible = true;
            explanation = 'A- can donate to A and AB blood types (both + and -).';
        } else if (donorBlood === 'A+' && (receiverBlood === 'A+' || receiverBlood === 'AB+')) {
            isCompatible = true;
            explanation = 'A+ can donate to A+ and AB+ blood types.';
        } else if (donorBlood === 'B-' && (receiverBlood === 'B-' || receiverBlood === 'B+' || receiverBlood === 'AB-' || receiverBlood === 'AB+')) {
            isCompatible = true;
            explanation = 'B- can donate to B and AB blood types (both + and -).';
        } else if (donorBlood === 'B+' && (receiverBlood === 'B+' || receiverBlood === 'AB+')) {
            isCompatible = true;
            explanation = 'B+ can donate to B+ and AB+ blood types.';
        } else if (donorBlood === 'AB-' && (receiverBlood === 'AB-' || receiverBlood === 'AB+')) {
            isCompatible = true;
            explanation = 'AB- can donate to AB blood types (both + and -).';
        } else if (donorBlood === 'AB+' && receiverBlood === 'AB+') {
            isCompatible = true;
            explanation = 'AB+ can only donate to other AB+ recipients.';
        } else if (donorBlood === receiverBlood) {
            isCompatible = true;
            explanation = 'Same blood types are always compatible.';
        } else {
            isCompatible = false;
            explanation = 'These blood types are not compatible. Donating could cause severe immune reactions.';
        }
        
        // Display result
        resultDiv.className = isCompatible ? 
            'mt-6 p-4 rounded-lg bg-green-100 text-green-800 show' : 
            'mt-6 p-4 rounded-lg bg-red-100 text-red-800 show';
        
        resultText.innerHTML = `
            <p class="font-bold">${isCompatible ? '✅ Compatible' : '❌ Not Compatible'}</p>
            <p class="mt-2">${explanation}</p>
            ${!isCompatible ? '<p class="mt-2 font-medium">⚠️ Warning: Transfusing incompatible blood can be life-threatening.</p>' : ''}
        `;
    });
    
    // Smooth scrolling for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            document.querySelector(this.getAttribute('href')).scrollIntoView({
                behavior: 'smooth'
            });
        });
    });
});
/* Custom styles that extend Tailwind */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');

body {
    font-family: 'Poppins', sans-serif;
}

/* Animation for compatibility result */
@keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}

#result.show {
    animation: fadeIn 0.5s ease-out forwards;
    display: block !important;
}

/* Custom scrollbar */
::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-track {
    background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
    background: #dc2626;
    border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
    background: #b91c1c;
}

/* Pulse animation for important elements */
@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
}

.pulse {
    animation: pulse 2s infinite;
}




}

customElements.define('custom-footer', CustomFo
