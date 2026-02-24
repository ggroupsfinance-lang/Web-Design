// main.js — Global Theme Sync (Home + Services pages)

document.addEventListener("DOMContentLoaded", () => {
  const body = document.body;
  const toggleBtn = document.getElementById("themeToggle");

  // 1. Read saved theme from localStorage
  const savedTheme = localStorage.getItem("theme");

  // 2. Apply theme to body
  if (savedTheme === "dark") {
    body.classList.add("dark");
  } else {
    body.classList.remove("dark");
  }

  // 3. Set toggle icon correctly (VERY IMPORTANT)
  if (toggleBtn) {
    toggleBtn.textContent = body.classList.contains("dark") ? "☀️" : "🌙";

    // 4. Toggle theme on click
    toggleBtn.addEventListener("click", () => {
      body.classList.toggle("dark");

      const isDark = body.classList.contains("dark");
      localStorage.setItem("theme", isDark ? "dark" : "light");

      // Update icon immediately
      toggleBtn.textContent = isDark ? "☀️" : "🌙";
    });
  }
});
