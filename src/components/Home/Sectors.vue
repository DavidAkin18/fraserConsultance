<template>
  <section id="sectors" class="px-4 md:px-16 py-6">
    <div class="container mx-auto">
      <h2 class="text-3xl font-bold text-center mb-8">
        What sectors of the economy do we serve?
      </h2>

      <!-- Mobile Carousel -->
      <div class="relative mt-10 overflow-scroll lg:hidden">
        <!-- Carousel Container -->
        <div
          class="flex gap-1 transition-transform duration-500 ease-in-out"
          :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
        >
          <div
            v-for="(sector, index) in sectors"
            :key="index"
            class="min-w-full rounded-lg relative group hover:scale-105 transition-all duration-300"
          >
            <router-link :to="sector.link">
              <div
                class="w-full h-64 bg-cover bg-center rounded-lg"
                :style="{ backgroundImage: `url(${sector.image})` }"
              >
                <div
                  class="absolute inset-0 rounded-lg px-4 bg-[#1B3228] bg-opacity-40 flex items-center justify-center"
                >
                  <p class="text-2xl font-bold text-white text-center">
                    {{ sector.name }}
                  </p>
                </div>
              </div>
            </router-link>
          </div>
        </div>

        <!-- Navigation Buttons -->
        <!-- <button
          @click="prev"
          class="absolute md:hidden left-0 top-1/2 transform -translate-y-1/2 bg-[#F1BF98] px-1 py-0.5 rounded-full shadow-lg text-gray-700 hover:bg-gray-200"
        >
        ←
        </button>
        <button
          @click="next"
          class="absolute md:hidden right-0 top-1/2 transform -translate-y-1/2  bg-[#F1BF98] px-1 py-0.5  rounded-full shadow-lg text-gray-700 hover:bg-gray-200"
        >
        →
        </button> -->

        <!-- Dot Indicators -->
        
      </div>
      <div class="flex  justify-center mt-4">
          <span
            v-for="(sector, index) in sectors"
            :key="index"
            @click="goToImage(index)"
            class="mx-1 cursor-pointer text-2xl"
            :class="{
              'text-gray-400': currentIndex !== index,
              'text-[#1B3228]': currentIndex === index,
            }"
          >
            <i
              class="ri-checkbox-blank-circle-fill"
              :class="{
                'text-gray-400': currentIndex !== index,
                'text-[#1B3228]': currentIndex === index,
              }"
            ></i>
          </span>
        </div>

      <!-- Larger Screen Carousel -->
      <div class="relative gap-2 bg-white mt-10 overflow-scroll hidden lg:block">
        <!-- Carousel Container -->
        <div
          class="flex transition-transform duration-500 ease-in-out"
          :style="{ transform: `translateX(-${currentIndexDesktop * 33.33}%)` }"
        >
          <div
            v-for="(sector, index) in sectors"
            :key="index"
            class="w-1/3 flex-shrink-0 relative group hover:scale-105 transition-all duration-300 px-4"
          >
            <router-link :to="sector.link">
              <div
                class="w-full h-64 bg-cover bg-center rounded-lg"
                :style="{ backgroundImage: `url(${sector.image})` }"
              >
                <div
                  class="absolute inset-0 bg-opacity-40 flex items-center justify-center"
                >
                  <p class="text-2xl font-bold text-white text-center">
                    {{ sector.name }}
                  </p>
                </div>
              </div>
            </router-link>
          </div>
        </div>

        <!-- Navigation Buttons -->
        <!-- <button
          @click="prevDesktop"
          class="absolute left-0 top-1/2 -translate-y-1/2 text-white bg-[#F1BF98] hover:bg-[#1B3228]/80 text-4xl px-4 py-2 rounded-full shadow-lg"
        >
          ‹
        </button>
        <button
          @click="nextDesktop"
          class="absolute right-0 top-1/2 -translate-y-1/2 text-white bg-[#F1BF98] hover:bg-[#1B3228]/80 text-4xl px-4 py-2 rounded-full shadow-lg"
        >
          ›
        </button> -->
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SectorsCarousel",
  data() {
    return {
      currentIndex: 0, // For mobile carousel
      currentIndexDesktop: 0, // For desktop carousel
      sectors: [
        {
          name: "OIL & GAS",
          image:
            "https://eco-cdn.iqpc.com/eco/images/channel_content/images/offshore_platform.webp",
          link: "/oil-gas",
        },
        {
          name: "AVIATION",
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR3uWzQM_PhE6MWbkfBprWlAdcrGo4LJnKSJA&s",
          link: "/aviation",
        },
        {
          name: "BLUE ECONOMY",
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQMMCLQ4XnM9kM5HZp3cJUR42bAxud1qsbd4g&s",
          link: "/blue-economy",
        },
        {
          name: "CONSTRUCTION",
          image:
            "https://ucarecdn.com/95f9cb0c-26a6-46f1-8c33-21634a3cc5fb/",
          link: "/construction",
        },
        {
          name: "AGRICULTURE",
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTWEeYG-uGlCj-D5dSUG-DWC1jE3iVI-RF0Gw&s",
          link: "/agriculture",
        },
        {
          name: "FINANCE",
          image:
            "https://www.infosysbpm.com/content/dam/infosys-bpm/en/blogs/images/financial-service-trends-medium.jpg",
          link: "/finance",
        },
      ],
    };
  },
  mounted() {
    // Auto-slide for mobile
    setInterval(this.next, 5000);
    // Auto-slide for desktop
    setInterval(this.nextDesktop, 5000);
  },
  methods: {
    prev() {
      this.currentIndex =
        this.currentIndex === 0 ? this.sectors.length - 1 : this.currentIndex - 1;
    },
    next() {
      this.currentIndex =
        this.currentIndex === this.sectors.length - 1 ? 0 : this.currentIndex + 1;
    },
    prevDesktop() {
      this.currentIndexDesktop =
        this.currentIndexDesktop === 0
          ? Math.ceil(this.sectors.length / 1) - 1
          : this.currentIndexDesktop - 1;
    },
    nextDesktop() {
      this.currentIndexDesktop =
        this.currentIndexDesktop === Math.ceil(this.sectors.length / 1) - 1
          ? 0
          : this.currentIndexDesktop + 1;
    },
    goToImage(index) {
      this.currentIndex = index;
    },
  },
};
</script>

<style scoped>
/* Common Styles */
.h-64 {
  height: 16rem;
}

.bg-cover {
  background-size: cover;
}

.bg-center {
  background-position: center;
}

button {
  font-size: 2rem;
  transition: background-color 0.3s ease;
}

/* Hover effect on carousel items */
.group:hover .bg-cover {
  filter: brightness(70%);
}

button:hover {
  background-color: #1b3228;
}

/* Dot Indicator Styles */
.text-gray-400 {
  color: #9ca3af;
}



.text-gray-700 {
  color: #374151;
}

/* Dot indicator animation */
.ri-checkbox-blank-circle-fill {
  transition: transform 0.3s ease-in-out;
}

.ri-checkbox-blank-circle-fill:hover {
  transform: scale(1.2);
}
</style>
