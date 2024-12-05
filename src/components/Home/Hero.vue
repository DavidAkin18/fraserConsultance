<template>
  <section
    class="relative bg-cover bg-center w-full min-h-[500px] flex items-center justify-center px-4 md:px-16 py-14 lg:py-28"
    style="background-image: url('https://media.istockphoto.com/id/1365436734/photo/group-of-business-persons-talking-in-the-office.jpg?s=612x612&w=0&k=20&c=HMfrS47_CcQK8UTUegQNKlzmoenMLTPdm17uuJoNUw4=');"
  >
    <!-- Overlay for better text readability -->
    <div class="absolute inset-0 bg-[#1B3228] opacity-60 backdrop-blur-sm"></div>

    <!-- Content Section -->
    <div class="relative z-10 text-center text-white max-w-4xl">
      <p class="text-4xl md:text-6xl font-bold uppercase bg-clip-text text-transparent bg-gradient-to-r from-[#ffffff] to-[#ffffff]">
        FRASER CONSULTING
      </p>
      <h2 class="text-2xl md:text-3xl font-semibold mt-4 text-white">
        Ultimate Solutions for Modern Businesses
      </h2>

      <div class="text-lg mt-8 text-white">
        International Consultants. Contract & Payment Facilitators. Claims Experts. Construction Economists & Estimators. 
        Contract Administrators. Project Management. OIL & GAS. AVIATION. BLUE ECONOMY. CONSTRUCTION. AGRICULTURE. FINANCE.
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style scoped>
/* Tailwind-based styles ensure responsiveness; no additional styles needed here. */
</style>
