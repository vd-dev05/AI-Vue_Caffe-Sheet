<template>
  <div class="bg-amber-50 min-h-screen">
    <div class="container mx-auto py-12 px-6">
      <h1 class="text-4xl font-bold mb-8 text-center">Our Menu</h1>
      
      <div class="max-w-4xl mx-auto">
        <!-- Categories -->
        <div class="flex flex-wrap justify-center mb-8">
          <button 
            v-for="(category, index) in categories" 
            :key="index"
            @click="activeCategory = category"
            :class="['px-4 py-2 mx-2 mb-2 rounded-full font-medium hover-grow', 
                    activeCategory === category ? 'bg-amber-900 text-white' : 'bg-white text-gray-700 hover:bg-amber-100 transition-colors duration-300']"
          >
            {{ category }}
          </button>
        </div>
        
        <!-- Products -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          <div v-for="(product, index) in filteredProducts" :key="index" class="bg-white rounded-lg shadow-md overflow-hidden hover-grow">
            <div class="h-48 overflow-hidden relative group cursor-pointer" @click="selectedProduct = product">
              <img :src="product.image" :alt="product.name" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
              <div class="absolute inset-0 bg-black bg-opacity-40 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                <span class="text-white font-medium px-3 py-1 rounded-full border border-white">View Details</span>
              </div>
              <div class="absolute top-2 right-2 bg-white px-2 py-1 rounded-full text-xs font-bold">
                {{ product.category }}
              </div>
            </div>
            <div class="p-4">
              <div class="flex justify-between items-center mb-2">
                <h3 class="font-bold text-lg">{{ product.name }}</h3>
                <div class="flex items-center">
                  <span class="text-yellow-500 mr-1">★</span>
                  <span>{{ product.rating }}</span>
                </div>
              </div>
              <p class="text-gray-600 text-sm mb-4">{{ product.description }}</p>
              <div class="flex justify-between items-center">
                <span class="font-bold text-amber-900">{{ product.price }}</span>
                <button @click="addToCart(product)" class="bg-amber-900 text-white px-3 py-1 rounded-full text-sm hover:bg-amber-800 transition-colors duration-300 transform active:scale-95 flex items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6" />
                  </svg>
                  Add to cart
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Product Detail Modal -->
    <div v-if="selectedProduct" class="fixed inset-0 flex items-center justify-center z-50 px-4">
      <div class="absolute inset-0 bg-black bg-opacity-70" @click="selectedProduct = null"></div>
      <div class="relative bg-white rounded-lg shadow-xl max-w-2xl w-full animate-float" style="animation-duration: 0.5s;">
        <button @click="selectedProduct = null" class="absolute top-4 right-4 text-gray-500 hover:text-gray-800">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
        
        <div class="flex flex-col md:flex-row">
          <div class="md:w-1/2">
            <img :src="selectedProduct.image" :alt="selectedProduct.name" class="w-full h-64 md:h-full object-cover">
          </div>
          <div class="md:w-1/2 p-6">
            <div class="flex justify-between items-center mb-2">
              <h2 class="text-2xl font-bold text-amber-900">{{ selectedProduct.name }}</h2>
              <div class="flex items-center">
                <span class="text-yellow-500 mr-1">★</span>
                <span>{{ selectedProduct.rating }}</span>
              </div>
            </div>
            
            <div class="mb-4">
              <span class="inline-block bg-amber-100 text-amber-800 px-2 py-1 rounded-full text-xs font-semibold">
                {{ selectedProduct.category }}
              </span>
            </div>
            
            <p class="text-gray-600 mb-6">{{ selectedProduct.description }}</p>
            
            <div class="mb-6">
              <h3 class="font-bold mb-2">Ingredients:</h3>
              <ul class="text-gray-600 text-sm space-y-1">
                <li v-for="(ingredient, i) in getIngredients(selectedProduct)" :key="i" class="flex items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 mr-2 text-green-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  {{ ingredient }}
                </li>
              </ul>
            </div>
            
            <div class="flex justify-between items-center">
              <div>
                <span class="text-gray-500 text-sm">Price</span>
                <p class="text-2xl font-bold text-amber-900">{{ selectedProduct.price }}</p>
              </div>
              
              <div class="flex items-center">
                <div class="flex items-center border border-gray-300 rounded-full overflow-hidden mr-2">
                  <button @click="quantity > 1 ? quantity-- : quantity" class="px-3 py-1 bg-gray-100 hover:bg-gray-200 focus:outline-none">-</button>
                  <span class="px-3">{{ quantity }}</span>
                  <button @click="quantity++" class="px-3 py-1 bg-gray-100 hover:bg-gray-200 focus:outline-none">+</button>
                </div>
                
                <button @click="addToCartAndClose()" class="bg-amber-900 text-white px-4 py-2 rounded-full hover:bg-amber-800 transition-colors duration-300 transform active:scale-95">
                  Add to cart
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MenuPage',
  data() {
    return {
      activeCategory: 'All',
      categories: ['All', 'Coffee', 'Non-Coffee', 'Pastries', 'Seasonal'],
      selectedProduct: null,
      quantity: 1,
      cart: [],
      products: [
        {
          name: 'Cappuccino',
          category: 'Coffee',
          price: '18K',
          rating: 4.8,
          description: 'Espresso with steamed milk and a deep layer of foam',
          image: 'https://images.unsplash.com/photo-1534778101976-62847782c213?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80'
        },
        {
          name: 'Latte',
          category: 'Coffee',
          price: '20K',
          rating: 4.7,
          description: 'Espresso with a large amount of steamed milk and light foam',
          image: 'https://images.unsplash.com/photo-1570968915860-54d5c301fa9f?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80'
        },
        {
          name: 'Americano',
          category: 'Coffee',
          price: '15K',
          rating: 4.5,
          description: 'Espresso diluted with hot water',
          image: 'https://images.unsplash.com/photo-1551030173-122aabc4489c?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80'
        },
        {
          name: 'Matcha Latte',
          category: 'Non-Coffee',
          price: '22K',
          rating: 4.6,
          description: 'Green tea powder whisked with steamed milk',
          image: 'https://images.unsplash.com/photo-1536256263959-770b48d82b0a?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80'
        },
        {
          name: 'Chocolate Croissant',
          category: 'Pastries',
          price: '15K',
          rating: 4.8,
          description: 'Buttery croissant filled with rich chocolate',
          image: 'https://images.unsplash.com/photo-1549903072-7e6e0bdb049d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80'
        },
        {
          name: 'Pumpkin Spice Latte',
          category: 'Seasonal',
          price: '24K',
          rating: 4.9,
          description: 'Espresso with steamed milk, pumpkin, cinnamon, and nutmeg',
          image: 'https://images.unsplash.com/photo-1509042239860-f550ce710b93?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80'
        }
      ]
    }
  },
  computed: {
    filteredProducts() {
      if (this.activeCategory === 'All') {
        return this.products;
      }
      return this.products.filter(product => product.category === this.activeCategory);
    }
  },
  methods: {
    addToCart(product) {
      this.cart.push({
        ...product,
        quantity: 1
      });
      // Hiển thị thông báo thêm vào giỏ hàng
      alert(`Added ${product.name} to cart!`);
    },
    addToCartAndClose() {
      if (this.selectedProduct) {
        this.cart.push({
          ...this.selectedProduct,
          quantity: this.quantity
        });
        // Hiển thị thông báo thêm vào giỏ hàng
        alert(`Added ${this.quantity} ${this.selectedProduct.name} to cart!`);
        this.selectedProduct = null;
        this.quantity = 1;
      }
    },
    getIngredients(product) {
      // Mô phỏng dữ liệu thành phần
      const baseIngredients = {
        'Coffee': ['Coffee beans', 'Filtered water'],
        'Non-Coffee': ['Milk', 'Sweetener'],
        'Pastries': ['Flour', 'Butter', 'Sugar', 'Eggs'],
        'Seasonal': ['Seasonal ingredients']
      };
      
      const specificIngredients = {
        'Cappuccino': ['Espresso', 'Steamed milk', 'Milk foam'],
        'Latte': ['Espresso', 'Steamed milk'],
        'Americano': ['Espresso', 'Hot water'],
        'Matcha Latte': ['Matcha powder', 'Steamed milk', 'Sweetener'],
        'Chocolate Croissant': ['Croissant dough', 'Dark chocolate', 'Butter'],
        'Pumpkin Spice Latte': ['Espresso', 'Pumpkin spice syrup', 'Steamed milk', 'Cinnamon', 'Nutmeg']
      };
      
      return specificIngredients[product.name] || baseIngredients[product.category] || ['Water', 'Sugar', 'Coffee'];
    }
  }
}
</script>

<style scoped>
.hover-grow {
  transition: transform 0.3s ease;
}
.hover-grow:hover {
  transform: scale(1.03);
}

@keyframes modalIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-modal {
  animation: modalIn 0.3s ease-out forwards;
}
</style> 