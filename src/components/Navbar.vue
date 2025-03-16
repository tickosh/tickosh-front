<script>
export default {
  name: "Navbar",
  data() {
    return {
      isMobileMenuOpen: false,
    };
  },
  methods: {
    toggleMobileMenu() {
      this.isMobileMenuOpen = !this.isMobileMenuOpen;
    },
    navigate(path) {
      this.$router.push(path);
    },
  },
};
</script>

<template>
  <nav class="bg-white shadow-lg">
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex justify-between items-center h-16">
        <!-- Logo -->
        <div class="flex items-center">
          <button
            @click="navigate('/')"
            class="text-xl font-bold text-gray-800"
          >
            Tickosh
          </button>
        </div>

        <!-- Navigation Links -->
        <div class="hidden md:flex items-center space-x-8">
          <button
            @click="navigate('/')"
            class="text-gray-600 hover:text-gray-900 transition duration-300"
          >
            Home
          </button>
          <button
            @click="navigate('/about')"
            class="text-gray-600 hover:text-gray-900 transition duration-300"
          >
            About
          </button>
          <button
            @click="navigate('/services')"
            class="text-gray-600 hover:text-gray-900 transition duration-300"
          >
            Services
          </button>
          <button
            @click="navigate('/contact')"
            class="text-gray-600 hover:text-gray-900 transition duration-300"
          >
            Contact
          </button>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden flex items-center">
          <button
            @click="toggleMobileMenu"
            class="outline-none mobile-menu-button"
          >
            <svg
              class="w-6 h-6 text-gray-500 hover:text-gray-900"
              fill="none"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div class="md:hidden" :class="{ hidden: !isMobileMenuOpen }">
      <button
        @click="navigate('/')"
        class="block w-full text-left py-2 px-4 text-sm hover:bg-gray-200"
      >
        Home
      </button>
      <button
        @click="navigate('/about')"
        class="block w-full text-left py-2 px-4 text-sm hover:bg-gray-200"
      >
        About
      </button>
      <button
        @click="navigate('/services')"
        class="block w-full text-left py-2 px-4 text-sm hover:bg-gray-200"
      >
        Services
      </button>
      <button
        @click="navigate('/contact')"
        class="block w-full text-left py-2 px-4 text-sm hover:bg-gray-200"
      >
        Contact
      </button>
    </div>
  </nav>
</template>
