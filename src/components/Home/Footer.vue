<template>
  <footer class="bg-[#1B3228] text-white px-4 md:px-16 py-14 lg:py-28 ">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row justify-between items-start">
        <!-- Left Column -->
        <div class="flex flex-col items-start mb-8 md:mb-0 w-full md:w-1/3">
          <img src="../../assets/images/fclogo.png" alt="Your Logo" class="w-40 mb-6">
          <p class="text-base mb-4 md:w-4/5">
            Velit facilisis senectus vel elit elementum. Consequat vel arcu feugiat dui eu tempor pretium at porta. Duis pellentesque sagittis.
          </p>
          <div class="flex space-x-4 mt-4">
            <a href="#" class="text-white hover:text-blue-500 transition-colors">
              <i class="ri-facebook-fill text-2xl"></i>
            </a>
            <a href="#" class="text-white hover:text-blue-500 transition-colors">
              <i class="ri-twitter-fill text-2xl"></i>
            </a>
            <a href="#" class="text-white hover:text-blue-500 transition-colors">
              <i class="ri-instagram-fill text-2xl"></i>
            </a>
            <a href="#" class="text-white hover:text-blue-500 transition-colors">
              <i class="ri-linkedin-fill text-2xl"></i>
            </a>
          </div>
          <p class="mt-4 text-lg font-semibold">Subscribe to Us</p>
        </div>

        <!-- Center Column - Services and Useful Links -->
        <div class="grid grid-cols-2 md:grid-cols-3 gap-8 w-full md:w-2/3">
          <div class="flex flex-col">
            <h3 class="text-lg font-bold mb-4">Services</h3>
            <ul class="space-y-2">
              <li><a href="#" class="hover:underline text-base">Marketing Strategy</a></li>
              <li><a href="#" class="hover:underline text-base">Financial Management</a></li>
              <li><a href="#" class="hover:underline text-base">Business Strategy</a></li>
              <li><a href="#" class="hover:underline text-base">Sales and Marketing</a></li>
              <li><a href="#" class="hover:underline text-base">Human Resources</a></li>
            </ul>
          </div>

          <div class="flex flex-col">
            <h3 class="text-lg font-bold mb-4">Useful Links</h3>
            <ul class="space-y-2">
              <li><a href="#" class="hover:underline text-base">Home</a></li>
              <li><a href="#" class="hover:underline text-base">Services</a></li>
              <li><a href="#" class="hover:underline text-base">News</a></li>
            </ul>
          </div>

          <div class="flex flex-col">   
            <h3 class="text-lg font-bold">Address</h3>
            <p class="text-base">
              <a href="https://www.google.com/maps?q=8592+Fairground+St,+Tallahassee,+FL+32303" target="_blank" class="text-gray-300 hover:text-white">8592 Fairground St, Tallahassee, FL 32303</a>
            </p>
            <h3 class="text-lg font-bold mt-4 mb-2">Email</h3>
            <p class="text-base">
              <a href="mailto:fraserconsult2000@qmail.com" class="text-gray-300 hover:underline">fraserconsult2000@qmail.com</a>
            </p>
            <h3 class="text-lg font-bold mt-4 mb-2">Phone</h3>
            <p class="text-base">
              <a href="tel:+18632673634" class="text-gray-300 hover:underline">(+234) 802-291-2562</a>, 
              <a href="tel:+2348088811881" class="text-gray-300 hover:underline">(+234) 808-881-1881</a>,
              <a href="tel:+2348050515555" class="text-gray-300 hover:underline">(+234) 805-051-5555</a>,
              <a href="tel:+2349094666000" class="text-gray-300 hover:underline">(+234) 909-466-6000</a>
            </p>
          </div>
        </div>
      </div>

      <!-- Footer Bottom -->
      
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
/* Footer Styles */
footer {
  /* background-color: #657B65; */
  color: white;
}

footer a {
  transition: color 0.3s ease;
}

footer a:hover {
  color: #FFFFFF; /* Blue color for hover effect */
}

/* Social Icons */
footer .ri-facebook-fill,
footer .ri-twitter-fill,
footer .ri-instagram-fill,
footer .ri-linkedin-fill {
  transition: transform 0.3s ease;
}

footer .ri-facebook-fill:hover,
footer .ri-twitter-fill:hover,
footer .ri-instagram-fill:hover,
footer .ri-linkedin-fill:hover {
  transform: scale(1.2);
}

/* Button Hover Effects */
footer button:hover {
  background-color: #2563EB; /* Lighter blue on hover */
}

footer input:focus {
  border-color: #2563EB;
  outline: none;
}
</style>
