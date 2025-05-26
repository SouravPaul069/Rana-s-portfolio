<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Rana Paul Portfolio</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
  
    tailwind.config = {
      darkMode: 'class',
    };
  </script>
  <style>
 
    @keyframes slideDown {
      0% { opacity: 0; transform: translateY(-30px); }
      100% { opacity: 1; transform: translateY(0); }
    }
    .slide-down {
      animation: slideDown 1s ease forwards;
    }

    @keyframes slideInLeft {
      0% { opacity: 0; transform: translateX(-100px); }
      100% { opacity: 1; transform: translateX(0); }
    }
    @keyframes slideInRight {
      0% { opacity: 0; transform: translateX(100px); }
      100% { opacity: 1; transform: translateX(0); }
    }
    .slide-left, .slide-right {
      opacity: 0;
      transition: all 0.7s ease;
    }
    .slide-left.active {
      animation: slideInLeft 0.7s forwards;
    }
    .slide-right.active {
      animation: slideInRight 0.7s forwards;
    }

    html {
      transition: background-color 0.5s, color 0.5s;
    }
  </style>
</head>
<body class="bg-white text-gray-900 dark:bg-gray-900 dark:text-white transition-colors duration-500">

  <button
    id="darkModeToggle"
    class="fixed top-4 right-4 px-4 py-2 bg-gray-200 dark:bg-gray-800 text-gray-900 dark:text-white rounded shadow transition"
  >
    Dark Mode On
  </button>

  <header class="text-center mt-16 mb-10">
    <h1 class="text-4xl font-bold slide-down">Rana Paul</h1>
    <p class="text-lg mt-2 font-semibold">Political Science Student</p>
    <p class="text-sm text-gray-600 dark:text-gray-400">Gobordanga Hindu College</p>
  </header>

  <section class="max-w-3xl mx-auto px-4 mb-16 slide-left">
    <h2 class="text-2xl font-semibold mb-4 border-b border-gray-300 dark:border-gray-700">About Me</h2>
    <p>
      I am Rana Paul, a dedicated Political Science student at Gobordanga Hindu College. Passionate about understanding political systems and governance, I aspire to contribute to society through insightful analysis and active participation.
    </p>
  </section>

  <section class="max-w-3xl mx-auto px-4 mb-16 slide-right" style="font-family: 'SolaimanLipi', Arial, sans-serif; font-size: 1.1rem;">
    <h2 class="text-2xl font-semibold mb-4 border-b border-gray-300 dark:border-gray-700">রাজনৈতিক ভাষণ</h2>
    <p>
      "জনগণের ক্ষমতা তাদের ঐক্য এবং সচেতনতা থেকে আসে। আমাদের উচিত ঐক্যবদ্ধ হয়ে দেশের উন্নয়নে কাজ করা।"
    </p>
  </section>

  <section class="max-w-3xl mx-auto px-4 mb-16 slide-left">
    <h2 class="text-2xl font-semibold mb-4 border-b border-gray-300 dark:border-gray-700">Projects</h2>
    <ul class="list-disc list-inside space-y-2">
      <li>Research Paper on Governance Models.</li>
      <li>Community Awareness Campaign for Youth Participation.</li>
      <li>College Political Debates and Events Organizer.</li>
    </ul>
  </section>

  <div class="flex justify-center space-x-6 mb-4">
    <a href="https://wa.me/919339066171" target="_blank" class="text-xl hover:text-green-400"><i class="fab fa-whatsapp"></i></a>
    <a href="https://www.instagram.com/its_your_rana?igsh=ZXE3YXF2dTlmN3k1" target="_blank" class="text-xl hover:text-pink-400"><i class="fab fa-instagram"></i></a>
    <a href="https://www.linkedin.com/in/rana-paul10?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank" class="text-xl hover:text-blue-300"><i class="fab fa-linkedin"></i></a>
  </div>
  <footer class="text-center text-sm text-gray-500 dark:text-gray-400 pb-4">
    © 2025 Created by Sourav Paul. All Rights Reserved.
  </footer>

  <script>
    const toggleBtn = document.getElementById("darkModeToggle");
    const htmlEl = document.documentElement;

    function updateButtonText() {
      toggleBtn.textContent = htmlEl.classList.contains("dark") ? "Dark Mode Off" : "Dark Mode On";
    }

    toggleBtn.addEventListener("click", () => {
      htmlEl.classList.toggle("dark");
      updateButtonText();
    });

    updateButtonText();

    const slideElements = document.querySelectorAll(".slide-left, .slide-right");

    function isInViewport(el) {
      const rect = el.getBoundingClientRect();
      return rect.top <= (window.innerHeight || document.documentElement.clientHeight) - 100;
    }

    function checkSlides() {
      slideElements.forEach(el => {
        if (isInViewport(el)) {
          el.classList.add("active");
        }
      });
    }

    window.addEventListener("scroll", checkSlides);
    window.addEventListener("load", checkSlides);
  </script>

 
  <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js"></script>
</body>
</html>
