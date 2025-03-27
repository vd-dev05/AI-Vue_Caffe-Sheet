<template>
  <div class="bg-amber-50 min-h-screen">
    <div class="container mx-auto py-12 px-6">
      <h1 class="text-4xl font-bold mb-8 text-center">About Us</h1>
      
      <div class="bg-white rounded-lg shadow-lg p-8 max-w-3xl mx-auto">
        <div class="mb-8">
          <h2 class="text-2xl font-bold mb-4 text-amber-900">Our Story</h2>
          <p class="text-gray-700 mb-4">
            Caffe Sheet was established in 2023 with a simple mission: to provide high-quality coffee that enhances productivity and brightens your day. What started as a small coffee stand has grown into a beloved destination for coffee enthusiasts.
          </p>
          <p class="text-gray-700">
            We source our beans directly from sustainable farms around the world, ensuring that every cup not only tastes exceptional but also supports ethical farming practices.
          </p>
        </div>
        
        <div class="mb-8">
          <h2 class="text-2xl font-bold mb-4 text-amber-900">Our Philosophy</h2>
          <p class="text-gray-700">
            We believe that a great cup of coffee is more than just a beverage – it's a moment of pleasure, a productivity booster, and sometimes the highlight of your day. That's why we pay attention to every detail, from bean selection to the final pour.
          </p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          <div class="text-center">
            <div class="bg-amber-100 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-amber-900" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z" />
              </svg>
            </div>
            <h3 class="font-bold text-lg mb-2">Quality</h3>
            <p class="text-gray-600">Premium beans, expertly roasted</p>
          </div>
          
          <div class="text-center">
            <div class="bg-amber-100 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-amber-900" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v13m0-13V6a2 2 0 112 2h-2zm0 0V5.5A2.5 2.5 0 109.5 8H12zm-7 4h14M5 12a2 2 0 110-4h14a2 2 0 110 4M5 12v7a2 2 0 002 2h10a2 2 0 002-2v-7" />
              </svg>
            </div>
            <h3 class="font-bold text-lg mb-2">Sustainability</h3>
            <p class="text-gray-600">Ethically sourced and eco-friendly</p>
          </div>
          
          <div class="text-center">
            <div class="bg-amber-100 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-amber-900" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.828 14.828a4 4 0 01-5.656 0M9 10h.01M15 10h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="font-bold text-lg mb-2">Community</h3>
            <p class="text-gray-600">Creating connections through coffee</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutPage'
}
</script> 