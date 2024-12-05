<template>
  <section id="about" class="py-20 bg-[#1B3228] text-white">
    <div class="container mx-auto text-center px-4 md:px-12">
      <h2 class="text-3xl font-bold mb-6">About Fraser Consulting</h2>
      
      <!-- Introduction Paragraph -->
      <p class="text-lg mb-8">
        <strong>Fraser Consulting</strong> is a dynamic and experienced firm dedicated to providing exceptional solutions across various industries. With a strong foundation in professionalism, integrity, and strategic thinking, we are committed to delivering exceptional results for our clients.
      </p>
      
      <!-- Specialization List -->
      <h3 class="text-2xl font-semibold mb-4">Our Specializations</h3>
      <ul class="list-disc list-inside text-lg space-y-2 text-left mx-auto max-w-2xl">
        <li>International Consulting</li>
        <li>Contract & Payment Facilitation</li>
        <li>Claims Expertise</li>
        <li>Construction Economics & Estimation</li>
        <li>Contract Administration</li>
        <li>Project Management</li>
      </ul>
      
      <!-- Industry Sectors List -->
      <h3 class="text-2xl font-semibold mt-8 mb-4">Industries We Serve</h3>
      <ul class="list-disc list-inside text-lg space-y-2 text-left mx-auto max-w-2xl">
        <li>Oil & Gas</li>
        <li>Aviation</li>
        <li>Blue Economy</li>
        <li>Construction</li>
        <li>Agriculture</li>
        <li>Finance</li>
      </ul>
      
      <!-- Final Paragraph -->
      <p class="text-lg mt-8 mb-4">
        Whether you need assistance with complex financial matters, project management, or strategic consulting, Fraser Consulting is your trusted partner. We are here to provide guidance and ensure your business achieves its goals.
      </p>

      <p class="text-lg">
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
  background-color: #1B3228; /* Dark green background */
}

section#about p {
  color: white; /* Ensures text is readable on dark background */
}

/* Heading and Subheading Styling */
section#about h2 {
  color: white;
  font-size: 2.25rem;
  font-weight: 700;
}

section#about h3 {
  color: #A8DADC; /* Light teal for subheadings */
  font-size: 1.75rem;
  font-weight: 600;
}

/* Bullet List Styling */
section#about ul {
  list-style-type: disc;
  color: #E9F1F4; /* Soft off-white text color for readability */
  margin-left: 2rem; /* Indentation for lists */
}

/* Responsive Styling */
@media (max-width: 768px) {
  section#about h2 {
    font-size: 2rem;
  }
  
  section#about h3 {
    font-size: 1.5rem;
  }

  section#about p, section#about ul {
    font-size: 1rem;
  }
}
</style>
