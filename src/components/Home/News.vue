<template>
  <section class="px-4 md:px-16 py-14 lg:py-28  bg-gray-100">
    <div class="container mx-auto text-center">
      <h1 class="text-2xl font-light">Fraser Consulting</h1>
      <h2 class="text-4xl font-bold">Latest News</h2>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-10">
        <!-- News Item 1 -->
        <a href="#" class="bg-white rounded-lg shadow-md p-6 hover:shadow-lg transition-shadow duration-300">
          <img 
            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQrI9hSB66LK1mMHBoDldPNXZ8FgO3GZezVHQ&s" 
            alt="Business Agility" 
            class="w-full h-48 object-cover rounded-lg mb-4" 
          />
          <h3 class="text-lg font-bold mb-4">25.01.24 / Business Consulting</h3>
          <h4 class="text-xl font-semibold mb-2">Building business agility begins with culture</h4>
          <p class="text-gray-600">Brief summary of the news article.</p>
          <p class="text-blue-500 hover:underline mt-2">Read more →</p>
        </a>

        <!-- News Item 2 -->
        <a href="#" class="bg-white rounded-lg shadow-md p-6 hover:shadow-lg transition-shadow duration-300">
          <img 
            src="https://cdn.punchng.com/wp-content/uploads/2023/06/16145643/press.jpg" 
            alt="Protecting Profits" 
            class="w-full h-48 object-cover rounded-lg mb-4" 
          />
          <h3 class="text-lg font-bold mb-4">25.01.24 / Business Consulting</h3>
          <h4 class="text-xl font-semibold mb-2">Strategies to protect your profits</h4>
          <p class="text-gray-600">Brief summary of the news article.</p>
          <p class="text-blue-500 hover:underline mt-2">Read more →</p>
        </a>

        <!-- News Item 3 -->
        <a href="#" class="bg-white rounded-lg shadow-md p-6 hover:shadow-lg transition-shadow duration-300">
          <img 
            src="https://www.channelstv.com/wp-content/uploads/2024/08/tinubu-cng-2.jpg" 
            alt="Cost Efficiency" 
            class="w-full h-48 object-cover rounded-lg mb-4" 
          />
          <h3 class="text-lg font-bold mb-4">25.01.24 / Business Consulting</h3>
          <h4 class="text-xl font-semibold mb-2">We Bring Flexibility & Cost Efficiency</h4>
          <p class="text-gray-600">Brief summary of the news article.</p>
          <p class="text-blue-500 hover:underline mt-2">Read more →</p>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'NewsSection',
};
</script>

<style scoped>
/* Add some hover effects for links */
a:hover {
  text-decoration: none;
}

img {
  border-radius: 0.5rem;
}
</style>
