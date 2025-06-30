<template>
  <div>
    <h3>Babylon Examples</h3>
    <canvas></canvas>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { BasicScene } from "@/BabylonExample/BasicScene";

export default defineComponent({
  name: "BabylonExample",
  mounted() {
    const canvas = document.querySelector("canvas")!;
    new BasicScene(canvas);
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* Base styles */
:root {
  --primary: #6366f1;
  --secondary: #8b5cf6;
  --accent: #ec4899;
  --text: #334155;
  --light: #f8fafc;
  --dark: #1e293b;
  --success: #10b981;
  --warning: #f59e0b;
  --danger: #ef4444;
}

body {
  font-family:
    "Inter",
    -apple-system,
    BlinkMacSystemFont,
    sans-serif;
  line-height: 1.6;
  color: var(--text);
  background-color: #f9fafb;
  padding: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

/* Typography */
h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: 700;
  line-height: 1.2;
  margin: 1.5rem 0 1rem;
  color: midnightblue;
}

h1 {
  font-size: 2.5rem;
  background: linear-gradient(90deg, var(--primary), var(--accent));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  margin-top: 0;
}

h2 {
  font-size: 2rem;
  border-bottom: 2px solid var(--primary);
  padding-bottom: 0.5rem;
}

h3 {
  font-size: 1.75rem;
}
h4 {
  font-size: 1.5rem;
}
h5 {
  font-size: 1.25rem;
}
h6 {
  font-size: 1rem;
}

p {
  margin-bottom: 1.25rem;
}

a {
  color: var(--primary);
  text-decoration: none;
  transition: all 0.2s ease;
  font-weight: 500;
}

a:hover {
  color: var(--accent);
  text-decoration: underline;
}

/* Canvas (original dimensions preserved) */
canvas {
  width: 70%;
  height: 70%;
  display: block;
  margin: 2rem auto;
  border-radius: 12px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
  background: linear-gradient(145deg, #f6f8fa, #e9ecef);
  transition: all 0.3s ease;
}

canvas:hover {
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.2);
  transform: translateY(-2px);
}

/* Buttons */
button,
.btn {
  background: linear-gradient(135deg, var(--primary), var(--secondary));
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  border-radius: 8px;
  cursor: pointer;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.3s ease;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

button:hover,
.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
  opacity: 0.9;
}

/* Forms */
input,
textarea,
select {
  width: 100%;
  padding: 0.75rem;
  margin: 0.5rem 0 1.5rem;
  border-radius: 8px;
  font-size: 1rem;
  transition: all 0.3s ease;
}

input:focus,
textarea:focus,
select:focus {
  outline: none;
  box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.2);
}

label {
  font-weight: 600;
  color: var(--dark);
}

/* Lists */
ul,
ol {
  margin-bottom: 1.5rem;
  padding-left: 1.5rem;
}

li {
  margin-bottom: 0.5rem;
}

/* Tables */
table {
  width: 100%;
  border-collapse: collapse;
  margin: 1.5rem 0;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  overflow: hidden;
}

th,
td {
  padding: 1rem;
  text-align: left;
}

th {
  background-color: var(--primary);
  color: white;
  font-weight: 600;
}

tr:nth-child(even) {
  background-color: #f8fafc;
}

tr:hover {
  background-color: #f1f5f9;
}

/* Code */
pre,
code {
  font-family: "Fira Code", monospace;
  background-color: #f3f4f6;
  border-radius: 6px;
  padding: 0.25rem 0.5rem;
  font-size: 0.9rem;
}

pre {
  padding: 1rem;
  overflow-x: auto;
  margin: 1.5rem 0;
  border-left: 4px solid var(--primary);
}

/* Blockquote */
blockquote {
  border-left: 4px solid var(--primary);
  padding: 1rem 1.5rem;
  margin: 1.5rem 0;
  background-color: #f8fafc;
  border-radius: 0 8px 8px 0;
  font-style: italic;
}

/* Images */
img {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
  margin: 1rem 0;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

/* Utility classes */
.text-center {
  text-align: center;
}
.text-primary {
  color: var(--primary);
}
.bg-light {
  background-color: var(--light);
}
.shadow {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
.rounded {
  border-radius: 8px;
}

/* Responsive */
@media (max-width: 768px) {
  body {
    padding: 1rem;
  }

  h1 {
    font-size: 2rem;
  }
}
</style>
