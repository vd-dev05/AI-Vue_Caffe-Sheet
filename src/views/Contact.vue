<template>
  <div class="bg-amber-50 min-h-screen">
    <div class="container mx-auto py-12 px-6">
      <h1 class="text-4xl font-bold mb-8 text-center">Delivery & Contact</h1>
      
      <div class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-12">
        <div class="bg-white rounded-lg shadow-lg p-8">
          <h2 class="text-2xl font-bold mb-6 text-amber-900">Delivery Information</h2>
          
          <div class="mb-6">
            <h3 class="font-bold text-lg mb-3">Delivery Hours</h3>
            <ul class="space-y-2 text-gray-700">
              <li class="flex justify-between">
                <span>Monday - Friday</span>
                <span>7:00 AM - 9:00 PM</span>
              </li>
              <li class="flex justify-between">
                <span>Saturday - Sunday</span>
                <span>8:00 AM - 10:00 PM</span>
              </li>
            </ul>
          </div>
          
          <div class="mb-6">
            <h3 class="font-bold text-lg mb-3">Delivery Fees</h3>
            <ul class="space-y-2 text-gray-700">
              <li class="flex justify-between">
                <span>Under 2 km</span>
                <span>Free</span>
              </li>
              <li class="flex justify-between">
                <span>2-5 km</span>
                <span>10K</span>
              </li>
              <li class="flex justify-between">
                <span>Over 5 km</span>
                <span>15K</span>
              </li>
            </ul>
          </div>
          
          <div>
            <h3 class="font-bold text-lg mb-3">Delivery Partners</h3>
            <div class="flex space-x-4">
              <div class="bg-gray-100 p-2 rounded">
                <img src="https://via.placeholder.com/60x30?text=Grab" alt="Grab" class="h-6">
              </div>
              <div class="bg-gray-100 p-2 rounded">
                <img src="https://via.placeholder.com/60x30?text=GoJek" alt="GoJek" class="h-6">
              </div>
              <div class="bg-gray-100 p-2 rounded">
                <img src="https://via.placeholder.com/60x30?text=Delivery" alt="Local Delivery" class="h-6">
              </div>
            </div>
          </div>
        </div>
        
        <div class="bg-white rounded-lg shadow-lg p-8">
          <h2 class="text-2xl font-bold mb-6 text-amber-900">Contact Us</h2>
          
          <form class="space-y-4">
            <div>
              <label for="name" class="block text-gray-700 mb-1">Name</label>
              <input type="text" id="name" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500">
            </div>
            
            <div>
              <label for="email" class="block text-gray-700 mb-1">Email</label>
              <input type="email" id="email" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500">
            </div>
            
            <div>
              <label for="message" class="block text-gray-700 mb-1">Message</label>
              <textarea id="message" rows="4" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500"></textarea>
            </div>
            
            <button type="submit" class="bg-amber-900 text-white py-2 px-4 rounded-md hover:bg-amber-800 transition duration-200">
              Send Message
            </button>
          </form>
          
          <div class="mt-8 pt-6 border-t border-gray-200">
            <h3 class="font-bold text-lg mb-3">Find Us</h3>
            <p class="text-gray-700 mb-4">123 Coffee Street, District 1, Ho Chi Minh City</p>
            
            <div class="flex items-center space-x-4 text-gray-700">
              <div>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                </svg>
              </div>
              <span>+84 123 456 789</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactPage'
}
</script> 