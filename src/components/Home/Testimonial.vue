<template>
  <section class="bg-[#E1F4CB] px-4 md:px-16 py-6">
    <div class="container mx-auto">
      <h2 class="text-3xl font-bold text-center text-[#ffffff] mb-8">Testimonial</h2>
      <div class="relative">
        <!-- Scrollable Container -->
        <div
          ref="scrollContainer"
          class="flex overflow-x-auto no-scrollbar snap-x snap-mandatory gap-6 transition-all duration-500 ease-out"
        >
          <!-- Individual Review Cards -->
          <div
            v-for="(review, index) in reviews"
            :key="index"
            class="min-w-[300px] max-w-sm flex-shrink-0 bg-[#1B3228] rounded-lg shadow-lg p-6 snap-center"
          >
            <p class="text-[#ffffff] text-lg mb-4">{{ review.text }}</p>
            <div class="flex items-center">
              <div class="w-12 h-12 rounded-full bg-gray-300 flex items-center justify-center text-gray-600 font-bold text-lg">
                {{ review.initials }}
              </div>
              <div class="ml-4">
                <h3 class="text-white font-semibold">{{ review.name }}</h3>
                <p class="text-gray-300 text-sm">{{ review.location }}</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Navigation Arrows -->
        <button
          @click="scrollLeft"
          class="absolute md:hidden left-0 top-1/2 transform -translate-y-1/2 bg-white px-2 py-1 rounded-full shadow-lg text-gray-700 hover:bg-gray-200"
        >
          ←
        </button>
        <button
          @click="scrollRight"
          class="absolute md:hidden right-0 top-1/2 transform -translate-y-1/2 bg-white px-2 py-1 rounded-full shadow-lg text-gray-700 hover:bg-gray-200"
        >
          →
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      reviews: [
        {
          text: "This is the best service I’ve ever used!",
          initials: "JD",
          name: "John Doe",
          location: "New York, USA",
        },
        {
          text: "Fantastic quality and quick delivery!",
          initials: "SS",
          name: "Sarah Smith",
          location: "London, UK",
        },
        {
          text: "Absolutely loved the experience!",
          initials: "AK",
          name: "Alice Kim",
          location: "Seoul, South Korea",
        },
        {
          text: "Highly recommend it to anyone.",
          initials: "ML",
          name: "Michael Lee",
          location: "Toronto, Canada",
        },
        {
          text: "Great customer support and amazing product.",
          initials: "AB",
          name: "Amelia Brown",
          location: "Sydney, Australia",
        },
        {
          text: "Top-notch services and worth every penny.",
          initials: "RB",
          name: "Robert Black",
          location: "Berlin, Germany",
        },
        {
          text: "Exceeded my expectations in every way.",
          initials: "KP",
          name: "Karen Patel",
          location: "Mumbai, India",
        },
        {
          text: "Will definitely return for more!",
          initials: "JW",
          name: "James Wilson",
          location: "San Francisco, USA",
        },
      ],
      scrollDirection: 'right', // Track the scroll direction
    };
  },
  mounted() {
    // Wait for DOM updates and ensure scrollContainer is available
    this.$nextTick(() => {
      this.autoScroll();
    });
  },
  methods: {
    // Method to scroll the container to the left by 300px
    scrollLeft() {
      const container = this.$refs.scrollContainer;
      container.scrollBy({ left: -300, behavior: "smooth" });
    },

    // Method to scroll the container to the right by 300px
    scrollRight() {
      const container = this.$refs.scrollContainer;
      container.scrollBy({ left: 300, behavior: "smooth" });
    },

    // Method to automatically scroll forward and backward
    autoScroll() {
      // Start the interval only after ensuring the container is available
      const container = this.$refs.scrollContainer;

      if (!container) {
        console.error("Scroll container not found");
        return;
      }

      setInterval(() => {
        const containerWidth = container.scrollWidth;
        const scrollPosition = container.scrollLeft;
        const visibleWidth = container.clientWidth;

        // Check if we're at the end or beginning of the scroll container
        if (this.scrollDirection === 'right') {
          if (scrollPosition + visibleWidth >= containerWidth) {
            this.scrollDirection = 'left'; // Reverse the scroll direction
          } else {
            container.scrollBy({ left: 300, behavior: 'smooth' }); // Scroll right
          }
        } else if (this.scrollDirection === 'left') {
          if (scrollPosition <= 0) {
            this.scrollDirection = 'right'; // Reverse the scroll direction
          } else {
            container.scrollBy({ left: -300, behavior: 'smooth' }); // Scroll left
          }
        }
      }, 3000); // Change direction every 3 seconds
    },
  },
};
</script>

<style>
/* Hide scrollbar for a clean look */
.no-scrollbar::-webkit-scrollbar {
  display: none;
}
.no-scrollbar {
  -ms-overflow-style: none;
  scrollbar-width: none;
}

/* Adding smooth scroll effect */
.scroll-container {
  transition: transform 0.5s ease-out;
}
</style>
