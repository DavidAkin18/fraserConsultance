<template>
  <section id="about" class="py-14 lg:py-28  bg-gradient-to-b from-[#1B3228] to-[#243C34] text-white">
    <div class="container mx-auto px-4 md:px-12">
      <!-- Header Section -->
      <h2 class="text-4xl font-extrabold text-center mb-12">About Fraser Consulting</h2>

      <div class="flex flex-col md:flex-row items-center md:items-start gap-12">
        <!-- Left Section -->
        <div class="md:w-1/2 border border-[#F1BF98] text-left p-8 rounded-lg shadow-lg">
          <p class="text-xl leading-loose font-semibold mb-6">
            <strong>Fraser Consulting</strong> is a dynamic and experienced firm dedicated to providing exceptional solutions across various industries. With a strong foundation in professionalism, integrity, and strategic thinking, we are committed to delivering exceptional results for our clients.
          </p>
          <p class="text-lg leading-relaxed">
            Whether you need assistance with complex financial matters, project management, or strategic consulting, Fraser Consulting is your trusted partner. We are here to provide guidance and ensure your business achieves its goals.
          </p>
        </div>

        <!-- Vertical Divider -->
        <div class="hidden md:block h-auto w-px bg-gray-500"></div>

        <!-- Right Section -->
        <div class="md:w-1/2 flex flex-col gap-8">
          <!-- Specializations Box -->
          <div class="p-6  rounded-lg border border-[#F1BF98] shadow-lg hover:shadow-xl transition-shadow duration-300">
            <h3 class="text-2xl font-semibold text-[#FFFFFF] mb-4">Our Specializations</h3>
            <ul class="text-lg leading-relaxed space-y-4 text-left">
              <li class="flex items-center gap-3">
                <span class="text-[#1B3228] text-xl">📈</span> International Consulting
              </li>
              <li class="flex items-center gap-3">
                <span class="text-[#1B3228] text-xl">💳</span> Contract & Payment Facilitation
              </li>
              <li class="flex items-center gap-3">
                <span class="text-[#1B3228] text-xl">🛠️</span> Claims Expertise
              </li>
              <li class="flex items-center gap-3">
                <span class="text-[#1B3228] text-xl">🏗️</span> Construction Economics & Estimation
              </li>
              <li class="flex items-center gap-3">
                <span class="text-[#1B3228] text-xl">📜</span> Contract Administration
              </li>
              <li class="flex items-center gap-3">
                <span class="text-[#1B3228] text-xl">📊</span> Project Management
              </li>
            </ul>
          </div>

          <!-- Industries Box -->
          <div class="p-6  rounded-lg border border-[#F1BF98] shadow-xl hover:shadow-xl transition-shadow duration-300">
            <h3 class="text-2xl font-semibold text-[#FFFFFF] mb-4">Industries We Serve</h3>
            <div class="grid grid-cols-2 gap-4 text-left">
              <p class="flex items-center gap-3 hover:text-[#717568] transition-colors">
                <span class="text-[#1B3228] text-xl">🛢️</span> Oil & Gas
              </p>
              <p class="flex items-center gap-3 hover:text-[#717568] transition-colors">
                <span class="text-[#1B3228] text-xl">✈️</span> Aviation
              </p>
              <p class="flex items-center gap-3 hover:text-[#717568] transition-colors">
                <span class="text-[#1B3228] text-xl">🌊</span> Blue Economy
              </p>
              <p class="flex items-center gap-3 hover:text-[#717568] transition-colors">
                <span class="text-[#1B3228] text-xl">🏗️</span> Construction
              </p>
              <p class="flex items-center gap-3 hover:text-[#717568] transition-colors">
                <span class="text-[#1B3228] text-xl">🌾</span> Agriculture
              </p>
              <p class="flex items-center gap-3 hover:text-[#717568] transition-colors">
                <span class="text-[#1B3228] text-xl">💰</span> Finance
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Horizontal Divider -->
      <div class="my-12 border-t border-gray-500"></div>

      <!-- Closing Paragraph -->
      <p class="text-lg leading-relaxed text-center">
        <strong>Contact us today</strong> to explore how our expertise can elevate your business and drive success.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
/* General Section Styling */
section#about {
  background: linear-gradient(to bottom, #1B3228, #243C34);
}

/* Typography and Spacing */
section#about h2 {
  font-size: 2.5rem;
  font-weight: 800;
}

section#about h3 {
  font-size: 1.75rem;
  font-weight: 600;
}

section#about p {
  font-size: 1.125rem;
  line-height: 1.75rem;
}

section#about .container {
  max-width: 1200px;
}

/* Box Styling */
section#about .p-6 {
  padding: 1.5rem;
  transition: box-shadow 0.3s;
}

section#about .bg-[#F1BF98] {
  border-radius: 0.5rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

/* Icon Styling */
section#about span {
  font-size: 1.5rem;
  font-weight: bold;
}

/* Hover Effects */
section#about .hover\\:text-[#717568]:hover {
  color: #717568;
}

/* Divider Styling */
section#about .border-t {
  border-color: rgba(255, 255, 255, 0.3);
}

section#about .bg-gray-500 {
  background-color: rgba(255, 255, 255, 0.3);
}

/* Responsive Styling */
@media (max-width: 768px) {
  section#about h2 {
    font-size: 2rem;
  }

  section#about h3 {
    font-size: 1.5rem;
  }

  section#about p {
    font-size: 1rem;
  }

  section#about .grid {
    grid-template-columns: 1fr; /* Single column on smaller screens */
  }
}
</style>
