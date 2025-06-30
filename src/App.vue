<template>
  <div id="app">
    <BabylonExample />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import BabylonExample from "./components/BabylonExample.vue";

export default defineComponent({
  name: "App",
  components: {
    BabylonExample,
  },
});
</script>

<style>
:root {
  --primary: #6366f1;
  --secondary: #8b5cf6;
  --accent: #ec4899;
  --text: #2c3e50;
  --light: #f8fafc;
  --dark: #1e293b;
  --success: #10b981;
  --warning: #f59e0b;
  --danger: #ef4444;
}
* {
  background-color: rgb(171, 214, 215);
}

/* Strictly preserved original #app styles */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: midnightblue;
  margin-top: 60px;
}

/* Your original canvas styles - completely unchanged */
canvas {
  width: 70%;
  height: 70%;
}

/* Enhanced styles for other elements below */
body {
  background-color: #f9fafb;
  margin: 0;
  line-height: 1.6;
}

/* Typography enhancements */
h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: 700;
  line-height: 1.2;
  margin: 1.5rem 0 1rem;
}

h1 {
  font-size: 2.5rem;
  background: linear-gradient(90deg, var(--primary), var(--accent));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

h2 {
  font-size: 2rem;
  border-bottom: 2px solid var(--primary);
  padding-bottom: 0.5rem;
  display: inline-block;
}

/* Button styles */
button {
  background: linear-gradient(135deg, var(--primary), var(--secondary));
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  border-radius: 8px;
  cursor: pointer;
  font-weight: 600;
  transition: all 0.3s ease;
  margin: 0.5rem;
}

button:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Form elements */
input,
textarea,
select {
  padding: 0.75rem;
  margin: 0.5rem 0;
  border: 1px solid var(--border);
  border-radius: 6px;
  transition: all 0.3s ease;
}

input:focus {
  outline: none;
}

/* Utility classes */
.text-center {
  text-align: center;
}
.shadow {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
.rounded {
  border-radius: 8px;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  #app {
    margin-top: 40px;
    padding: 0 1rem;
  }

  h1 {
    font-size: 2rem;
  }

  /* Canvas dimensions remain exactly as specified */
}
</style>
