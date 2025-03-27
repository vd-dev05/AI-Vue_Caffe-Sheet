<template>
  <div class="bg-amber-50 min-h-screen">
    <header class="container mx-auto py-4 px-6 flex justify-between items-center">
      <div class="flex items-center">
        <div class="w-8 h-8 bg-orange-500 rounded-full flex items-center justify-center mr-2">
          <span class="text-white font-bold">C</span>
        </div>
        <span class="font-bold">Caffe Sheet</span>
      </div>
      <nav class="hidden md:flex space-x-6">
        <router-link to="/about" class="font-medium">About us</router-link>
        <router-link to="/menu" class="font-medium">Our Product</router-link>
        <router-link to="/contact" class="font-medium">Delivery</router-link>
      </nav>
      <div class="flex items-center">
        <div class="relative mr-4">
          <input type="text" placeholder="Search..." class="pl-8 pr-2 py-1 rounded-full border border-gray-300">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 absolute left-2 top-2 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
          </svg>
        </div>
        <button class="bg-white p-2 rounded-full">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
          </svg>
        </button>
      </div>
    </header>

    <main class="container mx-auto px-6 py-12">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
        <div>
          <h1 class="text-4xl font-bold mb-4">Enjoy your <span class="text-orange-500">coffee</span><br>before your activity</h1>
          <p class="text-gray-600 mb-8">Boost your productivity and build your mood with a glass of coffee in the morning</p>
          <div class="flex space-x-4">
            <button class="bg-amber-900 text-white px-4 py-2 rounded-full flex items-center hover:bg-amber-800 transition-all duration-300 transform hover:scale-105 active:scale-95 shadow-md hover:shadow-lg">
              Order now
              <span class="bg-white text-amber-900 ml-2 w-5 h-5 rounded-full flex items-center justify-center text-xs">→</span>
            </button>
            <router-link to="/menu" class="text-gray-600 hover:text-amber-900 transition-colors duration-300 flex items-center hover:translate-x-1 transform">
              More menu
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
              </svg>
            </router-link>
          </div>
        </div>
        <div class="relative">
          <div class="bg-amber-900 rounded-full h-80 w-80 mx-auto flex items-center justify-center relative overflow-hidden">
            <img src="https://images.unsplash.com/photo-1497636577773-f1231844b336?ixlib=rb-1.2.1&auto=format&fit=crop&w=300&q=80" alt="Coffee cup" class="h-60 w-60 object-cover z-10 shadow-lg transform hover:scale-105 transition-transform duration-300">
            
            <!-- Floating badges -->
            <div class="absolute top-2 right-6 bg-white py-1 px-3 rounded-full shadow-lg animate-float" style="animation-delay: 0.2s;">
              <div class="flex items-center">
                <span class="text-amber-900 font-bold mr-1">4.8</span>
                <span class="text-yellow-500">★</span>
              </div>
            </div>
            
            <div class="absolute top-16 -left-5 bg-white py-1 px-4 rounded-full shadow-lg animate-float" style="animation-delay: 0.5s;">
              <span class="font-medium">Cappuccino</span>
            </div>
            
            <div class="absolute bottom-10 left-10 bg-white py-1 px-4 rounded-full shadow-lg animate-float" style="animation-delay: 0.8s;">
              <span class="font-medium">18K</span>
            </div>
          </div>
          
          <!-- Coffee beans scattered around with animation -->
          <div class="absolute top-0 left-0 animate-bounce delay-100 opacity-80 text-2xl">☕</div>
          <div class="absolute bottom-0 right-0 animate-bounce delay-300 opacity-80 text-2xl">☕</div>
          <div class="absolute top-1/4 right-1/4 animate-bounce delay-200 opacity-80 text-2xl">☕</div>
          <div class="absolute bottom-1/3 left-1/4 animate-bounce delay-150 opacity-80 text-2xl">☕</div>
          <div class="absolute bottom-1/2 right-1/3 animate-bounce delay-250 opacity-80 text-2xl">☕</div>
        </div>
      </div>

      <!-- Popular Now Section -->
      <div class="mt-24 mb-12 relative">
        <!-- Coffee beans scattered around with animation -->
        <div class="absolute -top-10 left-0 animate-bounce delay-150 opacity-80 text-2xl">☕</div>
        <div class="absolute -top-5 right-1/4 animate-bounce delay-200 opacity-80 text-2xl">☕</div>
        <div class="absolute -top-8 right-10 animate-bounce delay-300 opacity-80 text-2xl">☕</div>
        
        <h2 class="text-2xl font-bold mb-8">
          Popular Now
        </h2>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          <!-- Card 1: Vanilla Latte -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover-grow">
            <div class="relative h-48 overflow-hidden">
              <div class="absolute top-2 left-2 bg-white px-2 py-1 rounded-full text-xs z-10 font-medium">4.9 ★</div>
              <img src="https://images.unsplash.com/photo-1541167760496-1628856ab772?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Vanilla Latte" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center">
                <h3 class="font-bold text-lg">Vanilla Latte</h3>
                <span class="font-bold text-amber-900">21K</span>
              </div>
              <div class="flex justify-between items-center mt-3">
                <div class="flex space-x-2">
                  <span class="bg-gray-100 text-gray-600 px-3 py-1 rounded-full text-xs">Hot</span>
                  <span class="bg-gray-100 text-gray-600 px-3 py-1 rounded-full text-xs">Cold</span>
                </div>
                <button class="bg-amber-500 p-2 rounded-full hover:bg-amber-600 transition-colors duration-300 active:scale-95 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
          
          <!-- Card 2: Espresso -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover-grow">
            <div class="relative h-48 overflow-hidden">
              <div class="absolute top-2 left-2 bg-white px-2 py-1 rounded-full text-xs z-10 font-medium">4.7 ★</div>
              <img src="https://images.unsplash.com/photo-1541167760496-1628856ab772?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Espresso" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center">
                <h3 class="font-bold text-lg">Espresso</h3>
                <span class="font-bold text-amber-900">12K</span>
              </div>
              <div class="flex justify-between items-center mt-3">
                <div class="flex space-x-2">
                  <span class="bg-gray-100 text-gray-600 px-3 py-1 rounded-full text-xs">Hot</span>
                </div>
                <button class="bg-amber-500 p-2 rounded-full hover:bg-amber-600 transition-colors duration-300 active:scale-95 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
          
          <!-- Card 3: Hazelnut Latte -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover-grow">
            <div class="relative h-48 overflow-hidden">
              <div class="absolute top-2 left-2 bg-white px-2 py-1 rounded-full text-xs z-10 font-medium">4.8 ★</div>
              <img src="https://images.unsplash.com/photo-1541167760496-1628856ab772?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Hazelnut Latte" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center">
                <h3 class="font-bold text-lg">Hazelnut Latte</h3>
                <span class="font-bold text-amber-900">23K</span>
              </div>
              <div class="flex justify-between items-center mt-3">
                <div class="flex space-x-2">
                  <span class="bg-gray-100 text-gray-600 px-3 py-1 rounded-full text-xs">Hot</span>
                  <span class="bg-gray-100 text-gray-600 px-3 py-1 rounded-full text-xs">Cold</span>
                </div>
                <button class="bg-amber-500 p-2 rounded-full hover:bg-amber-600 transition-colors duration-300 active:scale-95 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
        </div>
        
        <div class="flex justify-center mt-8">
          <div class="h-1 w-20 bg-blue-500 mx-1 rounded-full"></div>
          <div class="h-1 w-10 bg-gray-300 mx-1 rounded-full"></div>
          <div class="h-1 w-10 bg-gray-300 mx-1 rounded-full"></div>
        </div>
      </div>

      <!-- Delivery Service Section -->
      <div class="mt-24 mb-12 relative">
        <h2 class="text-2xl font-bold mb-8 text-center">
          How to use delivery <span class="text-amber-600">service</span>
        </h2>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center max-w-4xl mx-auto">
          <!-- Step 1 -->
          <div class="flex flex-col items-center">
            <div class="bg-amber-100 rounded-full p-6 mb-4 w-28 h-28 flex items-center justify-center">
              <img src="https://cdn-icons-png.flaticon.com/512/3361/3361135.png" alt="Choose Coffee" class="w-16 h-16">
            </div>
            <h3 class="font-bold mb-2">Choose your coffee</h3>
            <p class="text-gray-600 text-sm">There are 20+ coffees for you</p>
          </div>

          <!-- Step 2 -->
          <div class="flex flex-col items-center">
            <div class="bg-amber-100 rounded-full p-6 mb-4 w-28 h-28 flex items-center justify-center">
              <img src="https://cdn-icons-png.flaticon.com/512/2771/2771401.png" alt="We delivery" class="w-16 h-16">
            </div>
            <h3 class="font-bold mb-2">We delivery it to you</h3>
            <p class="text-gray-600 text-sm">Choose delivery service</p>
          </div>

          <!-- Step 3 -->
          <div class="flex flex-col items-center">
            <div class="bg-amber-100 rounded-full p-6 mb-4 w-28 h-28 flex items-center justify-center">
              <img src="https://cdn-icons-png.flaticon.com/512/924/924514.png" alt="Enjoy coffee" class="w-16 h-16">
            </div>
            <h3 class="font-bold mb-2">Enjoy your coffee</h3>
            <p class="text-gray-600 text-sm">Choose delivery service</p>
          </div>
        </div>
      </div>

      <!-- About Us Section -->
      <div class="mt-24 mb-12">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
          <div class="relative">
            <img src="https://images.unsplash.com/photo-1541167760496-1628856ab772?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Coffee" class="rounded-lg shadow-xl transform -rotate-2 hover-grow">
          </div>
          
          <div>
            <h2 class="text-2xl font-bold mb-4">About <span class="text-amber-600">us</span></h2>
            
            <h3 class="text-lg font-bold mb-3">We provide quality coffee, and ready to deliver.</h3>
            
            <p class="text-gray-600 mb-6">
              We are specialized in providing high-quality coffee. Our delicious drinks, our most products is made with a secret recipe and available in stores worldwide.
            </p>
            
            <button class="bg-amber-900 text-white px-4 py-2 rounded-full hover:bg-amber-800 transition-colors duration-300 transform active:scale-95">
              Get your coffee
            </button>
          </div>
        </div>
      </div>

      <!-- Special Menu Section -->
      <div class="mt-24 mb-12 relative">
        <h2 class="text-2xl font-bold mb-8">
          Special menu for you
        </h2>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          <!-- Menu Item 1: Sandwich -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover-grow">
            <div class="relative h-40 overflow-hidden">
              <div class="absolute top-2 left-2 bg-white px-2 py-1 rounded-full text-xs z-10 font-medium">4.8 ★</div>
              <img src="https://images.unsplash.com/photo-1528735602780-2552fd46c7af?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Sandwich" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center mb-1">
                <h3 class="font-bold">Sandwich</h3>
                <span class="font-bold text-amber-900">12 K</span>
              </div>
              <p class="text-gray-500 text-xs mb-3">Bread with meat and vegetables</p>
              <div class="flex justify-end">
                <button class="bg-amber-500 p-2 rounded-full hover:bg-amber-600 transition-colors duration-300 active:scale-95 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
          
          <!-- Menu Item 2: Hot Milk -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover-grow">
            <div class="relative h-40 overflow-hidden">
              <div class="absolute top-2 left-2 bg-white px-2 py-1 rounded-full text-xs z-10 font-medium">4.7 ★</div>
              <img src="https://images.unsplash.com/photo-1517578239113-b03992dcdd25?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Hot Milk" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center mb-1">
                <h3 class="font-bold">Hot Milk</h3>
                <span class="font-bold text-amber-900">12 K</span>
              </div>
              <p class="text-gray-500 text-xs mb-3">Hot milk with less sugar</p>
              <div class="flex justify-end">
                <button class="bg-amber-500 p-2 rounded-full hover:bg-amber-600 transition-colors duration-300 active:scale-95 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
          
          <!-- Menu Item 3: Coffee Ice Cream -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover-grow">
            <div class="relative h-40 overflow-hidden">
              <div class="absolute top-2 left-2 bg-white px-2 py-1 rounded-full text-xs z-10 font-medium">4.9 ★</div>
              <img src="https://images.unsplash.com/photo-1579954115545-a95591f28bfc?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Coffee Ice Cream" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center mb-1">
                <h3 class="font-bold">Coffee Ice Cream</h3>
                <span class="font-bold text-amber-900">12 K</span>
              </div>
              <p class="text-gray-500 text-xs mb-3">Coffee with ice cream vanilla</p>
              <div class="flex justify-end">
                <button class="bg-amber-500 p-2 rounded-full hover:bg-amber-600 transition-colors duration-300 active:scale-95 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
          
          <!-- Menu Item 4: Cappuccino -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover-grow">
            <div class="relative h-40 overflow-hidden">
              <div class="absolute top-2 left-2 bg-white px-2 py-1 rounded-full text-xs z-10 font-medium">4.8 ★</div>
              <img src="https://images.unsplash.com/photo-1572442388796-11668a67e53d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Cappuccino" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center mb-1">
                <h3 class="font-bold">Cappuccino</h3>
                <span class="font-bold text-amber-900">12 K</span>
              </div>
              <p class="text-gray-500 text-xs mb-3">Hot cappuccino</p>
              <div class="flex justify-end">
                <button class="bg-amber-500 p-2 rounded-full hover:bg-amber-600 transition-colors duration-300 active:scale-95 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
          
          <!-- Menu Item 5: Moccacino -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover-grow">
            <div class="relative h-40 overflow-hidden">
              <div class="absolute top-2 left-2 bg-white px-2 py-1 rounded-full text-xs z-10 font-medium">4.8 ★</div>
              <img src="https://images.unsplash.com/photo-1541167760496-1628856ab772?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Moccacino" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center mb-1">
                <h3 class="font-bold">Moccacino</h3>
                <span class="font-bold text-amber-900">12 K</span>
              </div>
              <p class="text-gray-500 text-xs mb-3">Hot moccacino</p>
              <div class="flex justify-end">
                <button class="bg-amber-500 p-2 rounded-full hover:bg-amber-600 transition-colors duration-300 active:scale-95 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
          
          <!-- Menu Item 6: Waffle Ice Cream -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover-grow">
            <div class="relative h-40 overflow-hidden">
              <div class="absolute top-2 left-2 bg-white px-2 py-1 rounded-full text-xs z-10 font-medium">4.9 ★</div>
              <img src="https://images.unsplash.com/photo-1563805042-7684c019e1cb?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Waffle Ice Cream" class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center mb-1">
                <h3 class="font-bold">Waffle Ice Cream</h3>
                <span class="font-bold text-amber-900">12 K</span>
              </div>
              <p class="text-gray-500 text-xs mb-3">Waffle with ice cream</p>
              <div class="flex justify-end">
                <button class="bg-amber-500 p-2 rounded-full hover:bg-amber-600 transition-colors duration-300 active:scale-95 transform">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Testimonials Section -->
      <div class="mt-24 mb-12 relative bg-amber-100 py-12 px-6 rounded-xl">
        <h2 class="text-2xl font-bold mb-8">
          What they say about us
        </h2>
        
        <p class="text-gray-600 mb-8 max-w-lg">
          We always provide the best service and always maintain the quality of coffee
        </p>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          <!-- Testimonial 1 -->
          <div class="bg-white rounded-lg shadow-md p-6 hover-grow">
            <div class="flex items-center mb-4">
              <img src="https://randomuser.me/api/portraits/women/79.jpg" alt="Naura" class="w-12 h-12 rounded-full mr-4 object-cover">
              <div>
                <h3 class="font-bold">Naura</h3>
                <div class="flex text-yellow-500">
                  <span>★</span>
                  <span>★</span>
                  <span>★</span>
                  <span>★</span>
                  <span>★</span>
                </div>
              </div>
            </div>
            <p class="text-gray-600 text-sm">
              "I really love the cappuccino, the coffee was very smooth."
            </p>
          </div>
          
          <!-- Testimonial 2 -->
          <div class="bg-white rounded-lg shadow-md p-6 hover-grow">
            <div class="flex items-center mb-4">
              <img src="https://randomuser.me/api/portraits/men/52.jpg" alt="Alex" class="w-12 h-12 rounded-full mr-4 object-cover">
              <div>
                <h3 class="font-bold">Alex</h3>
                <div class="flex text-yellow-500">
                  <span>★</span>
                  <span>★</span>
                  <span>★</span>
                  <span>★</span>
                  <span>★</span>
                </div>
              </div>
            </div>
            <p class="text-gray-600 text-sm">
              "This coffee shop is in a convenient location and the staff is great!"
            </p>
          </div>
          
          <!-- Testimonial 3 -->
          <div class="bg-white rounded-lg shadow-md p-6 hover-grow">
            <div class="flex items-center mb-4">
              <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Kevin" class="w-12 h-12 rounded-full mr-4 object-cover">
              <div>
                <h3 class="font-bold">Kevin</h3>
                <div class="flex text-yellow-500">
                  <span>★</span>
                  <span>★</span>
                  <span>★</span>
                  <span>★</span>
                  <span>★</span>
                </div>
              </div>
            </div>
            <p class="text-gray-600 text-sm">
              "The coffee was amazing! I can't wait to come back!"
            </p>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: 'HomePage'
}
</script>

<style scoped>
/* Thêm hiệu ứng delay cho animation bounce */
.delay-100 {
  animation-delay: 0.1s;
}
.delay-150 {
  animation-delay: 0.15s;
}
.delay-200 {
  animation-delay: 0.2s;
}
.delay-250 {
  animation-delay: 0.25s;
}
.delay-300 {
  animation-delay: 0.3s;
}
</style> 